# Hosting a Static Website on Amazon S3 with Secure Access
Hosting a Static Website on Amazon S3 with Secure Access

#### Problem Statement
Nowadays increasing the demand of cost-effective, highly available, and globally accessible websites.  

Traditional web hosting: involved complex process like manage server configure softwares. it leads to high operational overhead making them unsuitable for projects with limited resources or scalability requirements.  

Amazon S3: offers a server-less, scalable alternative that enables users to host static websites with minimal configuration.  

When we need this use case:  
- Hosting Static Websites
- Scalable and Cost-Effective
- Global Content Delivery
- Security with Simple Access Control

Advantages:  
- Availability and Durability
- Scalability 5TB
- Security
- Cost Effective
- Performance

![diagram](diagram.png)


Step 1  
I have created a s3.

Step 2  
Add files in the bucket inside s3.

Step 3  
Add Static website hosting (Properties)

![steps](steps1.png)

Step 4  
Edit permmision and provide policy 

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::demo-website-vibin/*"
        }
    ]
}
```

We can see the output by clicking link in web hosting.  

### Conclusion
By configuring a secure bucket policy, you can easily host a static website on Amazon S3 and control access efficiently. This approach ensures that the website is publicly accessible for reading, while preventing unauthorized users from modifying or deleting the content. Additionally, integrating AWS CloudFront with your S3 bucket can improve content delivery speed globally, enhancing the user experience while maintaining a secure environment for your files.  
