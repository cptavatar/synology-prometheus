# Synology + Prometheus + Grafana + Unpoller
This project was forked from https://github.com/prahaladramji/synology-prometheus , then modified 
to add unpoller and to be ansible based. 


## Dependencies
- [Synology Docker](https://www.synology.com/en-global/dsm/packages/Docker) package already installed.
- SSH access to synology.
- Administrator user access.
- ansible installed locally


### Install
- modify inventory/hosts with your synology info
- add a unify user, modify prometheus/defaults/main.yml
- run "run-ansible.sh" to install files
- (on synology for now, easily added to ansible) /usr/local/bin/run-prometheus.sh start  
  

#### Endpoints 
- Grafana `http://<synology ip/hostname>:3000` (this may take upto 15 seconds to start up.)
- Prometheus `http://<synology ip/hostname>:9090`
- Alertmanager `http://<synology ip/hostname>:9093`
- Node-Exporter `http://<synology ip/hostname>:9100/metrics`
- Unpoller `http://<synology ip/hostname>:9130`
