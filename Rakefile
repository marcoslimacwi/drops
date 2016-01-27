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
  puts "Edite o arquivo #{@data_file} com seus dados"
end

def prepare_name(name)
  name.gsub(/\s+/, '').downcase
end

def set_file_paths(name)
  @page_file = "autores/#{name}.md"
  @data_file = "_data/authors/#{name}.yml"
end

def check_files_existence(name)
  if File.exist?(@page_file) || File.exist?(@data_file)
    raise "Autor #{name} já existe"
  end
end

def create_author_page(name)
  content = File.open("_templates/author", "rb").read
  template = Liquid::Template.parse(content)
  result = template.render('name' => name)
  File.open(@page_file, 'w') {|f| f.write(result) }
end

def create_author_data(name)
  content = File.open("_templates/author_data", "rb").read
  template = Liquid::Template.parse(content)
  result = template.render('name' => name)
  File.open(@data_file, 'w') {|f| f.write(result) }
end
