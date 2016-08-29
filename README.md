# go-neo4j-docker
Sample App to demonstrate Go using Neo4J in docker

## Links

https://neo4j.com/developer/go/
https://github.com/neo4j-examples/movies-go-cq
https://github.com/go-cq/cq
https://neo4j.com/developer/example-project/
https://neo4j.com/developer/docker/


## Quick Start

Clone the app

    cd <your-workspace-root>
    git clone git@github.com:atharrison/go-neo4j-docker.git
    
Get the Go dependencies

    cd go-neo4j-docker
    export GOPATH=<your-workspace-root>/go-neo4j-docker
    cut -d' ' -f3 dependencies.txt | xargs -n1 -pI package go get package
    
    # Hit 'y' and enter if prompted
    > go get github.com/daaku/go.httpgzip?...y
    > go get github.com/jmoiron/sqlx?...y
    > go get gopkg.in/cq.v1?...y

Build the app

    docker-compose build
    
Start the containers

    docker-compose up
    
Populate the Movies DB

* Visit [http://localhost:7474/browser/](http://localhost:7474/browser/)
* When prompted for user/pass, use the default of neo4j/neo4j
* It will ask you to enter a new password. Enter `password`
* In the prompt, type `:play movies`, then press enter
* Click the output of that result, then hit the "play" icon in the top-right to execute

Browse the Movies app

* Visit [http://localhost:8080/](http://localhost:8080/)
* Enter a search criteria in the box, and hit 'Search'

