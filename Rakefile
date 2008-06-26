WWW_FILES = FileList["www/*"] + FileList["bin/*"]

task :upload_webpage => WWW_FILES do |t|
  sh "rsync -essh -caz #{t.prerequisites * ' '} wmorgan@rubyforge.org:/var/www/gforge-projects/git-wt-commit/"
end

# vim: syntax=ruby
