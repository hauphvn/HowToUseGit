1. Create a new folder with option name

2. Run: git init

3. Create a md file and set name as README: to show to everyone effect of project

4. Run: git add .

5. Config a account git:

git config --global user.email " your email "

git config --global user.name "your name"

6. git log : view commits

   git show: view contents was changed

   git diff: check change

7. checkout -- [name file]

Remove any change in old commit

8. git reset HEAD [name file]

   git reset [name file]

Remove file was add into working directory

Remove a miss commit

   git reset --soft [hash of commit which you want to come back]

come back to stating mode : mode had added

   git reset --mixed [hash of commit which you want to come back]

        come back to working mode : not yet add

   git reset --hard [hash of commit which you want to come back]

come back to working mode BUT it will DELETE all old that was old commit

9. branch

When we code a new function, we will create a new branch

We well join into master branch when we have finished that function

The way to create a new branch:

- git checkout -b [branch name]

To come back other branch:

- git checkout [name branch]

To delete a branch

- git branch -D [name branch]

10. merge

Adding changes from other branch to current branch

Example: Merge A branch with B branch

Step 1: You must stay branch A: git checkout A

Step 2: git merge B

11. revert: return previous status

- git revert [name commit]

Should not use it. DANGEROUS

12. Github

- Create repository

- git remote add origin [http....]

- the first push: git push -u origin master

13. Git credential

There are ways to do this, in this case I use SSH

1. Checking for existing SSH keys:

ls -al ~/.ssh

2. If there are no SSH keys

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

Enter file location if you do not want use default

Enter passphrese if you want to increase secure

3. Start the ssh-agent in the background:

$ eval "$(ssh-agent -s)"

4.Add your SSH private key to the ssh-agent, with id_rsa is option, you can change that name

$ ssh-add ~/.ssh/id_rsa

5.Adding a new SSH key to Github account:

Because I use Ubuntu so it will be displayed following:

- Get content public key id_rsa.pub in .ssh folder

- Go to Settings tab in your Github

- In the user setting sidebar, click SSH and GPG keys

- Click New SSH key or Add SSH key

- Enter your title

- Paste your key into the Key field

- Click Add SSH key

- If prompted, confirm your Github password

Finish !

14. Git clone/pull

- git clone [http...]

- git pull

15. Steps team work:

- git checkout -b [branch name]

- git push origin [branch]

- create a pull request on Github

- review code

online: on Github

offline: using git fetch

16. Git fetch

- git fetch origin [name branch which you want pull to review code]

17. Resolve conflict

- Using rebase

- Using merge
