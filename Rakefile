task :watch do
  server = Process.spawn("jekyll")
  compass = Process.spawn("compass watch --poll")
end

task :server do
  server = Process.spawn("jekyll --server")
  compass = Process.spawn("compass watch --poll")
end

task :pow_setup do
  powder = Dir.home()+"/.pow"
  if File.directory? powder
    begin
      puts "Enter the desired domain name."
      gets domain
      File.symlink(Dir.pwd, powder+"/"+domain)
    rescue NotImplementedError=>e
      puts "POW setup failed. The " + e.to_s + "."
    end
  else
    puts "It does not appear that POW is installed."
  end
end