# How to work with private github project

## 1.Install git program
[git Installation package download](https://git-scm.com/download/)

Download git under compatible operating system

1. The installation is as simple as the QQ program. Double-click the installation package, select the installation path, and select the appropriate configuration environment. Just go to the next step.

2. After the installation is successful, open the E drive and create a new folder. This folder is used to store the cloned github project. The name should be in English to avoid unknown errors.

3. Open the new folder, right click Git Bash Here, and the Git command window will pop up. Then you can perform the relevant git operation.


## 2.Apply for project members

1. Need to get the connection of github project warehouse

>Project link:
>https://github.com/xxxx

2. Then click the fork in the upper right corner to complete the project pull

3. The private project needs the consent of the project owner


## 3.Configure git to use GitHub environment

Git needs to control GitHub project through SSH secret key

1. SSH cloning project needs to configure SSH key, and SSH key needs to be configured on GitHub

2. SSH cloning must be the holder or manager of the item to be cloned, and the SSH key must be added first, otherwise it cannot be cloned.

3. SSH does not need to enter the user name when pushing. If the password is set when configuring SSH key, you need to enter the password. Otherwise, you do not need to enter the password for direct connection.

### 1.GitHub configuration local SSH key

**Set the key user and mailbox**

You need to run the command to configure the local user name and mailbox. This can be real or fake

>View Configuration 
>
>git config --list
>
>Configure key user name 
>
>git config --global user.name "docker"
>
>Configure key mailbox
>
>git config --global user.email  "xxx@yeah.net"


**GitHub SSH key configuration**

Check for SSH Key

>cd ~/.ssh 
>
>ls

See if there is an id_rsa and id_rsa.pub file, if it exists, indicates that there is already an SSH key. If not, create a new SSH key.

**Create a new SSH key**

>$ ssh-keygen -t rsa -C “content neirong”
>
>-t : Type of key
>
>-C : Comment used to identify the key
>
>-C Generally, everyone writes email

Then two files will be produced in the. ssh directory: id_rsa and id_rsa.pub

id_rsa File is a private key，id_rsa.pub Is a public key.

**Get SSH key public key content（id_rsa.pub）**

Open the id under the. ssh directory id_rsa.pub file, copy the contents, or directly execute the command to view

>cat ~/.ssh/id_rsa.pub

After executing the command, a large string of characters of the public key will appear, copy the characters, and then configure the key on GitHub

### 2.Configure the secret key on GitHub

**Copy SSH key to GitHub**

1. Log in to your own gitbub, and click the inverted triangle of the user's avatar in the upper right corner. Select settings

2. Click on the left "SSH and GPG keys"

3. Click on the right "New SSH key" Copy the copied public key file to the key input box

[Configure GitHub key](https://blog.csdn.net/qq_20663639/article/details/126284892)


**Verify whether the setting is successful**

Now verify the authentication and communication with GitHub using the private key

>ssh -T git@github.com


>The authenticity of host 'github.com (xx.xx.xx.xx)' can't be established.
>
>RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
>
>This key is not known by any other names
>
>Are you sure you want to continue connecting (yes/no/[fingerprint])? yes (Enter here yes)
>

>>(The following indicates successful communication)

>
>Hi xxx! You've successfully authenticated, but GitHub does not provide shell access.


## 4.Clone project

**git clone instructions GitHub clone project to local**


>git clone git@github.com:lida2003/SnapAirUnitTest.git

After cloning the project on GitHub to the local location, you can edit the local file

[Get SSH link address of GitHub project](https://blog.csdn.net/qq_20663639/article/details/126284892)