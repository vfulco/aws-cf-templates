# aws-cf-templates

## Wordpress

Use this template to create a **highly available** and **scalable** Wordpress environment within minutes.

### Components

#### AWS services

* EC2: virtual servers running Apache serving Wordpress (PHP application)
* RDS: highly available MySQL database
* S3: stores and delivers uploaded media files (e.g. images, videos, ...)
* ELB: distributes incoming HTTP requests to multiple virtual servers
* VPC: environment is running in a separate private network
* Auto Scaling: manages the fleet of virtual servers
* CloudWatch: monitors the usage of the virtual servers and adds or removes additional servers if needed

#### Others

* Wordpress plugins: amazon-web-services and amazon-s3-and-cloudfront
* Wordpress CLI: wp-cli 

### Installation Guide

1. Open AWS CloudFormation within the Management Console: [https://console.aws.amazon.com/cloudformation](https://console.aws.amazon.com/cloudformation).
1. Create a new stack by clicking on the **Create Stack** button.
1. Select **Upload a template to Amazon S3* and upload the JSON-file **wordpress-ha.json** from this repository.
1. Click **Next** to proceed with the next step of the wizard.
1. Specify a name and all parameters for the stack.
1. Click **Next** to proceed with the next step of the wizard.
1. Click **Next** to skip the **Options** step of the wizard.
1. Check the **I acknowledge that this template might cause AWS CloudFormation to create IAM resources.** checkbox.
1. Click **Create** to start the creation of the stack.
1. Wait until the stack reaches the state **CREATE_COMPLETE**
1. Grab the URL of the Wordpress environment from the **Outputs** tab of your stack.

### Limitations

* It is not possible to install plugins or themes with the web interface at the moment as the changes are not propagated to all servers automatically.

### Support needed?

Do you need help? Mail to [team@widdix.de](mailto:team@widdix.de).