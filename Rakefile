task :default do
  puts "Welcome to Rob's MacBook!"
end

desc "Prints current date and time"
task :time do
  puts Time.new
end

desc "Prints a nice greeting"
task :greet do
  puts "What's your name?"
  name = STDIN.gets.chomp
  puts "Hello #{name}!"
end

task :print_favorite_food do
  puts ENV['FAVORITE_FOOD']
end

namespace :morning_activities do
  task :wake_up do
    puts "I'm awake!"
  end

  task :get_dressed => :wake_up do
    puts "And now I can get dressed."
  end

  task :eat_breakfast do
    puts "Must eat breakfast. Important meal."
  end

  task :brush_teeth do
    puts "Brushing your teeth is sanitary.  Gotta do that."
  end

  task :ready_for_class =>[:wake_up,:eat_breakfast, :brush_teeth] do
    puts "Now I'm ready for class"
  end
end
