require "rubygems"
require "tmpdir"

require "bundler/setup"
require "jekyll"


# Change your GitHub reponame
GITHUB_REPONAME = "tony-jones/2015-portfolio"
git@github.com:tony-jones/2015-portfolio.git

def say_what? message
  print message
  STDIN.gets.chomp
end


def sluggize str
  str.downcase.gsub(/[^a-z0-9]+/, '-').gsub(/^-|-$/, '');
end

desc "Generate blog files"
task :generate do
  Jekyll::Site.new(Jekyll.configuration({
    "source"      => ".",
    "destination" => "_site"
  })).process
end


desc "Generate and publish blog to gh-pages"
task :publish => [:generate] do
  Dir.mktmpdir do |tmp|
    cp_r "_site/.", tmp

    pwd = Dir.pwd
    Dir.chdir tmp

    system "git init"
    system "git add ."
    message = "Site updated at #{Time.now.utc}"
    system "git commit -m #{message.inspect}"
    system "git remote add origin git@github.com:#{GITHUB_REPONAME}.git"
    system "git push origin gh-pages -f"

    Dir.chdir pwd
  end
end

# Task that allows you create post with today's date
desc "Create a new post"
task :new do
  title     = say_what?('Title: ')
  filename  = "_posts/#{Time.now.strftime('%Y-%m-%d')}-#{sluggize title}.markdown"

  if File.exist? filename
    puts "Can't create new post: \e[33m#{filename}\e[0m"
    puts "  \e[31m- Path already exists.\e[0m"
    exit 1
  end

  File.open(filename, "w") do |post|
    post.puts "---"
    post.puts "layout:    post"
    post.puts "title:     #{title}"
    post.puts "---"
    post.puts ""
    post.puts "Once upon a time..."
  end

  puts "A new post was created for at:"
  puts "  \e[32m#{filename}\e[0m"
end

# Task that allows you create post and enter the post date.
desc "import an old post"
task :import do
  title     = say_what?('Title: ')
  year      = say_what?('Year(i.e. 2015): ')
  month     = say_what?('Month(i.e. 09): ')
  day       = say_what?('Day(i.e. 21): ')
  filename  = "_posts/#{sluggize year}-#{sluggize month}-#{sluggize day}-#{sluggize title}.markdown"

  if File.exist? filename
    puts "Can't create new post: \e[33m#{filename}\e[0m"
    puts "  \e[31m- Path already exists.\e[0m"
    exit 1
  end

  File.open(filename, "w") do |post|
    post.puts "---"
    post.puts "layout:    post"
    post.puts "title:     #{title}"
    post.puts "---"
    post.puts ""
    post.puts "Once upon a time..."
  end

  puts "A new post was created for at:"
  puts "  \e[32m#{filename}\e[0m"
end
