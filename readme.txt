### Run docker UI and All Plugin Kafka ###
docker run --rm -p 2181:2181 -p 3030:3030 -p 8081-8083:8081-8083 \
       -p 9581-9585:9581-9585 -p 9092:9092 -e ADV_HOST=127.0.0.1   \
       landoop/fast-data-dev:latest

### Mapping server port and expose to public ###
./ngrok http 1323

### Install all dependency project package ####
go env -w GO111MODULE=auto
go get ./...