# 🌐 Static Website Hosting on Amazon S3

## 📌 Project Overview
This project demonstrates how to host a **static website on Amazon S3** using AWS cloud services. The website is fully serverless, highly scalable, and cost efficient, making it ideal for portfolios, landing pages, and documentation sites. The project includes a modern AWS & DevOps themed UI hosted using **Amazon S3 Static Website Hosting**.


## 🛠️ AWS Services Used
- Amazon S3  
- AWS IAM  
- Amazon S3 Static Website Hosting  


## 📂 Project Structure
```
Static-Website-S3
├── index.html
├── error.html
└── README.md
```


## 🚀 Step by Step Implementation Guide

### 🧩 Step 1. Create Website Files
Create the following files on your local system:
- `index.html` for the main website
- `error.html` for error handling

These files contain HTML, CSS, and JavaScript in a single file format.


### 🪣 Step 2. Create an S3 Bucket
1. Open AWS Management Console  
2. Go to **Amazon S3**  
3. Click **Create bucket**  
4. Enter a globally unique bucket name  
5. Select a region  
6. Keep remaining settings default  
7. Create the bucket  

📌 Tip: Bucket name should be meaningful and easy to identify.
![MasterHead](https://github.com/user-attachments/assets/9c952d2e-d86d-42d0-96b2-82b7aa808257)


### 📤 Step 3. Upload Website Files
1. Open the created S3 bucket  
2. Click **Upload**  
3. Upload:
   - `index.html`
   - `error.html`
4. Complete the upload
![MasterHead](https://github.com/user-attachments/assets/3e719930-c7b3-4e5f-8689-72ba2b77cbb2)


### 🌐 Step 4. Enable Static Website Hosting
1. Open the bucket  
2. Go to **Properties**  
3. Scroll to **Static website hosting**  
4. Enable static website hosting  
5. Configure:
   - Index document: `index.html`
   - Error document: `error.html`
6. Save changes  
![MasterHead](https://github.com/user-attachments/assets/faae3b7c-33d5-4dc4-a208-b79a713adc8c)

### 🔓 Step 5. Disable Block Public Access
1. Go to **Permissions** tab  
2. Open **Block public access**  
3. Edit settings  
4. Uncheck all options  
5. Save changes and confirm  
![MasterHead](https://github.com/user-attachments/assets/2ba6cc4f-8b59-43d1-a5d2-5f81ac626480)


### 📜 Step 6. Add Bucket Policy
Add the following bucket policy to allow public read access:

```
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
```
![MasterHead](https://github.com/user-attachments/assets/e15c4bce-5289-4410-a867-38edf3e23a57)

### 🔍 Step 7. Verify Bucket Permissions
After adding the bucket policy, verify that public access is correctly configured.

- Ensure **Block Public Access** is disabled  
- Confirm the bucket policy status shows **Public**  
- Check that objects inside the bucket are publicly readable  



### 🌐 Step 8. Access the Website
1. Go to the **Properties** tab of your S3 bucket  
2. Scroll to **Static website hosting**  
3. Copy the **Bucket website endpoint URL**  
4. Paste the URL into a web browser  

✅ Your static website should load successfully.
![MasterHead](https://github.com/user-attachments/assets/2a5f254b-c455-472c-a003-28bb22d10c68)

### 🧹 Step 9. Clean Up Resources
To avoid unnecessary charges:

- Delete the S3 bucket when no longer required  
- Or remove uploaded objects if testing is complete  

⚠️ Always clean up unused cloud resources.


## 🧠 Final Architecture Flow
- 👤 User requests website URL  
- 🌍 Browser connects to S3 website endpoint  
- 📦 S3 retrieves static files  
- 📄 index.html or error.html is served  


## 🎯 Project Completion Status
- Static website deployed successfully  
- Public access configured securely  
- Error handling validated  
- Ready for portfolio and resume use




