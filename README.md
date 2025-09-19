ClusterIP:
1. Only for internal service communication inside cluster.

Nodeport Service:
1. service created on top of each node.
2. Need to change firewall rules to allow connection to node port directly.
3. For suitable for production grade projects, as it give direct access to Nodes.

LoadBalancer Service:
1. Lb needs to created for each service.
2. Better than nodeport but not scalable as new service needs new LB.
3. Create cloud specific LB in cloud.

Ingress:
1. Suitable for production projects.
2. client ---> ingress ----> clusterIp for each.
3. Ingress services calls/maps clusterIp service in background.
4. ClusterIp service for each service needs to be created for this.
5. Easy to scale.
6. It will create a global LB in gloud.
