# exams

The exams here have been graciously donated by members of MSESS. If you would like to donate an exam you have, please send an email to services@msess.ca with your exam or give it to an member of the MSESS exec team.

This website is intended for educational purposes only. MSESS does not claim to own any of these documents, they are the property of their respectful owners. If you feel any of the material should be taken down, please contact services@msess.ca and it will be taken down immediately.

## How to add an exam

On your local computer conduct the following steps: 
1. Create a folder for the course (named: MSE|ENSC|ECON ###) whose exams you wish to add
2. Create a folder inside the course folder named Final, Homework or Midterm
3. Copy the final/midterm/homework into the folder named Final/Midterm/Homework
4. Rename the final/midterm/homework file to: Summer|Fall|Spring-YEAR-ANYTHING_ELSE_YOU_WANT.pdf

On github conduct the following steps:
5. Fork this repository (MSESS/exams)

In your fork (YOUR_NAME/exams) conduct the following steps:

6. Click the `Upload files` button
7. Drag and drop the course folder (named: MSE|ENSC|ECON ### from step 1) into the drop area
8. Write a good commit message and press commit changes button
9. Send a pull request to the MSESS/exams repository

The folder structure and names (Caps, spacing, and info needed) are crucial. Please take a look at other exams that have already been uploaded to see how to capitalize and name files.


## For admins only

Updating msess.ca to automatically rebuild is automated using travis. See:

https://github.com/msess/exams/blob/master/common/travis/checkFileName.sh

https://github.com/msess/exams/blob/master/.travis.yml

99.9% of the time you wont have to do anything once you click the green merge button on the pull request in the github webgui. msess.ca's exam bank will automatically show the new exam after some time has passed. However, if you do not see a commit on the msess/msess.github.io repository after merging a pull request (and you have waited), you may have to start manually updating the exam bank. Here are the instructions on how to manually update msess.ca's exam bank to the current commit.

### Manual Updating

Once the new exam has been added to the MSESS/exams repository (the pull request has been accepted), you must tell the msess/msess.github.io (our website's repository) to regenerate and load the new exam.

1. `git clone https://github.com/msess/msess.github.io.git`
2. `cd msess.github.io`
3. `git submodule update --init --recursive`
4. `git submodule update --recursive --remote`
5. `git add exams`
6. `git commit -m "updated exam bank"`
7. `git push origin master`

remember to use `git status` often and google your errors.
