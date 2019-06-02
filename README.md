# Notes App
> A full-stack notes app project

### Git
Each component resides within it's own repo, merged through submodules in this main repo.

##### Config:
```bash
# Submodule status with git status
git config --local status.submoduleSummary true

# Automatically sync all on pull
git config --local submodule.recurse true
```

##### Useful commands:
```bash
# Clone recursively up to 8 in parallel (git v2.8<)
git clone --recurse-submodules -j8 git@github.com:Bajocode/notesapp-k8s-microservices-ios.git

# Add a submodule
git submodule add

# Checkout master all
git submodule foreach git checkout master

# Pull all
git pull --recursive-submodules

# Git alias
git config --local alias.spull '!git submodule foreach git checkout master && git pull --recurse-submodules && git submodule update --init --recursive --remote'
```
