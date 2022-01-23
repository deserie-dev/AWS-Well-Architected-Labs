# AWS Well-Architected Labs

<details>
<summary><b>Operational Excellence</b></summary><p>

# Lab 1: Inventory and Patch Management

Goals:

- Automated deployment of infrastructure
- Dynamic management of resources
- Automated patch management

1. Create Administrator IAM User and Group

![](/images/admin-user.png)

2. Use CloudFormation to Deploy the Infrastructure

![](/images/stack1.png)

---

## Inventory Management Using Operations as Code

### Setting up Systems Manager

1. Create an Instance Profile for Systems Manager managed instances.

![](/images/ssm-role.png)

2. Apply this role to the instances you wish to manage with Systems Manager

![](/images/modify-role1.png)

3. In the Systems Manager console navigate to Fleet Manager and you will see your instances populate into the list as managed instances.

![](/images/fleet.png)

### Create a Second CloudFormation Stack

1. Create a second CloudFormation stack: OELabStack2. Specify the InstanceProfile using the ManagedInstancesRole and define the Workload Name as Prod

![](/images/stack2.png)

### Systems Manager: Inventory

1. Use Systems Manager Inventory to Track Your Instances

![](/images/inventory.png)

### Systems Manager: State Manager

1. Review Association Status

![](/images/state-manager.png)

---

# Patch Management

### Systems Manager: Patch Manager

1. Create a Patch Baseline

![](/images/patch-baseline.png)

---

# Lab 2: Dependency Monitoring

![](/images/versioning-1.png)

</p></details>

<details>
<summary><b>Security</b></summary><p>

## Using Amazon Cognito for serverless consumer apps

In this workshop, I demonstrated end-to-end authentication and authorization using Amazon Cognito, Amazon API Gateway, AWS Lambda, and IAM.

A single page React JS web app called Wild Rydes hosts the HTML, CSS, and JavaScript to render the front-end which then connects to a public serverless backend API built using Amazon API Gateway and AWS Lambda. Amazon Cognito provides user identity management and authentication functions to secure the backend API. DynamoDB provides a persistence layer where data is stored and retrieved via the API's Lambda function.

---

### Module 1: User flows

In this module, I create an Amazon Cognito User Pool and Identity Pool for the Wild Rydes application. The Cognito User Pool will store user profile information and provide sign-up and sign-in capabilities, with the Cognito Identity Pool providing the ability to assume an Identity and Access Management (IAM) role from within the application.

---

1. Create an Amazon Cognito User Pool

![](/images/user-pool.png)

---

2. Create a Cognito Identity Pool

![](/images/identity-pool.png)

---

3. Integrate the application with Amazon Cognito

Configure the application to integrate to Amazon Cognito so it can store user profiles and enable sign-up and sign-in.

![](/images/amp-1.png)

---

![](/images/amp-2.png)

If the page then loads a map, sign-in was successful and you have successfully integrated Cognito for app authentication.

![](/images/auth-1.png)

---

Scroll down beyond the map to copy your user's identity token and decode it by pasting it into the 'encoded' input box at JWT.io . You will see all of your user's attributes are encoded within the token, along with other standard attributes such as the time the token was issued, the time the token expires, the user's unique ID, and more.

![](/images/jwt.png)

---

### Lambda Triggers

_Pre sign-up validation_
Use Lambda triggers to validate the email domain of the user to ensure it's a user from an approved domain prior to allowing them to sign-up.

![](/images/l-1.png)

---

Now that your Lambda function is configured, you can configure the trigger within your Cognito User Pool.

![](/images/l-2.png)

---

_Customize welcome message_
Now leverage the Custom Message trigger to customize the welcome message.

![](/images/l-3.png)

Now that your Lambda function is configured, you can configure the trigger within your Cognito User Pool.

![](/images/l-4.png)

---

</p></details>

<details>
<summary><b>Reliabilty</b></summary><p>

</p></details>

<details>
<summary><b>Performance Efficiency</b></summary><p>

</p></details>

<details>
<summary><b>Cost Optimization</b></summary><p>

</p></details>

<details>
<summary><b>Well-Architected Tool</b></summary><p>

</p></details>

<details>
<summary><b>Well-Architected Partners</b></summary><p>

</p></details>

---

**All pictured resources I created during my labs have been destroyed.**
