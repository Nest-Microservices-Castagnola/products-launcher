### Steps to Create Git Submodules

1. **Create a new repository on GitHub**
2. **Clone the repository to your local machine**
3. **Add the submodule**
   - Replace `<repository_url>` with the URL of the submodule repository.
   - Replace `<directory_name>` with the folder name where you want to store the submodule (this folder should not already exist in the project).

```bash
git submodule add <repository_url> <directory_name>
```

4. **Add and commit the changes to the main repository:**

Example:

```bash
git add .
git commit -m "Add submodule"
git push
```

5. **Initialize and update submodules:**  
   When someone clones the repository for the first time, they should run the following command to initialize and update the submodules:

```bash
git submodule update --init --recursive
```

6. **To update submodule references:**

```bash
git submodule update --remote
```

---

## ⚠️ **Important**

When working with a repository that contains submodules:

1. **First, update and push changes to the submodule.**
2. **Then, update and push changes to the main repository.**

🔑 **Why?**  
If you push to the main repository before updating the submodule, the references to the submodules in the main repository will be lost, potentially causing conflicts.
