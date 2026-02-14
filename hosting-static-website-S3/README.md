# 🌐 AWS Static Website Hosting using Amazon S3

## 📌 Project Overview
This project demonstrates how to host a static website using Amazon S3. 
The website files (HTML, CSS) were uploaded to an S3 bucket, 
and static website hosting was enabled to make the site publicly accessible.

---

## 🛠 AWS Services Used

- Amazon S3 – Storage and website hosting
- AWS IAM – User and access management

---

## 🏗 Architecture

User → Amazon S3 (Static Website Hosting Enabled)

---

## 🚀 Implementation Steps

1. Created an IAM Admin User
2. Logged in using IAM credentials
3. Created an S3 bucket
4. Disabled "Block Public Access"
5. Uploaded website files (index.html, style.css)
6. Enabled Static Website Hosting
7. Added bucket policy for public read access
8. Accessed website using S3 endpoint URL

---

## 📸 Screenshots

### 1️⃣ S3 Bucket Created
<img width="1855" height="795" alt="1  bucket lists" src="https://github.com/user-attachments/assets/4020c31e-4fcc-42b2-a086-fb21595248b5" />


### 2️⃣ Static Website Hosting Enabled
<img width="1807" height="847" alt="3  Static website hosting enabled" src="https://github.com/user-attachments/assets/6ffc4a68-4130-4330-a30f-e7262575c925" />


### 3️⃣ Bucket Policy Added
<img width="1841" height="858" alt="2  bucket policy" src="https://github.com/user-attachments/assets/ecebbe22-4c8f-45f1-a9f7-3a6225d5704d" />


### 4️⃣ Website Working in Browser
<img width="1832" height="900" alt="website" src="https://github.com/user-attachments/assets/6a656ba6-fb91-4bdf-8f25-50da693e40fd" />


---

## 🔗 Live Website URL
https://first-static-website-hosting-bucket1.s3.ap-south-1.amazonaws.com/index.html


---

## 🧠 Key Learnings

- Understanding Amazon S3 bucket configuration
- Managing public access settings
- Writing S3 bucket policies
- Basics of IAM user management
- Hosting static websites in AWS Cloud

---

## 🔐 Security Note

This project was implemented using an IAM Admin user for learning purposes.
In production environments, least-privilege IAM policies should be followed.

---

## 👨‍💻 Author

Ashokkumar  
Aspiring AWS Cloud Engineer
