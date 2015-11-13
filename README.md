# cfn-php-instance
Cloudformation template for a single-instance PHP site with load balancer. The instance is also configured for SES SMTP email sending as well as mounting an S3 bucket as a filesystem using yas3fs.

# Inputs

- InstanceProfile: IAM role name to run the instance under
- DNSPrefix / DNSZone: Combined to create a Route53 DNS entry that points to the ELB
- InstanceType: Size of instance to run
- KeyName: EC2 keypair to assign to the instance
- LoadBalancerSSLCertId: ARN of the SSL cert to assign to the ELB
- SMTPHost: SES SMTP endpoint
- SMTPUser/SMTPPassword: Username and password provided by SES to access the SMTP endpoint
- SMTPVerifiedSender: a verified SES sender which email can be sent from
- Vpcid: ID of the VPC to run the instance and ELB in
- VPCSubnet - a valid VPC subnet to run the instance and ELB in

