🚀 Hosting a Static Website on Amazon S3
Turn your S3 bucket into a highly available, blazing-fast website in just a few steps! AWS S3 makes it easy to serve static content with scalability and cost efficiency.
🌟 Why Host on S3?
- No server hassles – Fully managed static hosting
- Scalable & cost-effective – Pay for storage & data transfer, no fixed costs
- Seamless integration – Works with AWS services like CloudFront for HTTPS

- Prerequisites
Before you get started, ensure you have:
- An AWS account
- A registered domain (optional but recommended)
- A basic understanding of AWS S3

Steps to Host Your Website
- Create an S3 Bucket- Navigate to the AWS S3 Console.
- Click "Create Bucket."
- Set the bucket name (must be globally unique).
- Choose the correct region and enable "Block Public Access."

- Enable Static Website Hosting- Go to the bucket properties.
- Find "Static website hosting" and enable it.
- Set the index document (e.g., index.html).

- Upload Website Files- Click "Upload" in the S3 bucket.
- Add all necessary HTML, CSS, and JS files.
- Set public read permissions if required.

- Set Bucket Policy for Public Access (if making the site public)- Navigate to "Permissions" → "Bucket Policy."
- Add a policy like the following:
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}

- Access Your Website- Navigate to the "Static Website Hosting" section in S3 properties.
- Use the provided URL to access your website.









