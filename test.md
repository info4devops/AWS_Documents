# 🏗 **Steps to Create an AWS Account**

## 📌 **Step 1: Provide Root User Email and Account Name**
1. Visit the [AWS Console](https://aws.amazon.com/console).
2. Enter your **root user email** (this will be the primary login for your AWS account).
3. Provide an **account name** (e.g., `My AWS Account`, `Prod`, `Dev`, `Training`).
4. **Verify your email**:
   - AWS will send a **verification code** to your email.
   - Enter the code to verify your account.
5. Set a **strong password** to secure access.

---

## 📌 **Step 2: Provide Contact Information**
1. Choose your **account type**:
   - 🔹 **Business** (for organizations, recommended)
   - 🔹 **Personal** (for individual use or learning)
2. Enter your **contact details**:
   - Full Name
   - Phone Number
   - Address
   - Country/Region

---

## 💳 **Step 3: Enter Billing Information**
1. Provide a valid **credit/debit card** for payment verification.
2. Ensure **billing details match** the account information to prevent suspension.
3. AWS will deduct a **small amount** (e.g., **₹2 INR** or **$1 USD**) for verification, which will be refunded.

🔹 **Tips:**
- Use the same name as in Step 2 and your payment details.
- Enable **International Transactions** on your card.

---

## ✅ **Step 4: Confirm Identity**
1. Select your **country** for identity confirmation.
2. Upload a **government-issued ID** for verification:
   - PAN card, Voter ID, Driver’s License, or Passport (varies by country).
3. Follow on-screen instructions to complete this step.

---

## 📲 **Step 5: Confirm Phone Identity**
1. Provide a **valid phone number** for verification.
2. Choose a verification method:
   - 🔹 **Text Message (SMS)**
   - 🔹 **Phone Call** (AWS will call with a verification code).
3. Enter the **verification code** to confirm your phone number.

---

## 💡 **Step 6: Choose a Support Plan**
1. Select a support plan based on your needs:
   - 🆓 **Basic Support Plan** (Free, best for learners and personal use)
   - 💻 **Developer Plan** ($29/month, email support within 12-24 hours)
   - 🏢 **Business Plan** ($100/month, 24/7 support via phone, chat, email)
   - 🏆 **Enterprise Plans** ($5,500+ per month, priority support, TAM access)

🔹 **Tip:** Start with the **Basic Support Plan** to avoid extra costs.

---

## 🚀 **Step 7: Log In to the AWS Management Console**
1. Once your account is created, AWS will send a **confirmation email**.
2. Go to the [AWS Console](https://aws.amazon.com/console).
3. **Log in** using your **root user email** and password.

---

# 🔑 **Understanding AWS Root User & IAM Users**

## 👤 **Root User**
- The **Root User** is the **account owner** with **unrestricted access**.
- Critical actions **only the root user can perform**:
  - Change support plans
  - Modify billing/payment methods
  - Close the AWS account
  - Transfer account ownership

🔹 **Security Tip:** Enable **MFA (Multi-Factor Authentication)** to protect the root account.

### ❓ **Why Only One Root User?**
- AWS accounts are tied to **a single email ID**, making the root user unique.

### ⚠ **Should Root Credentials Be Shared?**
❌ **No.** Sharing root credentials can compromise the entire AWS account.
✔ Instead, create **IAM users** with specific permissions.

---

## 🔐 **IAM Users (Identity and Access Management)**
AWS **IAM (Identity & Access Management)** allows you to create users and groups with **customized permissions**.

### **IAM Key Concepts:**
- 👤 **IAM Users** – Individuals needing AWS access.
- 👥 **Groups** – Logical grouping of users for easier permission management.
- 📜 **Policies** – JSON-based documents defining access rules.

🔹 **Why Create IAM Users?**
- IAM Users prevent sharing **root credentials**.
- Example: Assign a **ReadOnlyAccess** policy to an intern monitoring resources.

---

# 🎯 **Roles & Permissions for IAM Users**

| **Role**              | **Responsibilities**                                        | **Example Policy**         |
|----------------------|--------------------------------------------------|----------------------------|
| 🏗 **AWS Administrator** | Manages AWS resources like EC2, VPC, and databases. | `AdministratorAccess` |
| 👨‍💻 **Developer** | Limited access to specific development resources. | Custom policies |
| 📊 **DBA** | Manages AWS databases and backups. | `DBAdminAccess` |
| 🛠 **Support Team** | Monitors resources and reports issues. | `ReadOnlyAccess` |

---

# 🛡 **IAM Policies: Managed vs Inline Policies**

### 🗂 **AWS-Managed Policies**
✅ Predefined by AWS for common use cases.
✅ Examples:
- `AmazonS3FullAccess`
- `AdministratorAccess`
❌ Cannot be modified or deleted.

### 📜 **Customer-Managed Policies**
✅ Created by account admins for **custom needs**.
✅ More flexible than AWS-managed policies.

### 📌 **Inline Policies**
✅ Embedded **directly into a single** IAM user, group, or role.
❌ Not reusable across multiple users.

🔹 **Best Practice:** Prefer **Managed Policies** for easier scalability & maintenance.

---

# 📌 **Amazon Resource Name (ARN)**
Each AWS resource has a **unique ARN**.

**Format:**
```
arn:partition:service:region:account-id:resource-type/resource-id
```

**Examples:**
- IAM user: `arn:aws:iam::123456789012:user/JohnDoe`
- S3 bucket: `arn:aws:s3:::example-bucket`

📌 **Use Cases:**
- Defining access permissions in IAM policies.
- Tracking AWS resources in logs and audits.

---

# 📊 **Tracking IAM User Activities**
### 📝 **Using AWS CloudTrail**
CloudTrail logs **all API calls** and IAM activities.

✅ **Tracks:**
- **Who** made changes
- **What** actions were taken
- **When & Where** it happened

✅ **Best Practice:**
- Store logs in **Amazon S3** for long-term retention.
- Use **CloudWatch** to monitor IAM changes in real time.

---

## 🔎 **How to Track User Last Login & MFA Status**
### 📥 **Download IAM Credentials Report**
1. Open **IAM Dashboard** → **Security Credentials**.
2. Click **Download Credentials Report**.
3. The report provides:
   - Last login timestamps
   - MFA status
   - Access key status

---

# 🚀 **Conclusion**
✅ Setting up an AWS account properly ensures **security & efficient access control**.
✅ Use **IAM users** instead of **Root User** for daily operations.
✅ Enable **MFA** & follow **least privilege principle** for security.

💡 Need more AWS guidance? Keep learning and practicing! 🎯

