# Portfolio Collection

A centralized repository aggregating portfolio projects and profile of koniz-dev, managed through Git submodules.

## 📦 Submodules

This repository contains the following submodules:

### 1. [koniz-dev](https://github.com/koniz-dev/koniz-dev)
GitHub profile README with information about skills, technologies, and contact details.

### 2. [koniz-portfolio](https://github.com/koniz-dev/koniz-portfolio)
Personal portfolio website with responsive design, dark/light theme, and project showcase.
- 🌐 Live: [https://koniz-dev.github.io/koniz-portfolio](https://koniz-dev.github.io/koniz-portfolio)

### 3. [rpm-blender-sketchfab](https://github.com/koniz-dev/rpm-blender-sketchfab)
Project about Blender and Sketchfab integration.

## 🚀 Getting Started

### Clone Repository

When cloning this repository, submodules will be empty. To clone with submodules:

```bash
git clone --recursive https://github.com/koniz-dev/portfolio.git
```

Or if you've already cloned, initialize submodules:

```bash
git submodule update --init --recursive
```

### Updating Submodules

Check if submodules have changes:

```bash
# Check status of all submodules
git submodule status

# Check if each submodule has new commits
# (Uses origin/HEAD - automatically points to default branch)
git submodule foreach 'git fetch && git log HEAD..origin/HEAD --oneline 2>/dev/null || echo "No changes"'

# Or manually check each submodule (specify branch):
cd <submodule-name>
git fetch
git log HEAD..origin/main --oneline   # if branch is main
# or
git log HEAD..origin/master --oneline # if branch is master
cd ..
```

Update all submodules to the latest commit:

```bash
# Update all submodules to latest commit from remote
git submodule update --remote

# Then commit changes in main repository
git add .
git commit -m "Update submodules"
git push
```

Update a specific submodule:

```bash
cd koniz-dev
git pull origin main
cd ..
git add koniz-dev
git commit -m "Update koniz-dev submodule"
```

### Adding a New Submodule

```bash
git submodule add <repository-url> <path>
```

### Removing a Submodule

```bash
# Remove entry from .gitmodules
git submodule deinit -f <path>
git rm -f <path>
rm -rf .git/modules/<path>
```

## 📝 Useful Git Submodule Commands

```bash
# View changes in submodule
git submodule status

# Update submodule to specific commit (not latest)
git submodule update

# Update and merge with remote
git submodule update --remote --merge

# Enter submodule directory and work as normal repo
cd <submodule-name>
git checkout -b feature-branch
# ... work ...
git push origin feature-branch
```

## 🛠️ Project Structure

```
portfolio/
├── .gitmodules              # Submodule configuration
├── koniz-dev/               # GitHub profile README
├── koniz-portfolio/         # Portfolio website
├── rpm-blender-sketchfab/   # Blender/Sketchfab project
└── README.md                # This file
```

## 📄 License

Submodules may have their own licenses. Please check each repository for details.

## 👨‍💻 Author

**koniz-dev**

- 🌐 Website: [https://koniz-dev.github.io/koniz-portfolio](https://koniz-dev.github.io/koniz-portfolio)
- 📧 Email: kietna.work@gmail.com
- 💼 LinkedIn: [koniz-dev](https://linkedin.com/in/koniz-dev)
- 🐙 GitHub: [@koniz-dev](https://github.com/koniz-dev)

---

_Built with ❤️ by koniz-dev_
