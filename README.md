# Amazon S3 – Static Website Deployment

## Codomax AWS Cloud & DevOps Internship | Module 03

### Project Overview

This project demonstrates how to host a static website using Amazon Simple Storage Service (Amazon S3) without managing a traditional web server.

As part of Module 03 of the Codomax AWS Cloud & DevOps Internship, I configured an S3 bucket, uploaded website files, managed access permissions, and successfully deployed a publicly accessible static website.

### Technologies Used

- Amazon Web Services (AWS)
- Amazon S3
- HTML5
- CSS3
- AWS IAM and S3 Bucket Policies
- GitHub

### AWS Configuration

| Component | Configuration |
|---|---|
| AWS Service | Amazon S3 |
| Region | Asia Pacific (Sydney) – ap-southeast-2 |
| Bucket Type | General purpose |
| Bucket Namespace | Account Regional |
| Object Ownership | Bucket owner enforced (ACLs disabled) |
| Storage Class | S3 Standard |
| Bucket Versioning | Disabled |
| Encryption | SSE-S3 |
| Static Website Hosting | Enabled |
| Index Document | index.html |
| Public Access | Read-only access using bucket policy |

### Implementation Steps

**1. Created an Amazon S3 Bucket**

Created a general-purpose S3 bucket in the Asia Pacific (Sydney) Region.

**2. Uploaded Website Files**

Uploaded the HTML website files to the S3 bucket using the AWS Management Console.

**3. Enabled Static Website Hosting**

Configured the bucket to host a static website using `index.html` as the index document.

**4. Configured Access Permissions**

Configured the necessary bucket-level public access settings and added a bucket policy granting public read-only access to the website objects.

**5. Tested the Website**

Accessed the S3 static website endpoint through a browser to verify successful deployment.

### Architecture

```text
       Internet Users
              |
              v
         Web Browser
              |
              | HTTP Request
              v
     Amazon S3 Website Endpoint
              |
              v
         S3 Bucket
              |
              v
        index.html
              |
              v
       Static Website
```

Unlike Amazon EC2, Amazon S3 does not require an operating system or Apache web server to host static HTML, CSS, and JavaScript files.

### Live Website

http://codomax-module03-2026-041711547617-ap-southeast-2-an.s3-website-ap-southeast-2.amazonaws.com

### Security Considerations

- Used ACLs-disabled object ownership.
- Configured public read-only access for website files.
- Did not enable public write permissions.
- Used server-side encryption with Amazon S3-managed keys.
- Avoided uploading private credentials or sensitive data.
- Restricted the project to non-sensitive static content.

**Note:** Amazon S3 website endpoints support HTTP only. A production website should use HTTPS, typically through Amazon CloudFront with a private S3 origin.

### Learning Outcomes

Through this project, I learned how to:

1. Understand S3 buckets, objects, and storage classes.
2. Create and configure an Amazon S3 bucket.
3. Upload and manage files using the AWS Console.
4. Understand public access settings and bucket policies.
5. Enable static website hosting.
6. Deploy a website without managing an EC2 server.
7. Compare EC2-based and S3-based website hosting.

### Conclusion

This project provided practical experience with AWS object storage, basic cloud security, and static website deployment.

By completing this module, I gained a better understanding of how Amazon S3 can be used to host static web content without maintaining a virtual server.

This knowledge provides a foundation for future AWS projects involving cloud networking, databases, serverless computing, and CI/CD.

---

**Codomax Digital Solutions | AWS Cloud & DevOps Virtual Internship 2026**
