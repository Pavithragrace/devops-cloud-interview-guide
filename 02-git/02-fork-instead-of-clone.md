## Question  
Explain a scenario where you used `git fork` instead of `git clone`. Why was forking necessary?

## ✅ Answer  
I used `git fork` when I contributed to a DevOps project in my org on GitHub. Since I didn’t have write access to the original repository, I forked it into my GitHub account, made changes, and then created a pull request from my fork to the upstream repo.

### 📘 Detailed Explanation  
In one of my previous projects at Wipro, we were managing AWS infrastructure using Terraform. We maintained reusable Terraform modules for resources such as EC2, VPC, ALB, Auto Scaling Groups, and S3.
For example, suppose I needed to update an existing Terraform module to add new tags and modify security group configurations.
The main Terraform repository was maintained by another team, and I didn't have direct write access.
So, instead of working directly in the original repository, I created a fork under my GitHub account.
I cloned my fork to my local machine, created a feature branch, made the required Terraform changes, and validated them using terraform fmt and terraform validate.
After testing, I pushed my changes to my fork and raised a pull request to the original repository.
The repository maintainers reviewed my changes and could merge them after approval.
Forking allowed me to contribute without needing direct write access to the original repository."

From there:
1. I cloned **my fork** to my local system:
   ```bash
   git clone https://github.com/my-username/aws-terraform-modules.git
   ```
2. Created a new feature branch feature/update-terraform-tags, made the fix, committed the changes.
3. Pushed the branch to **my fork**:
   ```bash
   git push -u origin feature/update-terraform-tags
   ```
4. Finally, I submitted a **pull request** to the original repository.

Using `git clone` directly on the upstream repo wouldn't have helped because I couldn’t push changes or open a PR without a fork. So, **forking gave me independence and write access on my own terms**, while still contributing back to the main project.

---
