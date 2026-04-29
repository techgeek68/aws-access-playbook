# AWS Account Creation & Free Tier Guidance

This guide walks you through creating an AWS account via the AWS Management Console, covering Free Tier benefits and how to monitor your usage to avoid unexpected charges.

---

## Creating an AWS Account

**1. Navigate to the AWS Sign-Up Page**

- Go to [aws.amazon.com](https://aws.amazon.com).
- Click **Create an AWS Account** in the top right corner.

**2. Enter Account and Contact Information**

- **Root user email address:** Enter a valid email address (AWS will send a verification code to confirm it).
- **Account Name:** Choose a name for your AWS account.
- **Password:** Your password must be at least 8 characters and include a mix of uppercase, lowercase, numbers, and symbols; and cannot match your account name or email address.
- **Contact Information:** Select Personal or Business, then fill in your name (or company name), phone number, and address. For business accounts, it's best practice to use a company phone number rather than a personal one.

**3. Add Payment Details & Complete Identity Verification**

- **Payment Method:** Enter a valid credit or debit card. AWS may place a small temporary authorization charge (typically around $1 USD) to verify the card.
- **Identity Verification:** Select a contact method to receive a verification code, enter your phone number, and submit the code you receive.

**4. Choose the Free Basic Support Plan**

- AWS will prompt you to select a support plan.
- Choose **Basic Support; Free** to avoid any support charges.

**5. Log In to the AWS Management Console**

- Go to [console.aws.amazon.com](https://console.aws.amazon.com).
- Sign in with your registered email and password (root user).
- Explore the Console dashboard to begin using AWS services.

---

## How the AWS Free Tier Works

### Free Tier Types

**1. 12 Month Free Tier**

Available to new accounts, this tier provides free usage of select services for the first 12 months. Key limits include:

- **Amazon EC2:** 750 hours/month of t2.micro or t3.micro instances (Linux or Windows). You can run multiple instances, but their combined usage must not exceed 750 hours per month.
> **Note:** For accounts created on or after July 15, 2025, AWS changed the EC2 Free Tier. Instead of 12 months on t2.micro/t3.micro, these accounts receive 6 months of access with a broader set of instance types (t3.micro, t3.small, t4g.micro, t4g.small, c7i-flex.large, m7i-flex.large) backed by $200 in credits.
- **Amazon S3:** 5 GB of Standard storage, 20,000 GET requests, and 2,000 PUT/COPY/POST/LIST requests per month, plus 15 GB of data transfer out.
- **Amazon RDS:** 750 hours/month for db.t2.micro or db.t3.micro instances, plus 20 GB of General Purpose SSD (gp2) storage and backup storage up to 100% of your provisioned DB size. db.t4g.micro is also included for eligible database engines.

**2. Always Free**

Certain services remain free indefinitely, beyond the 12-month window:

- **AWS Lambda:** 1 million requests and 400,000 GB-seconds of compute time per month.
- **Amazon DynamoDB:** 25 GB of storage, 25 provisioned Write Capacity Units (WCU), and 25 provisioned Read Capacity Units (RCU); enough to handle approximately 200 million requests per month.

**3. Short Term Trials**

Some AWS services offer free trials for a limited period, typically ranging from a few days to several months, to help you evaluate them before committing.

---

### Free Tier Limits at a Glance

| Service   | Free Tier Limit (per month)                       | Duration    |
|-----------|---------------------------------------------------|-------------|
| EC2       | 750 hours of t2.micro/t3.micro (Linux or Windows) | 12 months\* |
| S3        | 5 GB storage, 20,000 GET, 2,000 PUT requests      | 12 months   |
| RDS       | 750 hours, 20 GB storage (db.t2/t3/t4g.micro)    | 12 months   |
| Lambda    | 1M requests, 400,000 GB-seconds                   | Always Free |
| DynamoDB  | 25 GB storage, 25 WCU, 25 RCU (~200M req/month)  | Always Free |

>*For accounts created on or after July 15, 2025, the EC2 Free Tier is 6 months, with different instance types and $200 in credits, not the standard 12-month t2/t3.micro offer.*

---

### Monitoring Free Tier Usage

- **Free Tier Dashboard:**
  Go to the [AWS Billing Console](https://console.aws.amazon.com/billing/home) and select **Free Tier** to view current usage and remaining allowances across all services.

- **Billing Alerts:**
  Set up proactive alerts using **AWS Budgets**. Create a budget (e.g., $1 threshold) and configure email or SNS notifications so you're alerted before you incur any charges.

---

### Recommendations

- Check the Free Tier dashboard regularly to stay on top of usage.
- Stop or terminate EC2 and RDS instances when not in use; running instances count against your monthly hours even if idle.
- Delete unused S3 objects and EBS snapshots to avoid storage charges.
- Be aware that t2.micro and t3.micro instances run in **Unlimited CPU credit mode by default**, which can result in small additional charges if sustained CPU usage exceeds the baseline.

---

## Resources

- [AWS Free Tier Details](https://aws.amazon.com/free)
- [AWS Free Tier Usage Dashboard](https://console.aws.amazon.com/billing/home#/freetier)
- [AWS Budgets Documentation](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/budgets-create.html)
- [Create an AWS Account (Official Guide)](https://aws.amazon.com/resources/create-account/)
- [AWS Account Creation & Free Tier (Video Guide)](https://www.youtube.com/watch?v=CecVvOVOtuQ)

---
