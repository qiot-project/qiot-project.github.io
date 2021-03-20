# Including only the changed build task
require 'jekyll'

task :build do
  config = Jekyll.configuration({ 
    'source' => './', 
    'destination' => './_site' 
  })
  site = Jekyll::Site.new(config)
  Jekyll::Commands::Build.build site, config
end