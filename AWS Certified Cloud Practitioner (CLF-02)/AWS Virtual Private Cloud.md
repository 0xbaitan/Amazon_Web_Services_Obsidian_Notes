## **Account Aliases vs. Account IDs**

- **Account Aliases**: You can create a human-friendly alias (e.g., `my-company-prod`) for your AWS account, which can be used instead of the long, numeric **account ID** when signing in to the AWS Management Console.
    
- **Common Mistake**: Believing aliases change the account ID itself—they only provide a more memorable login URL.
    
- **Best Practice**: Use aliases to reduce login errors and improve clarity for teams managing multiple accounts.
    

## **AWS Region Selector**

- **Purpose**: Allows you to choose the AWS Region in which you want to create or manage resources.
    
- **Billing Console**: Certain features, like the **Billing Dashboard**, are only available in the default region (typically **us-east-1**, N. Virginia).
    
- **Common Mistake**: Assuming all services and features are available in every region or that billing data is region-specific—it’s global, but the interface is region-locked.
    

## **Region-Agnostic Services**

- **Examples**: **Amazon S3**, **CloudFront**.
    
- **Explanation**: These services operate globally or have a global namespace, so you don’t need to select a region to use them.
    
- **Common Mistake**: Assuming all AWS services are region-specific; some, like IAM and Route 53, are also global.
    

## **Metered Billing**

- **Definition**: AWS charges based on actual usage (compute hours, storage, data transfer, etc.).
    
- **Risk**: Misconfigurations (e.g., accidentally leaving resources running) can lead to unexpectedly high bills.
    
- **Best Practice**: Regularly review usage and set up **billing alarms**.
    

## **Budgets and Billing Alerts**

- **First Two Budgets Free**: AWS Budgets allows you to create up to two free budgets per account; additional budgets incur charges.
    
- **Fine Print**: Free tier applies only to the first two budgets, and there may be costs for advanced features (e.g., notifications).
    
- **Billing Alerts**: Set via **My Billing Dashboard > Billing Preferences > Receive Free Tier Usage Alerts**.
    
- **Billing Alarms**: Can be set for usage or cost thresholds, and can trigger notifications via **SNS (Simple Notification Service)**.
    
- **Anomaly Detection**: AWS Budgets and Cost Explorer can detect and alert on unusual spending patterns.
    
- **Common Mistake**: Assuming billing alarms provide forecasting—they only alert on actual or forecasted spend, not predictive analytics.
    

## **Auto Scaling**

- **Purpose**: Automatically adjusts the number of EC2 instances or other resources based on demand.
    
- **Powerful but Risky**: Can scale up quickly, potentially increasing costs if not configured with limits.
    
- **Common Mistake**: Relying solely on budgets for cost control—auto scaling can outpace your budget if not monitored.
    

## **Multi-Factor Authentication (MFA)**

- **Security Best Practice**: Always enable MFA for the root user and privileged IAM users to protect against unauthorized access.
    
- **Common Mistake**: Not enabling MFA on the root account, leaving it vulnerable.
    

## **Innovation Waves & Business Concepts**

- **Kondratiev Waves**: Economic theory suggesting long-term cycles of innovation and technological change.
    
- **Burning Platform**: Describes a scenario where organizations must abandon legacy systems for new technology, often under pressure and uncertainty.
    

## **Computing Power Types**

| Type              | Description                                 | AWS Example            | Common Use Case              |
| ----------------- | ------------------------------------------- | ---------------------- | ---------------------------- |
| **General**       | Standard CPU-based compute                  | EC2, Lambda            | Web servers, apps, databases |
| **GPU Computing** | Accelerated computing for ML, AI, graphics  | EC2 P3, Inf1 instances | Deep learning, rendering     |
| **Quantum**       | Quantum processors for advanced computation | AWS Braket             | Research, cryptography       |

- **AWS Inferentia (Inf1)**: AWS’s custom chip for machine learning inference, similar to Google’s TPU.
    
- **AWS Braket**: Quantum computing service. Simulator usage is free; real hardware incurs charges.