
# Steps to setup CI/CD Infra 
1. Use e2-aws.template to create CI/CD Infra. This will create VPC, Public & Private Subnets, Jenkins & App Instances, IGW & NAT Gateway.
2. Once the infra is created go to http://{PUBLIC_IP}/jenkins and follow steps to setup Jenkins.
3. Create Pipeline job in Jenkins and copy content of jenkinspipeline and save.
4. Edit ip address in deploy-build/environments/dev/hosts file with Private instance ip and commit change.
5. Login to Jenkins instance, edit /etc/httpd/conf.d/app.conf file, replace localhost with Private instance ip & restart httpd service
6. Run pipeline job & once completed open the url http://{PUBLIC_IP}/spring-petclinic

Note : application startup may take some time
