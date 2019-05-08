# Administering a Raspberry Pi with AWS Systems Manager

We use ssm (particularly https://github.com/guardian/ssm-scala) for remote shell
access to our EC2 instances, as an alternative to `ssh` that has better user &
credential management, and we can actually do the same thing with the
Raspberry Pi computers that we host within the building. This can be convenient
if, for instance the Raspberry Pi is physically hard to get to (the Ophan one is 
stored down in the basement), or isn't connected to a keyboard/mouse itself.

This blog post by Amazon tells you it can be done...

https://aws.amazon.com/blogs/mt/manage-raspberry-pi-devices-using-aws-systems-manager/

...but there are a couple of places where you'll need to modify the instructions.

```
$ aws ssm create-activation --profile ophan --default-instance-name SomeRPiName --iam-role SSMServiceRole --registration-limit 1 --region eu-west-1
```
