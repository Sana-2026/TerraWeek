
# 🌱 TerraWeek Day 1 — Introduction to IaC & Terraform Basics

## 📝 Tasks

### Task 1: Understand IaC & Terraform
Write short answers (in your blog/notes) to:
- What is **Infrastructure as Code**, and what problems does it solve compared to clicking around a cloud console?
- What is **Terraform**, and why is it so popular? (Hint: declarative, provider-agnostic, huge ecosystem.)
- **Terraform vs alternatives** — write one line each on how Terraform compares to **OpenTofu**, **Pulumi**, **CloudFormation**, and **Ansible**.

### Task 2: Install Terraform (latest version)
- Install **Terraform ≥ 1.15** using the [official install guide](https://developer.hashicorp.com/terraform/install).
- Verify your install and **paste the output** in your notes:

```bash
terraform version
terraform -help
```


<img width="910" height="548" alt="task2-b" src="https://github.com/user-attachments/assets/2c9eecc9-8ced-4a24-83d4-b457626cd9aa" />
<img width="674" height="162" alt="task1" src="https://github.com/user-attachments/assets/9a41eb71-665a-4404-b5a1-fbdc8b011e69" />


- Install the **HashiCorp Terraform** extension in VS Code for syntax highlighting and autocomplete.

<img width="1366" height="639" alt="task2" src="https://github.com/user-attachments/assets/61af69d0-c72b-4897-ae1e-9c5d5974c00a" />


### Task 3: Learn 6 Crucial Terraform Terminologies
Explain each of these **in your own words** with a one-line example:
1. **Provider** — a plugin that lets Terraform talk to a platform (AWS, Azure, Docker…).                                                                                       + A provider is a plugin that allows Terraform to communicate with a specific platform or service (like AWS, Azure, Docker, Kubernetes).                                  + A translator between Terraform and the cloud platform.
   
2. **Resource** — a piece of infrastructure you want to create (an EC2 instance, an S3 bucket…).
      + A resource is an infrastructure component that Terraform creates or manages.
      + The actual thing you want to build.
        
3. **State** — Terraform's record of what it manages (the `terraform.tfstate` file).
      + State is Terraform's record of the infrastructure it manages, stored in the terraform.tfstate file.
      + Terraform's memory of what already exists.
        
5. **Plan** — a preview of the changes Terraform will make.
      + A plan is a preview of the changes Terraform will make before applying them.
      + A "before you proceed" checklist.
        
7. **HCL** — HashiCorp Configuration Language, the syntax you write Terraform in.
      + HCL is the language used to write Terraform configuration files.
      + Terraform's instruction language.
      
9. **Module** — a reusable, packaged group of Terraform configuration.
      + A module is a reusable collection of Terraform configurations that performs a specific task.
      + A template or blueprint you can reuse.

### Task 4: Your First Terraform Config (no cloud account needed!)
Use the **starter code in [`./example`](./example)** — it uses the `local` and `random` providers, so it costs **nothing** and needs **no credentials**.

Run the **core Terraform workflow** and capture the output of each step:
```bash
cd example
terraform init      # download providers, initialize the working directory
terraform fmt       # format your code
terraform validate  # check for syntax errors
terraform plan      # preview what will be created
terraform apply     # create the resources (type: yes)
cat greeting.txt    # see the file Terraform generated
terraform destroy   # clean up (type: yes)
```



<img width="965" height="555" alt="task4-1" src="https://github.com/user-attachments/assets/4a4a73a4-5aa7-44cd-9166-0e6e2d2cd01c" />

<img width="1342" height="670" alt="task4-2" src="https://github.com/user-attachments/assets/8f4a9330-a8dc-4497-9cc6-3cf662170180" />

<img width="1358" height="666" alt="task4-3" src="https://github.com/user-attachments/assets/6b3f63f7-4861-40ce-b6ec-9a1713a1f9a1" />

<img width="1345" height="499" alt="task4-4" src="https://github.com/user-attachments/assets/51b55c85-775a-4ee1-a588-340a6edc1efa" />

<img width="1366" height="685" alt="task4-5" src="https://github.com/user-attachments/assets/acdc6c2f-59e0-4891-9035-9dfabc9a2191" />


---

## 🔁 The Core Terraform Workflow

```
  Write  ──▶  Init  ──▶  Plan  ──▶  Apply  ──▶  Destroy
  (.tf)     (init)     (preview)   (create)    (clean up)
```

---

## 🍫 Bonus (Brownie Points)
- Set up **tab completion** for the Terraform CLI: `terraform -install-autocomplete`.
- Try **[OpenTofu](https://opentofu.org/)** (the open-source fork) and note the differences.
- Explore the `.terraform.lock.hcl` lock file that gets created — what is it for?

---

