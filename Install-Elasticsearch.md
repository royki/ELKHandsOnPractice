##### _Install Elastic in Debian_
-`curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.2.1.deb`
-`sudo dpkg -i elasticsearch-6.2.1.deb`

##### _Check Status of Elasticsearch_
-`sudo service elasticsearch status`

##### _Configure Elasticsearch to start during system startup_
-`systemctl enable elasticsearch`

##### _Run Elasticsearch_
-`sudo /etc/init.d/elasticsearch start` or
-`sudo systemctl start elasticsearch`

##### _Check Elastic is Up and Running_
-`curl -X GET http://localhost:9200`

##### _Troubleshoot_
-`Connection refused error on Elastic Search` / `Elasticsearch memory problems`

```sh
There is insufficient memory for the Java Runtime Environment to continue.
```

- Set network.host to localhost from `.yml`
```sh
/etc/elasticsearch/elasticsearch.yml
network.host: 0.0.0.0
```
OR 
- Change `max heap size` and `min head size` from `jvm.options`
```sh
/etc/elasticsearch/jvm.options

...

################################################################

# Xms represents the initial size of total heap space
# Xmx represents the maximum size of total heap space

-Xms2g
-Xms2g

################################################################

```

##### _Useful links_
|Site|Link|
|----|----|
|Ubu| [https://lxadm.com/Problems_starting_elasticsearch_in_Ubuntu_16.04] |
|SO| [https://stackoverflow.com/questions/29447434/elasticsearch-memory-problems] |
|SO| [https://stackoverflow.com/questions/31677563/connection-refused-error-on-elastic-search] |
|DO| [https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-16-04] |
|DO| [https://www.digitalocean.com/community/tutorials/how-to-install-elasticsearch-logstash-and-kibana-elk-stack-on-ubuntu-16-04] |
|RH| [https://www.rosehosting.com/blog/install-and-configure-the-elk-stack-on-ubuntu-16-04/] |
|ITz| [https://www.itzgeek.com/how-tos/linux/ubuntu-how-tos/setup-elk-stack-ubuntu-16-04.html] |

