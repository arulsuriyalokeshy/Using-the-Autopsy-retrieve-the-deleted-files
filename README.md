# File_Recovery-using-Autopsy

## Aim
The objective of this guide is to demonstrate how to:  
 - Create a **Virtual Hard Disk (VHD)**.  
 - Add images to the disk, delete them, and recover them using **Autopsy**.  
 - Understand the forensic recovery process for deleted files.  
 - Learn how to remove the virtual disk after completing the experiment.

## Virtual Disk Creation & File Recovery using Autopsy 


## Step 1: 
   Create a Virtual Hard Disk (VHD) 

### **1. Open Disk Management**  
- Press **Windows + X** → Click **Disk Management** 

 ![1](https://github.com/user-attachments/assets/64c24930-f09d-48ad-a015-7035723d2228)


### **2. Create a New VHD**  
- Click **Action** (top menu) → **Create VHD**.
![2](https://github.com/user-attachments/assets/9597a859-2cbc-4de7-b833-b373179a7818)

![3](https://github.com/user-attachments/assets/9d109647-346d-4377-be2f-109561389e97)



### **3. Choose File Location & Size**  
- Click **Browse** and select where to save the VHD file (e.g, `C:\new VHD.vhd`)
- Set the **size** (e.g: `1GB`) 
- Choose **VHD (Fixed Size)** and Click **OK**

![3 5](https://github.com/user-attachments/assets/a20c0527-2dc4-4a1f-9aa3-2a469a7bb636)


### **4. Initialize the Disk**  
- In **Disk Management**, find your new disk (marked as "Not Initialized").  
![4](https://github.com/user-attachments/assets/60c00c26-78d1-449d-8cf4-f2e95e9292b6)


- Right-click the disk → Click **Initialize Disk**.

- Select **MBR (Master Boot Record)**. 
![4 5](https://github.com/user-attachments/assets/8ee67e9f-4062-4ff4-8a28-ae5965239037)



### **6. Create & Format the Partition**  
- Right-click the **Unallocated Space** → Click **New Simple Volume**.  
![4](https://github.com/user-attachments/assets/0d9e1514-c433-46b7-9fed-71837c26f5c9)

![5](https://github.com/user-attachments/assets/31bc78ed-212a-478d-b621-0ddbf348901c)

![6](https://github.com/user-attachments/assets/e1d08e10-0f01-485c-a01b-5e22a4242618)


- Click **Next** → **Click on Mount in the following empty NTFS folder** → **Browse** → **Assign a drive letter (e.g., `C: or D:`)** → **New folder** → **OK**

![7](https://github.com/user-attachments/assets/84c018c8-816a-46ce-9bf1-af5bd1d42e09)

![8](https://github.com/user-attachments/assets/6cca486f-b66f-4861-817d-0bb9b2f28ea5)

- Click **next** → **Finish**. 

---

## **Step 2: Add & Delete Files for Recovery** 

### **1. Copy Files to the Virtual Disk**  
- Open **File Explorer** → Go to the new drive (`C: or D:`), where the folder created in the previous step
- Create a new folder (`TestFolder`) and copy **images or files** into it.  

### **2. Delete the Files**  
- Select any one or two images → Press **Delete**.  
- Empty the **Recycle Bin** to permanently delete them.  

---

## **Step 3: Recover Deleted Files Using Autopsy**  
### **1. Open Autopsy & Create a New Case** 

- Launch **Autopsy** and **Run as a administrator**  
- Click **Create New Case**.  

![9](https://github.com/user-attachments/assets/3510305a-77e9-4d8c-8990-d36c114a6fda)


- Enter a **Case Name** (e.g., `Autopsy1`).  
- Choose a **Case Folder** location.  
- Click **Next** → Click **Finish**.  
![10](https://github.com/user-attachments/assets/fba49193-9443-4901-afa1-28953ce0e58d)


### **2. Add the Virtual Disk as an Evidence Source**  
- Click **Add Data Source**  → **Select Host**
![11](https://github.com/user-attachments/assets/37ed2167-fbe0-4d87-8a60-e7cafa71cdf8)

- Select **Local Disk** → **next** 
![12](https://github.com/user-attachments/assets/c7e306b1-efaf-4ff1-bfa5-95d51440f130)


- Select Disk → **Choose the VHD drive (`Drive1`)**
![13](https://github.com/user-attachments/assets/3fbcb342-c33e-4df4-9a98-b146024af0ff)


- Click **Next** → Keep default settings → Click **Finish**.  
- Wait for Autopsy to process the disk.  

### **3. Recover Deleted Files**  
- Go to **File Views** (left panel).  
![14](https://github.com/user-attachments/assets/75bd9a64-c4da-416b-80ad-3dd07df1220e)


- Click **Deleted Files** → Find your deleted images.  
- Right-click an image → Click **Extract File**.  

![15](https://github.com/user-attachments/assets/41ca9b25-1588-466d-8d3b-7026f0848dac)


- Select a folder to see the recovered files (e.g., `C:\image_recovery`).  

**Your deleted images are now recovered!**  

---

## **Step 4: Delete the Virtual Disk (Optional Cleanup)** 

### **1. Detach the VHD**  
- Open **Disk Management** (`Win + X` → Disk Management).  
- Find the **virtual disk** (`C: or D:`).  
- Right-click the disk (not the partition) → Click **Detach VHD**.  

### **2. Delete the VHD File**  
- Open **File Explorer**.  
- Go to the location where you saved the `.vhd` file (e.g., `C:\new VHD.vhd`).  
- **Delete** the `.vhd` file.  
- Empty the **Recycle Bin**.  

**Your virtual disk is completely removed!**  
 

 

## Result :
 This guide covers creating a Virtual Hard Disk (VHD), adding, deleting, and recovering images using Autopsy, and safely deleting the virtual disk after the experiment.
