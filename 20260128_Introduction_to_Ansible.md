# Day 01, 28.01.2026

## `<span style="color:Blue">` __Infrastructure as Code: Ansible__ 

## __Schedule__

[spanstyle=&#34;color:black&#34;](spanstyle=%22color:black%22)

|Time|Content|

|---|---|

|09:00 - 10:00|Introduction|

|10:00 - 11:30|First theoretical inputs|

|11:30 - 13:00|Other theoretical inputs|

|13:00 - 14:00|Lunch Break|

|14:00 - 15:00|Practical exercises|

|15:00 - 18:00|Exercises and Ending|

---

## `<span style="color:black">` __Introduction into Ansible__ 

* [spanstyle=&#34;color:green&#34;](spanstyle=%22color:green%22) Configuration Management :

  * Keep servers, containers, and network gear in a desired state (packages, users, permissions, services).
* [spanstyle=&#34;color:green&#34;](spanstyle=%22color:green%22) Application Deployment:

  * Push application code or artifacts to multiple environments with repeatability and zero-downtime techniques.
* [spanstyle=&#34;color:green&#34;](spanstyle=%22color:green%22) Orchestration :

  * Coordinate multi-tier roll-outs (e.g., update DB, then web, then cache) or cloud resource lifecycles.

---

## `<span style="color:black">` __Key Concepts__ 

[spanstyle=&#34;color:black&#34;](spanstyle=%22color:black%22)

**Inventory**: A static file (INI or YAML) or dynamic script that lists hosts and host-groups Ansible manages.

**Module**: A self-contained script executed on the remote host (package install, file copy, service restart, etc.).

**Playbook**: A YAML file containing one or more plays; each play targets specific hosts & runs tasks built from modules.

**Role**: A standardized folder layout—tasks/, handlers/, templates/, etc.—that packages reusable automation logic.

**Ad-hoc Command**: A one-liner for quick tasks such as ansible web -m ping (no playbook needed).

</span>

---

## `<span style="color:black">` __Installing Ansible__ 

[spanstyle=&#34;color:red&#34;](spanstyle=%22color:red%22)

* Please visit the **Introduction to Ansible lesson**, where you will find these topics.

  * Installing Ansible
  * Project Setup with VS Code
  * Commands & Playbook

</span>

---

[spanstyle=&#34;color:black&#34;](spanstyle=%22color:black%22)

## `<span style="color:black">` __Build a YAML File__ 

```yaml

# Example: user profile data


user:

name: John Doe

age: 30

email: john.doe@example.com

active: true


skills:

    - Python

    - AWS

    - Docker

    - Terraform


address:

street: 123 Main Street

city: Berlin

zip: 10115

```

**Save and validate**

``yamllint employee_records.yml                          ``

<span style="color:grey">

---

## `<span style="color:black">` __What is an Ansible Inventory?__ 

* `<span style="color:black">` An inventory is a collection of hosts (managed machines) that Ansible can reach. Think of it as the phone book Ansible consults to know where to execute each task.

  **Host**: One machine managed by Ansible (identified by IP, hostname, or alias).

  **Group:** A collection of hosts that share something in common (e.g. web, db).

  **Implicit Groups**: Automatic groups:

  * all = every host

  * ungrouped = hosts not in any group

  **Inventory Source:** Where Ansible gets the list of hosts (file, cloud plugin, script, etc.).

  **ansible.cfg:** Configuration file that tells Ansible which inventory and settings to use.

  **host_vars/:** Folder for variables that apply to one specific host.

  **group_vars/:** Folder for variables that apply to all hosts in a group.

## `<span style="color:black">` Define the Inventory (hosts)

```[web_servers]

server1.ironhack.com ansible_user=root  ansible_password='Pass@123'

server2.ironhack.com ansible_user=admin ansible_password='Pass@123'

server3.ironhack.com ansible_user=root  ansible_password=pass


[db_servers]

db1.ironhack.com ansible_user=admin ansible_password='Pass@123'


[all_servers:children]

web_servers

db_servers


[local]

localhost ansible_connection=local

```

[spanstyle=&#34;color:green&#34;](spanstyle=%22color:green%22) For more details, check the Ironhack lesson **Create Ansible Inventory File.**

---

## `<span style="color:black">` __Links__ 

* [spanstyle=&#34;color:green&#34;](spanstyle=%22color:green%22) You can find this content in the Ironhack platform under Module 4, Week 3 of the DevOps bootcamp.

[Ironhack](https://my.ironhack.com/cohorts/6853f14924f1b7002b81f7c5/lms/courses/github:course:ironhack-edu:devops-bootcamp:cohort-B2C-DVFT-20260112-RMT-EN/modules/module_4_week-3)
