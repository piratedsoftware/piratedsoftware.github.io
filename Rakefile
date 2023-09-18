# File name: Rakefile
# Stript type: Rake
# Description: Task creation file for the 'manager.rb' file.

require "./libs/manager.rb"

# Instance class
manager = Manager.new

# Task create header post
# Example: rake post
desc "Create new post"
task :post do
  manager.post_create
end

# Task create header page
# Example: rake page
desc "Create new page"
task :page do
  manager.page_create
end

# Other outputs
def get_stdin(message)
  print message
  STDIN.gets.chomp
end

def ask(message, valid_options)
  if valid_options
    answer = get_stdin("#{message} #{valid_options.to_s.gsub(/"/, '').gsub(/, /,'/')} ") while !valid_options.include?(answer)
  else
    answer = get_stdin(message)
  end
  answer
end
