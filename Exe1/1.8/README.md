## Link to docker hub
https://cloud.docker.com/repository/docker/purushot/ratebeer

## Prerequisites
Install rails.
<br/>
For example get it from the image rails:onbuild <br/>
https://hub.docker.com/_/rails/

## For some reason yarn needs to be installed separately to get the rails server running. 
Install yarn and node. <br/>
`curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -` <br/>
`curl -sL https://deb.nodesource.com/setup_8.x | bash` <br/>
`echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list` <br/>

`apt-get install -y nodejs` <br/>
`apt-get update && apt-get install -y yarn` <br/>

For rails sever to start properly following environments need to be set. <br/>
NODE_ENV=development <br/>
RAILS_ENV=development <br/>
WEBPACKER_DEV_SERVER_HOST=0.0.0.0 <br/>

## Be sure to run migrations before running the application. The application will run even without CMD configuration because rails:onbuild has the CMD configuration that runs the rails server.  




