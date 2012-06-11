task :watch do
  system "compass compile --css-dir source/css" unless File.exist?("source/css/style.css")
  server = Process.spawn("jekyll")
  compass = Process.spawn("compass watch")
  trap("INT") {
    [server, compass].each { |pid| Process.kill(9, pid) rescue Errno::ESRCH }
    exit 0
  }
  [server, compass].each { |pid| Process.wait(pid) }
end
 
task :server do
  system "compass compile --css-dir source/css" unless File.exist?("source/css/style.css")
  server = Process.spawn("jekyll --server")
  compass = Process.spawn("compass watch")
  trap("INT") {
    [server, compass].each { |pid| Process.kill(9, pid) rescue Errno::ESRCH }
    exit 0
  }
  [server, compass].each { |pid| Process.wait(pid) }
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