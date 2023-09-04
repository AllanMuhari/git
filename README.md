# create a new feature branch
git checkout -b feature/add-login-form develop

# make some changes and commit them
git add .
git commit -m "Add login form"

# merge the feature branch back into develop
git checkout develop
git merge --no-ff feature/add-login-form

# create a new release branch
git checkout -b release/1.0.0 develop

# test the release branch and fix any issues
# ...

# merge the release branch back into develop and master
git checkout develop
git merge --no-ff release/1.0.0
git checkout master
git merge --no-ff release/1.0.0

# tag the master branch with the release version number
git tag -a 1.0.0 -m "Release 1.0.0"


