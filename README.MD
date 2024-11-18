# initial feature release

git init
touch feature.txt
git add . && git commit -m "feat: initial commit"
echo "complete task 1" >> feature.txt
git add . && git commit -m "feat: complete task 1"
echo "complete task 2" >> feature.txt
git add . && git commit -m "feat: complete task 2"

# Your initial progress on feature2

git checkout -b feature2
touch feature2.txt
git add . && git commit -m "feat: start work on feature2"
echo "complete feature2 task 1" >> feature2.txt
git add . && git commit -m "feat: complete feature2 task 1"
echo "complete feature2 task 2" >> feature2.txt
git add . && git commit -m "feat: complete feature2 task 2"

# Your team member fixing a bug

git switch master
git checkout -b fix-feature
echo "fix feature bug 1" >> feature.txt
git add . && git commit -m "fix: fix feature bug 1"
echo "fix feature bug 2" >> feature.txt
git add . && git commit -m "fix: fix feature bug 2"
git switch master
git merge fix-feature

<!-- this is the commit history while using rebase -->

# 7be2edd (HEAD -> feature2) feat: complete feature2 task 2

# 382247e feat: complete feature2 task 1

# 559c9bd feat: start work on feature2

# 6db40d1 (master, fix-feature) fix: fix feature bug 2

# e2f5b13 fix: fix feature bug 1

# fb3febc feat: complete task 2

# 047ed57 feat: complete task 1

# cd12408 feat: initial commit
