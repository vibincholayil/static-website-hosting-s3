# static-website-s3
Hosting a Static Website on Amazon S3 with Secure Access


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
create iam policy
Cloudfront - Content Delivery Network (CDN) 
CloudFront caches that content at edge locations (data centers) around the world
