# collector-aws
## Setup Grafana on EC2 instance
```bash
sudo yum update -y
sudo yum install docker -y
# run Grafana instance on docker
docker run -d -p 3000:3000 --name=grafana  grafana/grafana
```
## Add Database and Dashboard Using Grafana's UI
- Go to EC2's DNS\IP at port 3000.
- Login with the credentials "admin" "admin", and than change the password when asked.
- Go to Home --> Connections --> Add new connection --> Mysql and add Collector's RDS credentials.
- Go to Home --> Dashboards --> New Dashboard --> Import a dashboard and upload grafana's json (can be exported from current dashboard, will be uploaded to github soon).
