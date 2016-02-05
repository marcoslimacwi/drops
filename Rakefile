require 'rake'
require 'liquid'

task :author do
  ARGV.each { |a| task a.to_sym do ; end }
  username = ARGV[1]
  username = prepare_username username
  set_file_paths username
  check_files_existence username
  create_author_page username
  create_author_data username
  print_end_message username
end

def prepare_username(username)
  username.gsub(/\s+/, '').downcase
end

def set_file_paths(username)
  @page_file_path = "autores/#{username}.md"
  @data_file_path = "_data/authors/#{username}.yml"
end

def check_files_existence(username)
  raise "Autor #{username} já existe" if File.exist?(@page_file_path) || File.exist?(@data_file_path)
end

def create_author_page(username)
  create_author_file "_templates/author", @page_file_path, 'username' => username
end

def create_author_data(username)
  create_author_file "_templates/author_data", @data_file_path, 'username' => username
end

def create_author_file(template_path, destination_path, params)
  content = File.open(template_path, "rb").read
  template = Liquid::Template.parse(content)
  result = template.render(params)
  File.open(destination_path, 'w') {|f| f.write(result) }
end

def print_end_message(username)
  puts
  puts "    Criado author #{username}!"
  puts
  puts " -> Arquivos criados:"
  puts " ->   - arquivo de dados do autor (#{@data_file_path})"
  puts " ->   - arquivo que gera a página do autor (#{@page_file_path})"
  puts " -> Edite o arquivo #{@data_file_path} com seus dados"
  puts
end
