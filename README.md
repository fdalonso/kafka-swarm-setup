# kafka-swarm-setup
kafka docker-compose.yml to be used with docker swarm. setup is prepared to prd envs.

this docker-compose is using KRaft kafka mode instead zookeeper configuration, since the use of zookeeper will be discontinued in further kafka releases.
more information here: https://developer.confluent.io/learn/kraft/

# tips
- don't forget to first create a new swarm network with swarm scope.
  references here: https://docs.docker.com/reference/cli/docker/network/create/
- turn-on swarm mode in your docker installation
- create the appropriated swarm nodes and join then to swarm master
- run: 'docker stack deploy -c docker-compose.yml <stack name>' to bring all services up
- certificate keystore and truststore, could also be JKS. Make appropriate adjustments to do that.
