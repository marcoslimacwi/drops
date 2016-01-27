require 'rake'
require 'liquid'

task :author do
  ARGV.each { |a| task a.to_sym do ; end }
  name = ARGV[1]
  name = prepare_name name
  set_file_paths name
  check_files_existence name
  create_author_page name
  create_author_data name
  puts "Criado author #{name}"
  puts "Edite o arquivo #{@data_file_path} com seus dados"
end

def prepare_name(name)
  name.gsub(/\s+/, '').downcase
end

def set_file_paths(name)
  @page_file_path = "autores/#{name}.md"
  @data_file_path = "_data/authors/#{name}.yml"
end

def check_files_existence(name)
  if File.exist?(@page_file_path) || File.exist?(@data_file_path)
    raise "Autor #{name} já existe"
  end
end

def create_author_page(name)
  create_author_file "_templates/author", @page_file_path, 'name' => name
end

def create_author_data(name)
  create_author_file "_templates/author_data", @data_file_path, 'name' => name
end

def create_author_file(template_path, destination_path, params)
  puts params
  content = File.open(template_path, "rb").read
  template = Liquid::Template.parse(content)
  result = template.render(params)
  File.open(destination_path, 'w') {|f| f.write(result) }
end
