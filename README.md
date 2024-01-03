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

**Change directory permissions**

As per the instructions for this project, only the user (researcher2 in this case) should be able to access the **drafts** directory. From the permissions screenshots, it is apparent that the group has Execute permissions, so these need to be removed. To accomplish this I used the following command:

```chmod g-x drafts```

![Screenshot of changing directory permissions](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Change%20directory%20permissions%20screenshot.png)

**Summary**

This project allowed me to apply the knowledge of changing permissions to files and directories that I gained through the preceeding videos and readings. I learned how to use different flags, symbols, and characters to add or remove permissions from three different types of users. After going through this project I am more confident in navigating the file system in Linux and more comfortable with working with file permissions.

### _Apply Filters to SQL Queries (Google Cybersecurity Professional Certification)_
For this project I ventured into the realm of SQL to use SQL filters to retrieve records from different datasets and investigate potential security issues as a security professional for a fictional organization. Here are the supplemental materials that were provided for this project:

- [Apply filters to SQL queries](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Apply%20filters%20to%20SQL%20queries.pdf)
- [Table formats](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Table%20formats.pdf)

**Project description**

For this project, I am going to use SQL operators like ```LIKE```, ```AND```, ```OR```, and ```NOT``` to query several database tables for information that may help investigate suspicious events and security issues that may be present on the organization's network/system. I will use SQL queries on the ```employees``` and ```log_in_attempts``` tables to retrieve these records.

**Retrieve after hours failed login attempts**

For this part of the project, I used a SQL query to find all failed login attempts that took place after 18:00. Here is the query that I used for that:

```SELECT *```

```FROM log_in_attempts```

```WHERE login_time > '18:00' AND success = 0;```

This query is to select all the possible entries **(*)** from the **log_in_attempts** table where the login took place after **(>)** 18:00 and it was a failed **(success = 0)** login attempt.

![Screenshot of a SQL query result to find failed after hours login attempts](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20after%20hours%20failed%20login%20attempts%20screenshot.png)

**Retrieve login attempts on specific dates**

The task for this part of the project was to investigate a suspicious event that happened on 2022-05-09. To complete this task I was asked to construct a SQL query that will identify login attempts that occurred on 2022-05-09 or 2022-05-08. Here is the query that I used to get those results:

```SELECT *```

```FROM log_in_attempts```

```WHERE login_date BETWEEN '2022-05-08' AND '2022-05-09';```

![Screenshot getting all login attempts between two dates with BETWEEN](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20login%20attempts%20on%20specific%20dates%20BETWEEN.png)

Here I used the BETWEEN filter to find any login attempts that were made between two dates. The BETWEEN filter could also be replaced by OR to accomplish this task in another way.

```WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';```

![Screenshot getting all login attempts between two dates with OR](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20login%20attempts%20on%20specific%20dates%20OR.png)

In this alternative method, OR is used to include the two possible values that **login_date** can have to match the necessary filter. 


**Retrieve login attempts outside of Mexico**

Here I use several different operators to filter out login attempts made outside of Mexico. First, I use ```NOT``` before the country value so that anything that matches the value in the SQL query is not returned. Next, I use ```LIKE``` to search for a custom string to match. Finally, in the string value that is searched for I include ```%``` which matches any number of characters where it is placed. So, in this instance, the query will match with any records that match **MEX** and **MEXICO** and will _not_ include them when the query is returned. 

![Screenshot of query returning login attempts made outside of Mexico](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20login%20attempts%20outside%20of%20Mexico.png)

**Retrieve employees in Marketing**

For this portion of the project, I was tasked with finding records for all employees that are in the Marketing department which has all of it's offices in the East building. So, for this SQL query I needed to use the ```department``` column and the ```office``` column to filter the results properly from the ```employees``` table.

![Screenshot of SQL query to get Marketing employees](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20employees%20in%20Marketing.png)

**Retrieve employees in Finance or Sales**

This task takes a little bit of everything learned in this project so far to find records for employees that are either part of the 'Finance' department ```OR``` the 'Sales' department.

![Screenshot of SQL query to get Fincance and Sales employees](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20employees%20in%20Finance%20or%20Sales.png)

**Retrieve all employees not in IT**

The final task in this project uses the ```NOT``` operator to get records for **all** employees **except** those that are part of the IT department. 

![Screenshot of SQL query getting all employee records except IT](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Retrieve%20all%20employees%20not%20in%20IT.png)

**Summary**

By using several operators and conditions in my SQL queries I was able to investigate suspicious activity that is occuring on the organizations network and systems. For instance, I was able to use the ```>``` and the ```=``` operators to find failed login attempts that took place after working hours. I was also able to use ```NOT```, ```AND```, ```OR```, and ```LIKE``` to sift through hundreds of employee records to find exactly what I was looking for in a more streamlined process than going through each record individually.

### _Analyze a Vulnerable System for a Small Business (Google Cybersecurity Professional Certification)_
For this project I was tasked with performing a vulnerability assessment for an e-commerce company that uses a remote database server for their employees to query information from. The employees use this database server to get information for potential customers, but the database has been open to the public since the company launched three years prior. 

I was given a [template](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Vulnerability%20assessment%20report%20template.pdf) that explains the system hardware used for the remote database and the scope which provides the focus and boudaries of the vulnerability assessment. In conjunction with the template, a supplemental file that outlines the [NIST SP 800-30 Rev. 1](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/NIST%20SP%20800-30%20Rev.%201.pdf) publication is used to conduct the vulnerability assessment. 

For the vulnerability assessment, I was to provide a purpose statement, identify three threat sources for a risk assessment, provide the approach that I took for the vulnerability assessment, and a remediation strategy to improve the security of the system. [Here](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/Vulnerability%20assessment%20report%20-%20Ramiro%20Garces.pdf) is my vulnerability assessment - my responses are shown in **red**.

### _Document an Incident with an Incident Handler's Journal (Google Cybersecurity Professional Certification)_

For this project, I was presented with a scenario in which a U.S.-based healthcare clinic was the victim of a ransomware attack and I was asked to fill in an entry on a [Incident Handler's Journal](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/Incident%20handler's%20journal%20.pdf). 

Below is the information from the Incident Handler's Journal entry that I created from the template provided. 

---

Date: January 3, 2024

Entry: #1

Description
A small U.S. health care clinic experienced a security incident in the form of an organized group of unethical hackers installing ransomware on the clinic’s system. The hackers were able to perform this attack by successfully using a phishing email which contained a malicious attachment. Once the malicious attachment was downloaded, ransomware was deployed which encrypted the organization’s computer files and data.

Tool(s) used
Logs
Possibly a SIEM

The 5 W's 

-Who caused the incident?

An organization of unethical hackers that target healthcare and transportation industries.

-What happened?

The hackers were able to install ransomware and encrypt a healthcare clinic’s data through the use of a phishing email which contained a malicious attachment.

-When did the incident occur?

On a Tuesday at approximately 9:00am (according to the project description)

-Where did the incident happen?

This incident happened at the healthcare clinic that was attacked by the organization of hackers.

-Why did the incident happen?

The incident was made possible because someone who works at the clinic downloaded a malicious attachment from a phishing email which allowed ransomware to be installed on the system.

Additional notes

The clinic may need to conduct better training for their employees, particularly in the area of identifying possible phishing emails or email security/safety.

---


## Certifications
![Image of the CompTIA Network+ certification badge](https://github.com/ramgarces/CybersecurityPortfolio/blob/main/images/NetworkPlus%20Logo%20Certified%20CE.png)

Code: KRNM28XTKMV4QZKB

Verify at: http://verify.CompTIA.org
