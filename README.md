# cloudwatch-agent
  * You can create a custom metrics for Memory usages using cutom metrices
  * After you are connected to the instance, type below command:
  * sudo yum install perl-Switch perl-Switch perl-DateTime perl-Sys-Syslog perl-LWP-Protocol-https -y
#### Download custom monitoring script provided by AWS
  * curl http://aws-cloudwatch.s3.amazonaws.com/downloads/CloudWatchMonitoringScripts-1.2.1.zip -O
  * unzip the file and go inside the folder
  * By default aws resources can't talk with each other, so you should give the roles or permissions.
  * Go to instance settings, and attach/replace IAM Role
  * You may give Admin access for practice, but it's recommmended to give Cloudwatch access 
#### To keep the Metrics onto cloudwatch
  * ./mon-put-instance-data.pl --mem-util --mem-util --mem-used-incl-cache-buff --mem-used --mem-avail
  * Now go to EC2 console and click on monitoring tab on buttom, click on view-CLoudWatch metrices.
  * Note the right instance id. Click on Linux System under custom namespaces and click on InstanceId.
  * You can now select the metric Name and see the results in line or percentage.
  
#### Automating the metrices
  * We don't want to put the metrices every time manually. The whole point of metrices is to monitor our instances without having to go into them. 
  * Let's schedulte the monitoring in 1 minute for our lab. You may want to do it in 5 mins or so. 
  
