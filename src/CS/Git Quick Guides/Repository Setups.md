After creating the *repository* using `git init`, users must set up several global configurations for smoother workflows. While Git allows users to setup their workflows with hundreds of combinations, majority of them are irrelevant and exist merely for niche purposes. Below are the most important setups users must take note of when setting up their git repositories: 

# Local Git 

### Minimum
The user may first specify their preferred text editor: 
```powershell
git config --system core.editor editor_name
git config --global core.editor editor_name
git config --local core.editor editor_name
```
Next thing to ensure is that the user's chosen text editor is allowed to wait while a commit message is being written:
```powershell
git config --system core.editor "editor_name --wait" # applied to all users on system
git config --global core.editor "editor_name --wait" # applied to all repositories for the current user
git config --local core.editor "editor_name --wait" # applied to current repo only
```
There's sometimes an error that causes git to abort commits prematurely. Once that's been settled, the step is to set up the identity of the user: 
```powershell
git config --system user.name "name of dev" # applied to all users on system
git config --global user.name "name of dev" # applied to all repositories for the current user
git config --local user.name "name of dev" # applied to current repo only

git config --system user.email "user.email@example.com" # applied to all users on system
git config --global user.email "user.email@example.com" # applied to all repositories for the current user
git config --local user.email "user.email@example.com" # applied to current repo only
```


### Recommended
While the code above is what the user must do to get the setup running, the code below is recommended so as to greatly improve workflow: 
```powershell
git config --global init.defaultBranch master_branch_name # state main branch
```
The user may also dictate the behavior of *line endings*, which vary depending on the user's operating system: 
```powershell
git config --global core.autocrlf true # for Linux or Mac
git config --global core.autocrlf true # for Windows
```

Git configuration settings can be viewed using
```julia
git config --list # list all settings
git config --list --show-origin # show locations of where changes are stored
```
Specific settings may be viewed using lines like
```powershell
git config user.name
git config user.email
git config core.editor
```

### Advanced Configurations
More advanced configurations can be set up using the following: 
```powershell
git config --global color.ui # enable colorful output

# below are some examples of ways to set aliases (abreviations) for common commands:
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st

# configure pull behavior
git config --global pull.rebase true
```

---

# Remote Git
