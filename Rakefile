namespace :greeting do
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end
desc 'outputs hello in spanish to the terminal'
task :hola do
  puts "hola de Rake!"
end
end

desc 'connects the environment .rb from the config folder'
task :environment do
  require_relative './config/environment'
end


namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
    puts "migration is complete!"
  end
end  

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
