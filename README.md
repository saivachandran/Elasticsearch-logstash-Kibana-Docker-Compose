# Elasticsearch-logstash-Kibana-Docker-Compose
Create ELK stack using Docker Compose
# create directory
```
mkdir elk

cd elk

```


vim logstash.conf

add below contnetnt in logstatsh.conf file
```
input {

    file {

        path => "/root/temp/inlog.log"
    }
}

output {

    elasticsearch {

        hosts => ["http://elasticsearch:9200"]
    }
}
```

# back to elk folder

create docker-compose.yaml file use yaml file 

# back to root director

create directory temp
```
mkdir temp

cd /root/temp

```

vim inlog.log

This is elk stack

save the file


# now up the docker compose file
```
docker-compose -f docker-compose up -d
```




