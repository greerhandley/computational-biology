# computational-biology
Hey! I am Greer Handley, and this is my hub for all of my classwork throughout my Computational Biology course at LA Tech.
All of the code below was created following step-by-step instructions as a way to become familiar with Python and its applications.

# create a new directory, and initialize it with git-specific functions
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
touch README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "add README to initial commit"

# provide the path for the repository you created on github
git remote add origin https://github.com/greerhandley/computational-biology.git

# push changes to github
git push --set-upstream origin main
