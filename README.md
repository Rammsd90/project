# TASK1:lunchig ec2 instance with type t2.small,volume 10 gb,and elastic ip through cloudformation 
Services - Management Tools - CloudFormation - Create a new stack 
Select Template
Select the template that describes the stack that we want to create.
If you refer to the AWS::EC2::Instance documentation we 'll see that the only required parameter is ImageId
ImageId property refers to the AMI that is used for the instance. For this example, I'll use AMI ami-0cb0e70f44e1a4bb5, which is Amazon linux instance
As mentioned BlockDeviceMappings configure the instance storage. This is done through an array of Block Device Mapping Properties.
In order to configure BlockDeviceMappings you will need to set a few properties. In particular, the DeviceName property is required. This is the mount point for the device, such as /dev/sda1.
The Ebs property is defined by the Amazon Elastic Block Store Block Device Property which allows us to configure the following properties:
Iops - provisioned Iops
VolumeSize - size of the volume in GB
VolumeType - gp2 for General Purpose SSD, io1 for Provisioned IOPS SSD
Now we can specify the type of instance here with InstanceType: t2.small
then mention ami-id here with the ImageId: ami-0cb0e70f44e1a4bb5
after that we have specify the key-pair,security group and subnet id.
if we refer to the AWS::EC2::EIP, it will see that the requied parameter for the elastic ip
******************************************************************************************************************************************
Task2:Lunch Nginx with ssl using ansible playrbook including roles
1.we are using the roles for the code reuse
2.first i create role with nginx with plays
Here's what you get with this role:

3.Configure 1 or more sites-enabled (virtual hosts)
4.Configure 0 or more upstreams per virtual host
5.Configure a working nginx playbook in as little as 3 lines of YAML
6.Forced HTTPS with A+ certificate ratings (bearing your certificate authority)
7.Self signed certs are generated to work out of the box for non-production environments
8.First class support for Let's Encrypt SSL certificates for production environments
9.Tune a bunch of nginx.conf settings for performance
10.Allow you to optionally declare custom nginx and vhost directives easily
11.Allow you to easily customize your upstream's proxy settings
