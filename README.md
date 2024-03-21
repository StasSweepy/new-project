# What is it?
It's a step-by-step instructions how to setup github repository connectivity and then how to use additional branches to non-affect main branch.

## Instructions

1. Link to your Github profile.
2. Switch to repositories page and create new as a public repository.
3. Create SSH key to setup connectivity between remote and local development. Use [official documentation](https://docs.github.com/ru/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for that.
4. Clone your repository via SSH.
5. Create `README.md` and paste some initial text to it.
6. Track, commit and push your changes to remote repository from `main` branch.
7. Create and switch to `development` branch.
8. Do any changes in `README.md` on `development` branch.
9. Track, commit and push your changes to remote repository from `development` branch.
10. Switch back to `main` and pull any remote changes if exists.
11. Merge `development` branch to `main` and push `main` to remote repository.


## Following commands
```
git clone YOUR_REPO_SSH_LINK       # clone repository
echo "Initial Text" > README.md    # create README.md file with a text
git add README.md                  # add to track README.md file
git commit -m "commit_message"     # commit your changes
git push origin main               # push your changes
git checkout -b development        # switch to development branch
nano README.md                     # you could to use any editors to edit file. In example, I use editor nano
git add README.md                  # add to track README.md file
git commit -m "commit_message"     # commit your changes
git push origin development        # push your changes from development branch
git checkout main                  # switch to main branch
git pull origin main               # pull main branch for any remote changes
git merge development              # merge development branch to main
git push origin main               # push your changes
```

`NOTE: always use 'git status' to review what happens with your local development.`
