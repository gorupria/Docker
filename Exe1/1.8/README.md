## Link to docker hub
https://cloud.docker.com/repository/docker/purushot/ratebeer

## Prerequisites
Install rails.
<br/>
For example get it from the image rails:onbuild
https://hub.docker.com/_/rails/

## For some reason yarn needs to be installed separately to get the rails server running. 
Install yarn and node.
`curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -`
`curl -sL https://deb.nodesource.com/setup_8.x | bash`
`echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list`

`apt-get install -y nodejs`
`apt-get update && apt-get install -y yarn`

For rails sever to start properly following environments need to be set. 
NODE_ENV=development
RAILS_ENV=development
WEBPACKER_DEV_SERVER_HOST=0.0.0.0

## Be sure to run migrations before running the application. The application will run even without CMD configuration
because rails:onbuild has the CMD configuration that runs the rails server.  




