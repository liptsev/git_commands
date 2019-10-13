# BASH  
dir  
cd {dirname} (/ ..)  
mkdir {dirname}  
touch {filename}  
echo ' ' > {filename}  
cat {filename}  
rm {filename}  
mv {filename} {newpath}  
chmod ??? {filename}  
chown ?????? {filename}  
  
# GIT BASIC  
git config --global user.name  
git config --global user.email  
git init  
git log  
git status  
git add {filename}  
git add .  
git commit  
git commit -m ' '  
gitk  
git clean -n  
git clean -fdx  
git clone {http_link}  
git remote add origin {http_link}  
git remote -v  
git push  
git push -f  
git fetch  
git rm  
git mv  
  
# GIT RESET  
head||index||filesystem  
git reset --soft {hash}  
git reset {hash}  
git reset --hard {hash}  
git reset {filename}  
git reset {hash} {filename}  

# GIT CHECKOUT  
git checkout {hash}  
git checkout master  
git checkout -b {new_branch_name}  
git branch  
git tag  
git tag {tag_name}  
git tag -d {tag_name}  
git checkout {tag_name}  
git checkout {filename}  

git revert head/{hash}  
git commit --amend  