### Project Title - Deploy a high-availability web app using CloudFormation

This folder provides the starter code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:

## Run

First thing is to create a IAm role called "UdacityS3ReadOnlyEC2" that allow read on S3 with the following permission

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*"
            ],
            "Resource": "*"
        }
    ]
}
```

then you can simply run the command `./utils/create.sh udacity-devops ./udacity-devops.yml udacity-parameters.json` from the root of the project

## Result

One output of the cloudformation script is the dns of the load balancer that you can use the access your app!
