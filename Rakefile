task :default do
  git = `which git`.strip
  raise "Could not find git - is it in the path? Try 'which git'." unless File.exists?(git)
  
  git_path = File.dirname(git)
  raise "Permission denied - #{git_path} is not writable. Try 'sudo rake' or set the permissions accordingly." unless File.writable?(git_path)
  
  Dir['git-*'].each do |file|
    cp file, git_path
  end
end