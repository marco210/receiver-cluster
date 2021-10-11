# THANOS RECEIVE CLUSTER TEST
A Docker compose file configuration to demonstrate Thanos Receive 3 nodes cluster
1. To run docker compose
  * `git clone`
  * `docker-compose up -d`
# ARCHITECTURE
![markdown](https://github.com/marco210/receiver-cluster/blob/master/images/thanos-receive.png)
# COMPONENT
1. Prometheus
2. Thanos Receive
3. Minio
4. Thanos Store
5. Thanos Query

# REFERENCES
1. https://github.com/thanos-io/thanos/blob/main/docs/components/receive.md
2. https://github.com/thanos-io/thanos/blob/main/docs/components/compact.md
3. https://github.com/thanos-io/thanos/blob/main/docs/components/query.md
4. https://github.com/thanos-io/thanos/blob/main/docs/components/store.md
5. https://github.com/thanos-io/thanos/blob/main/docs/proposals-done/201812-thanos-remote-receive.md
