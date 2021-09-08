# Data Generator APP 
## _on AWS EC2 Instances_

[![Streamlit|io](https://aws1.discourse-cdn.com/business7/uploads/streamlit/original/2X/8/8cb5b6c0e1fe4e4ebfd30b769204c0d30c332fec.png)](https://streamlit.io/)

[![Build Status](https://app.travis-ci.com/Sanpme66/Data_GenerationAPP_AWSEC2.svg?branch=main)](https://travis-ci.org/joemccann/dillinger)

Data Generator is a cloud-enabled EC2 instance deployed APP,mobile-ready, offline-storage compatible,
Streamlit and faker powerd API.

- Generate you own data
- Just for fun
- ✨Magic ✨

## Features

- Import a HTML file and watch it magically convert to Markdown
- Drag and drop images (requires your Dropbox account be linked)
- Import and save files from GitHub, Dropbox, Google Drive and One Drive
- Drag and drop markdown and HTML files into Dillinger
- Export documents as Markdown, HTML and PDF



> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.


## Installation

AWS EC2 requires [Amazon Linux 2 AMI (HVM), SSD Volume ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html) v2019+ to run.

### To launch the EC2 instance and mount an EFS file system

1. Open the **Amazon** [EC2 console](https://console.aws.amazon.com/ec2/).
![](images/EC2console.jpg)
2. Choose **Launch Instance.**

3. **In Step 1:** Choose an Amazon Machine Image (AMI), find an Amazon Linux 2 AMI at the top of the list and choose Select.

4. **In Step 2:** Choose an Instance Type, choose Next: Configure Instance Details.

5. **In Step 3:** Configure Instance Details, provide the following information:

- Leave Number of instances at one.

- Leave Purchasing option at the default setting.

- For Network, choose the entry for the same VPC that you noted when you created your EFS file system in Step 1: Create your Amazon EFS file system.

- For Subnet, choose a default subnet in any Availability Zone.

- For File systems, make sure that the EFS file system that you created in Step 1: Create your Amazon EFS file system is selected. The path shown next to the file system ID is the mount point that the EC2 instance will use, which you can change.

- The User data automatically includes the commands for mounting your Amazon EFS file system.

6. **Choose Next:** Add Storage.

7. **Choose Next:** Add Tags.

8. **Name your instance and choose Next**: Configure Security Group.

9. **In Step 6**: Configure Security Group, set Assign a security group to Select an existing security group. Choose the default security group to make sure that it can access your EFS file system.

>You can't access your EC2 instance by Secure Shell (SSH) using this security group. SSH access isn't required for this exercise. To add access by SSH later, you can edit the default security and add a rule to allow SSH. Or you can create a new security group that allows SSH. You can use the following settings to add SSH access:

- **Type**: SSH

- **Protocol**: TCP

- **Port Range**: 22

- **Source**: Anywhere 0.0.0.0/0

10. Choose **Review and Launch**.

11.  Choose **Launch**.

12. Select the check box for the key pair that you created, and then choose **Launch Instances.**


### Connect to your Linux instance using SSH

1. In a terminal window, use the ssh command to connect to the instance. You specify the path and file name of the private key (.pem), the user name for your instance, and the public DNS name or IPv6 address for your instance. For more information about how to find the private key, the user name for your instance, and the DNS name or IPv6 address for an instance, see Locate the private key and Get information about your instance. To connect to your instance, use one of the following commands.

- (Public DNS) To connect using your instance's public DNS name, enter the following command.

```
ssh -i /path/my-key-pair.pem my-instance-user-name@my-instance-public-dns-name
```
- (IPv6) Alternatively, if your instance has an IPv6 address, to connect using your instance's IPv6 address, enter the following command.
```
ssh -i /path/my-key-pair.pem my-instance-user-name@my-instance-IPv6-address
```
You see a response like the following:
```
The authenticity of host 'ec2-198-51-100-1.compute-1.amazonaws.com (198-51-100-1)' can't be established.
ECDSA key fingerprint is l4UB/neBad9tvkgJf1QZWxheQmR59WgrgzEimCG6kZY.
Are you sure you want to continue connecting (yes/no)?
```
2. (Optional) Verify that the fingerprint in the security alert matches the fingerprint that you previously obtained in (Optional) Get the instance fingerprint. If these fingerprints don't match, someone might be attempting a "man-in-the-middle" attack. If they match, continue to the next step.
3. Enter **yes**.
> You see a response like the following:

```
Warning: Permanently added 'ec2-198-51-100-1.compute-1.amazonaws.com' (ECDSA) to the list of known hosts.
```

## library's

Instructions on how to use them in your own application are linked below.

| Library | Doc |
| ------ | ------ |
| Python 3.8 | https://aws1.discourse-cdn.com/business7/uploads/streamlit/original/2X/8/8cb5b6c0e1fe4e4ebfd30b769204c0d30c332fec.png |
| Streamlit | https://docs.streamlit.io/en/stable/ |
| Faker | https://faker.readthedocs.io/en/master/ |
| Numpy | https://numpy.org/doc/ |
| Pandas | https://pandas.pydata.org/docs/ |
| ASW EC2 | https://docs.aws.amazon.com/efs/latest/ug/gs-step-one-create-ec2-resources.html] |
| bitbucket | https://bitbucket.org/ |


## Contact me 
[Github][PlDb], [linkedin][PlGh], [Emial][PlGd] 
## License

MIT



   [PlDb]: <https://github.com/Sanpme66>
   [PlGh]: <https://www.linkedin.com/in/sanjaysg6633/>
   [PlGd]: <https://www.linkedin.com/in/sanjaysg6633/>
   

#### By.
+ Sanjay S G
+ Sanjaygowda6633

