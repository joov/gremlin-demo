#GREMLIN Demo

Demo consists of two docker-containers
* gremlin-server (port 8182)
* gremlin-graphexp javascript frontent (port 8183)

Both are started as docker-containers from a docker-compose file.
If you have docker-compose running you can simply start by tying 
`docker-compose up -d`

If you are on a windows machine, install vagrant and virtualbox.
Then you can start with `vagrant up`, ssh into the vbox (e.g. with putty)
and start the docker-containers there (directory is `/vagrant`)