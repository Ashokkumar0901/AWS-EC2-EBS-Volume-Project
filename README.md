# AWS-EC2-EBS-Volume-Project
Hands-on AWS project demonstrating how to create, attach, format, and mount an EBS volume to an EC2 instance.

# AWS EC2 + EBS Volume Hands-on Project

This project demonstrates how to **create, attach, format, and mount an EBS volume** to an EC2 Linux instance.  
It teaches fundamental cloud concepts used in **Cloud Support, Cloud Operations, and DevOps** job roles.

---

## Project Overview

AWS EBS (Elastic Block Store) provides block-level storage volumes for EC2 instances.  
In this project I performed:

- Creating a new gp3 EBS volume  
- Attaching it to a running EC2 instance  
- Identifying the device using `lsblk`  
- Formatting the disk with EXT4  
- Mounting the volume to `/data`  
- Making it persistent using `/etc/fstab`  

---

## Architecture Diagram
+-------------+ +-------------------+
| AWS EC2 | ---> | EBS Volume |
| (Amazon Linux 2) | /dev/xvdf |
+-------------+ +-------------------+


---

## Technologies Used
- AWS EC2  
- AWS EBS (gp3)  
- Amazon Linux 2  
- SSH (EC2 Connect)  
- Linux filesystem commands  

---

## Steps Performed

### **1. Create EBS Volume**
- Open EC2 Console → Volumes → Create Volume  
- Volume type: `gp3`  
- Size: `5 GiB`  
- AZ: same as EC2 instance  

### **2. Attach Volume**
- Select volume → Actions → Attach  
- Device name: `/dev/sdf` (OS reads as `/dev/xvdf`)  

### **3. Connect to EC2**
ssh -i mykey.pem ec2-user@<public-ip>

### **4. Verify New Disk**
lsblk

### **5. Format the Disk**
sudo mkfs -t ext4 /dev/xvdf

### **6. Create Mount Directory**
sudo mkdir /data

### **7. Mount the Disk**
sudo mount /dev/xvdf /data

### **8. Verify**
df -h

### **9. Make Mount Persistent**
**Get UUID:**
sudo blkid /dev/xvdf


**Edit fstab:**
sudo nano /etc/fstab


**Add:**
UUID=<YOUR-UUID>   /data   ext4   defaults,nofail   0   2


