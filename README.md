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
