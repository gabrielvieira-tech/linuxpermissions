<p align="center">
  
![Linux Backgrounds Free Download](https://github.com/user-attachments/assets/c6748177-3c4a-4869-845d-336fe4f4957d)


<h1>File permissions in Linux</h1>
In this lab activity, I’ll use Linux commands to configure authorization.

Authorization is the concept of granting access to specific resources in a system. It's important because without authorization any user could access and modify all files belonging to other users or system files. This would certainly be a security risk.

In Linux, file and directory permissions are used to specify who has access to specific files and directories. I’ll explore file and directory permissions and change the ownership of a file and a directory to limit who can access them.

As a security analyst, setting appropriate access permissions is critical to protecting sensitive information and maintaining the overall security of a system.<br />

<h2>Environments and Technologies Used</h2>

- Qwiklabs

<h2>Operating Systems Used </h2>

- Linux Debian 12 x64 Gen2
  
<h2>List of Prerequisites</h2>

- Computer/laptop
- 4gb VRAM 
- Duo Core CPU
- Internet access


<h2> Check file and directory details</h2>

<img width="935" height="239" alt="1 2" src="https://github.com/user-attachments/assets/7365e204-627e-4a97-8b8b-3c170ae79838" />


<p>

First, navigate into the projects directory from the current working location by using the command "cd projects". Once inside, list out the contents of the directory along with their associated permissions by using the "ls -l" command. This allows you to review which files and subdirectories are present, as well as the specific read, write, and execute privileges assigned to each.
<br />

<h2> Describe the permissions string</h2>

<img width="935" height="180" alt="2" src="https://github.com/user-attachments/assets/1c6f4ff1-2340-4bde-b031-8092fcc3eb38" />


<p>

Each entry in a directory listing begins with a 10-character (respresented by the color orange) string that defines the file’s type and permissions. The very first character specifies the type of item "d" for a directory or "-" for a regular file. The next three characters represent the read(r), write(w), and execute(X) rights for the file’s owner. The following three characters specify the same permissions for the group associated with the file, and the final three characters indicate the permissions granted to all other users on the system. Whenever a hyphen (-) appears in place of a letter(r,w or x), it means that particular permission is not granted. Beyond the permissions string, the listing also shows the user who owns the file (respresented by the color yellow) and the group ownership (respresented by the color blue).
</p>
<br />

<h2> Change file permissions</h2>

<img width="932" height="372" alt="3 1" src="https://github.com/user-attachments/assets/a3014e31-2ba7-445d-a297-393aae8eb023" />

<p>

The first step is to check whether any files inside the projects directory grant write permissions to “others” (users outside of the file’s owner and group). Allowing such access could lead to unauthorized modifications and weaken system security. After reviewing the files, it was found that "project_k.txt" granted write access to others. To fix this, the "chmod o-w project_k.txt" command was used, which removes write permissions for “others” while keeping user and group settings intact.
</p>
<br />

<img width="932" height="367" alt="3 2" src="https://github.com/user-attachments/assets/8593177a-52f6-40c7-bdd7-b6a2e18ecbcc" />

<p>

Some files require stricter access rules. For example, "project_m.txt" is designated as a restricted file and should only be accessible by its owner. Neither the group nor others should have read or write permissions. Upon inspection, the group was found to still have read access. To correct this, the "chmod" command was applied again to remove those permissions, ensuring that only the user can read from or write to the file, thereby enforcing tighter security: command used was "chmod g-r project_m.txt"
</p>
<br />

<h2> TEXT </h2>

<img width="935" height="180" alt="2" src="https://github.com/user-attachments/assets/1c6f4ff1-2340-4bde-b031-8092fcc3eb38" />


<p>

Each entry in a directory listing begins with a 10-character (respresented by the color orange) string that defines the file’s type and permissions. The very first character specifies the type of item "d" for a directory or "-" for a regular file. The next three characters represent the read(r), write(w), and execute(X) rights for the file’s owner. The following three characters specify the same permissions for the group associated with the file, and the final three characters indicate the permissions granted to all other users on the system. Whenever a hyphen (-) appears in place of a letter(r,w or x), it means that particular permission is not granted. Beyond the permissions string, the listing also shows the user who owns the file (respresented by the color yellow) and the group ownership (respresented by the color blue).
</p>
<br />

