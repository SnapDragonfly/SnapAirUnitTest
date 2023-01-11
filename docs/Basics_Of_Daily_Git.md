
# Basics of Daily Git Operation

## 1.git clone

When using this command, you need to complete the key configuration between the local user and github.

Instruction usage:

>git clone git@github.com:lida2003/SnapAirUnitTest.git

When this command is used, a copy of the project file of the github project will be copied locally, which can be edited locally.

## 2.git pull

Synchronize remote warehouse code to local

Before git add/git commit code, first git pull needs to pull the code from the server to avoid overwriting others' code; If there is a conflict, first back up your own code, the latest code in the remote database under git checkout, merge your own code, and then submit your code

Instruction usage：

>git pull

The appearance of "Already up-to-date" means that the local code has been updated to be consistent with the remote warehouse.


## 3.git status

View current status

Instruction usage：

>git status

When you forget which files you have modified, you can use git status to view the current status. The red font shows the files you have modified.

## 4.git log

View all submission records

Instruction usage：

>git log

View the latest submission record

Instruction usage:

>git log -n 1

## 6.git add

Submit the code to the local git cache and wait for the upload comment.

Instruction usage:

>git add Basics_Of_Daily_Git.md


## 7.git commit

Make comments on this submission, which will be displayed on the github submission record.

Instruction usage:

>git commit -m “Comments on submitted documents” 
>
>git commit -m "[#16] Tello Function List for mobile APP, about 20% done"

### Git annotation naming convention

- Step 1: Find issue number from issue tab
- Step 2: Add "[#16]" to the head of comment
- Step 3: Use simple brief desciption of submission

*Note: see below for example.*

>[#16] Tello Function List for mobile APP, about 20% done

