# Cybersecurity Portfolio

As a dedicated IT professional with a passion for cybersecurity, I am eager to transition into the role of a Cybersecurity Analyst. The world of cybersecurity, with its evolving concepts and tools, captivates me, driving my daily commitment to acquiring new skills. My goal is to contribute effectively to any organization by implementing and upholding robust security standards. Strong communication skills complement my technical expertise, ensuring a seamless integration of cybersecurity measures in the ever-changing landscape of technology.

## Projects

### _Conducting an Internal Security Audit (Google Cybersecurity Professional Certification)_
For this first Portfolio Activity from the Google Cybersecurity Professional Certification course, I conducted an internal security audit for a ficitonal company. The activity provides you with supplemental materials that outline the different control categories to look for in one file, and another file that provides the details about the fictional company called Botium Toys. The file with details about Botium Toys goes into detail about what controls the company has in place, what controls the company may be lacking on, and some assets that the company keeps track of. The task to be performed in this activity is to use the provided Controls and Compliance Checklist file to identify what controls are in place, what controls are not in place, and whether or not the company is in-line with some common industry compliances and standards, indicated by checking a "yes" or "no" box. 

After checking the necessary boxes from referencing the supplimental material, there is an optional section where suggestions can be made about what controls or methods can be put into place to fix the issues that were found. I provided some of my own recommendations at the bottom of the page as you can see in the file below.

[Here](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Controls%20and%20Compliance%20Checklist%20-%20Ramiro%20Garces%20Jr.pdf) is the copy of my Controls and Compliance Checklist from the activity. 

### _Use the NIST Cybersecurity Framework to Respond to a Security Incident (Google Cybersecurity Professional Certification)_
This project allowed me to use the knowledge that I have gained about networks in the certification course so far to analyze a network incident that happened to a fictional company. Along with the network knowledge gained in the course, the NIST Cybersecurity Framework (CSF) is used to create an incident report for the organization to use for furture cybersecurity incidents. 

![Image of the NIST CSF 5 core functions](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/NIST%20CSF%205%20core%20functions.png)

After being presented with the cybersecurity incident scenario, I used the supplemental files provided by the course to go through each core function of the NIST CSF framework to help the company improve their cybersecurity posture for furture attacks/incidents. 

[Here](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Incident%20Report%20Analysis%20-%20Ramiro%20Garces%20Jr.pdf) is my Incident Report Analysis for the fictional company that experienced this attack.

### _Use Linux Commands to Manage File Permissions (Google Cybersecurity Professional Certification)_
This project goes over managing file permissions. Several supplemental files and a Linux Virtual Machine hosted by Google are used to complete this project. [Here](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Current%20file%20permissions.pdf) is a file that is provided to show the structure of the default file permissions before the activity is started. The [main document](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/File%20permissions%20in%20Linux.pdf), which is to be completed as you go through the activity, has been made the main part of this project section below instead of using the file itself.

**Project Description**

Linux commands will be used in a shell to change permissions for files, hidden files, and directories.

**Check file and directory details**

To check file permissions, the ```ls -l``` command should be used. However, since there are hidden files in this directory, adding the ```-a``` flag to the command can be used to display those files as well. Thus, the following command ```ls -la``` (the ```-l``` and ```-a``` flag combined) is used to display the permissions for all files in the __/home/researcher2/projects__ directory.

![Screenshot of file permissions](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Current%20file%20permissions%20screenshot.png)

**Describe the permissions string**

The permission string is the letters and hyphens that are on the left side of the example screenshot above. These letters and hyphens indicate if the entry is a file or directory and the permissions for that particular entry. I will explain the significance of the letters and hypens using the line below as an reference and example.

![Screenshot of a single line in the Linux command line showing permissions](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/directory%20permissions%20line.png)

The permissions string is a 10-character string with ten different "spots" to tell the user about the permissions for that particular file or directory. The first character, if it is a ```d``` indicates that entry is a directory. If the first character is a ```-``` (hyphen) then that entry is a file. For the rest of the characters, which are split up into three groups, the following letters are used:

- ```r``` = Read permissions, the user can read or view the file or directory

- ```w``` = Write permissions, the user can write or modify the file or directory

- ```x``` = Execute permissions, the user can execute an executable file or search a directory

- ```-``` = No permissions, the user does not have the permission where this character appears

Now, as mentioned before, the remaining nine characters are split up into three groups. The first group of three (characters 2-4) are permissions for the user who is set as the **User Owner**. The second group of three (characters 5-7) are permissions for any users in the group who is set as the **Group Owner**. The last group of three (characters 8-10) are for any user who is not in the first two categories or **Other**.

So, using the single line above as an example, the entry is a directory (```d``` in the first character), the User Owner has Read, Write, and Execute permissions (```rwx``` in characters 2-4), the Group Owner has only Execute permissions (```--x``` in characters 5-7), and Other users have no permissions (```---``` in characters 8-10). 

**Change file permissions**
For this step of the project, the following prompt is given:
>The organization does not allow other to have write access to any files. Based on the permissions established in Step 3, identify which file needs to have its permissions modified. Use a Linux command to modify these permissions.

To change the permissions of the file I used the ```chmod``` command to remove **write** permissions from Other users.

![Screenshot of the terminal changing permissions for the file](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Change%20permission%20screenshot%20outlines.png)

As is apparent from the screenshot above, I used the letter ```o``` (for Other user(s)), along with the ```-``` (minus) symbol to indicate that I want to **remove** ```w``` (write) permissions for the ___project_k.txt___ file.

**Change file permissions on a hidden file**
Here the project prompts that a hidden file in the directory should not have write permissions for anyone, but the user and group should be able to read the file. To accomplish this I used the following command to change permissions:

```chmod u-w,g-w,g+r .project_x.txt```

As you can see from the code snippet above, I use ```-``` to remove write permissions from the users that have them, and ```+``` to add read permission to the group. This command can be seen highlighted, in action, in the screenshot below.
![Screenshot of changing permissions for a hidden file](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Change%20hidden%20file%20permissions%20highlighted.png)

## Certifications
![Image of the CompTIA Network+ certification badge](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/NetworkPlus%20Logo%20Certified%20CE.png)

Code: KRNM28XTKMV4QZKB

Verify at: http://verify.CompTIA.org
