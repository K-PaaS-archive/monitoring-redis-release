## Related Repositories

<table>
  <tr>
    <td colspan=2 align=center>플랫폼</td>
    <td colspan=2 align=center><a href="https://github.com/PaaS-TA/paasta-deployment">어플리케이션 플랫폼</a></td>
    <td colspan=2 align=center><a href="https://github.com/PaaS-TA/paas-ta-container-platform">컨테이너 플랫폼</a></td>
  </tr>
  <tr>
    <td colspan=2 rowspan=2 align=center>포털</td>
    <td colspan=2 align=center><a href="https://github.com/PaaS-TA/portal-deployment">AP 포털</a></td>
    <td colspan=2 align=center><a href="https://github.com/PaaS-TA/container-platform-portal-release">CP 포털</a></td>
  </tr>
  <tr align=center>
    <td colspan=4><a href="https://github.com/PaaS-TA/monitoring-dashboard-source">모니터링 대시보드</a></td>
  </tr>
  <tr align=center>
    <td rowspan=2 colspan=2><a href="https://github.com/PaaS-TA/monitoring-deployment">모니터링</a></td>
    <td><a href="https://github.com/PaaS-TA/monitoring-dashboard-release">Monitoring</a></td>
    <td><a href="https://github.com/PaaS-TA/monitoring-influxdb-release">InfluxDB</a></td>
    <td>🚩 <a href="https://github.com/PaaS-TA/monitoring-redis-release">Redis</a></td>
    <td></td>
  </tr>
  <tr align=center>
    <td><a href="https://github.com/PaaS-TA/monitoring-pinpoint-release">Pinpoint</td>
    <td><a href="https://github.com/PaaS-TA/monitoring-pinpoint-buildpack">Pinpoint Buildpack</td>
    <td><a href="https://github.com/PaaS-TA/monitoring-zabbix-release">Zabbix</a></td>
    <td></td>
  </tr>
  </tr>
  <tr align=center>
    <td rowspan=4 colspan=2><a href="https://github.com/PaaS-TA/service-deployment">AP 서비스</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-CUBRID-RELEASE">Cubrid</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-API-GATEWAY-SERVICE-RELEASE">Gateway</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-GLUSTERFS-RELEASE">GlusterFS</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-APP-LIFECYCLE-SERVICE-RELEASE">Lifecycle</a></td>
  </tr>
  <tr align=center>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-LOGGING-SERVICE-RELEASE">Logging</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-MONGODB-SHARD-RELEASE">MongoDB</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-MYSQL-RELEASE">MySQL</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-PINPOINT-RELEASE">Pinpoint APM</a></td>
  </tr>
  <tr align=center>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-DELIVERY-PIPELINE-RELEASE">Pipeline</a></td>
    <td align=center><a href="https://github.com/PaaS-TA/rabbitmq-release">RabbitMQ</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-ON-DEMAND-REDIS-RELEASE">Redis</a></td>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-SOURCE-CONTROL-RELEASE">Source Control</a></td>
  </tr>
  <tr align=center>
    <td><a href="https://github.com/PaaS-TA/PAAS-TA-WEB-IDE-RELEASE-NEW">WEB-IDE</a></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr align=center>
    <td rowspan=1 colspan=2><a href="https://github.com/PaaS-TA/paas-ta-container-platform-deployment">CP 서비스</a></td>
    <td><a href="https://github.com/PaaS-TA/container-platform-pipeline-release">Pipeline</a></td>
    <td><a href="https://github.com/PaaS-TA/container-platform-source-control-release">Source Control</a></td>
    <td></td>
    <td></td>
  </tr>
</table>
<i>🚩 You are here.</i>

# PaaS-TA monitoring-redis-release Guide

### Create PaaS-TA monitoring-redis-release   
  - Download the latest PaaS-TA Monitoring Redis Release
    ```   
    $ git clone https://github.com/PaaS-TA/monitoring-redis-release.git
    $ cd monitoring-redis-release
    ```
  - Download & Copy "source files" into the src directory
    ```   
    ## download source files
    $ wget -O src.zip https://nextcloud.paas-ta.org/index.php/s/9qCfYSWwgKLQkkD/download

    ## unzip download source files
    $ unzip src.zip

    ## final src directory
    src
     ├── pidutils.sh
     └── redis
        └── 7.0.8.tar.gz

    ```
  - Create PaaS-TA monitoring-redis-release  
    ```   
    ## <VERSION> :: release version (e.g. 5.8.5)
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/monitoring-redis-release-<VERSION>.tgz)
    $ bosh -e <bosh_name> create-release --name=redis --sha2 --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force
    ```
### Deployment
- https://github.com/PaaS-TA/monitoring-deployment
