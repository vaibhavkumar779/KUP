# AWS Assignment


**AWS CLI S3 commands**

cp copy syntax cp or or

ls list ls or NONE

mb aws s3 mb s3://mybucket

mv Move command mv or or

rm The following rm command deletes a single s3 object: aws s3 rm s3://mybucket/test2.txt


**Why /16 is used in subnet?**

* Class A Example - /8 - 16 Million Hosts
* Class B Example - /16 - 65,000 Hosts
* Class C Example - /24 - 254 Hosts

**What is Power user access ?**

When we make any user to power aser access it means you that user has full permission to create any resources or use any service ,but doesn't have ability to manage IAM users . We can say its similar to administrator.

**Difference between NACL & Security groups ?**

In simple words we can say that NACL perform security at subnet level and security group perform security at instance level . What are Endpoints ? Endpoints act as NAT gateway , but its cheaper than NAT gateway and in this we can give access to particular service for private subnet .
 

**What is difference bewteen IGW and Nat Gateway?**

* Igw- An Internet Gateway allows resources within your VPC to access the internet, and vice versa.
* NAT-It allows resources in a private subnet to access the internet.
 It only works one way. The internet at large cannot get through your NAT to your private resources unless you explicitly allow it.

**What is Cidr?**

Classless inter-domain routing is a set of Internet protocol standards that is used to create unique identifiers for networks and individual devices andThe host identifier is used to determine which host or device on the network should receive incoming information packets.
 
**What are Elastic IP addresses?**

An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is allocated to your AWS account, and is yours until you release it. By using an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account. Alternatively, you can specify the Elastic IP address in a DNS record for your domain, so that your domain points to your instance. For more information, see the documentation for your domain registrar, or Set up dynamic DNS on Your Amazon Linux instance.

An Elastic IP address is a public IPv4 address, which is reachable from the internet. If your instance does not have a public IPv4 address, you can associate an Elastic IP address with your instance to enable communication with the internet. For example, this allows you to connect to your instance from your local computer.


**What does SCP use?**

The SCP is a network protocol, based on the BSD RCP protocol, which supports file transfers between hosts on a network. SCP uses Secure Shell (SSH) for data transfer and uses the same mechanisms for authentication, thereby ensuring the authenticity and confidentiality of the data in transit.


**What is Power user access ?**

When we make any user to power aser access it means you that user has full permission to create any resources or use any service ,but doesn't have ability to manage IAM users . We can say its similar to administrator.

 
**Difference between NACL & Security groups ?** 

In simple words we can say that NACL perform security at subnet level and security group perform security at instance level . What are Endpoints ? Endpoints act as NAT gateway , but its cheaper than NAT gateway and in this we can give access to particular service for private subnet .

