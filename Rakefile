require 'rake/remote_task'

set :domain, 'pichot.webfactional.com'

task default: [:deploy, :restart_apache]

task :deploy do
  sh "rsync -rtz --delete src/flavors/betterblockgr/ wf:~/webapps/shareabouts_web/shareabouts/src/flavors/betterblockgr/"
end

remote_task :restart_apache do
  run "~/webapps/shareabouts_web/apache2/bin/restart"
end
