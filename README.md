Sample Vagrant configuration that starts up **Ubuntu 20.04** box, then runs an **Ansible** playbook that does the following:
* Installs Docker, Docker-compose, and Node Exporter
  * Node Exporter is installed through a [Cloud Alchemy role](https://github.com/cloudalchemy/ansible-node-exporter)
* Starts two Docker containers:
  * Prometheus, preconfigured to collect metrics from host VM's Node Exporter
  * Grafana, preconfigured to use Prometheus as the data source and [Node Exporter Full dashboard](https://grafana.com/grafana/dashboards/1860) to visualize metrics

After VM is provisioned, Grafana should be available at http://localhost:3000

--------------
Конфигурация Vagrant, запускающая бокс **Ubuntu 20.04** и плейбук **Ansible** для следующих действий:
* Установка Docker, Docker-compose и Node Exporter
  * Node Exporter устанавливается с помощью [роли Cloud Alchemy](https://github.com/cloudalchemy/ansible-node-exporter)
* Запуск двух контейнеров Docker:
  * Prometheus, настроенный на сбор метрик с Node Exporter хостовой ВМ
  * Grafana, настроенная на использование Prometheus в качестве источника данных и с [дашбордом Node Exporter Full](https://grafana.com/grafana/dashboards/1860) для визуализации метрик

После подготовки ВМ, Grafana должна быть доступна на http://localhost:3000
