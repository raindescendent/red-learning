Permissions
> root: superuser


- Change Ownership

[User]
> CHOWN - chown {user} {relativePath}
[Group]
> CHGRP - chgrp {user} {relativePath}

------------------------------------------------------------------------------

- Checking Permissions (ls -l)

[Levels] 
> set (rwx)
>> 'X': Execute
>> 'W: Write
>> 'R: Read

[Command]
> ls -l  

drwxr-xr-x. 1 santigimenez santigimenez 418 Feb 27 19:21 arc-theme
drwxr-xr-x. 1 santigimenez santigimenez 130 May 12 14:18 Desktop

[Output]
>> drwxr-xr-x // SYNTAX: file type (d) + permissions [own, grp, users] - (rwx, rx, rx)
>> links
>> owner
>> file/directory size (bytes)
>> file/directory create or modify date
>> name of the file/directory

------------------------------------------------------------------------------

- Changing Permissions (chmod)

> set (rwx) require a octal-system value to define the specific level of permission

------------------------------------------
BIN     OCTAL   RWX
000     0       ---
001     1       --x     (1 == execute)
010     2       -w-     (2 == write)
011     3       -wx
100     4       r--     (4 == read)
101     5       r-x
110     6       rw-
111     7       rwx
------------------------------------------

Linux All permissions
4 (r) + 2 (w) + 1 (x) = 7 

[Command]
> ls -l 
[Output]
>> -rw-r--r--. 1 santigimenez santigimenez 418 Feb 27 19:21 newhackertool
[Command]
> chmod 766 newhackertool 
[Output]
>> -rwxrw-rw-. 1 santigimenez santigimenez 418 Feb 27 19:21 newhackertool   

------------------------------------------------------------------------------

UGO System (set, add or remove rwx)

ID's
'u': user (owner)
'g': group
'o': others

OPERATORS
'=': SET
'+': ADD
'-': REMOVE

[Command]
> ls -l 
[Output]
>> -rw-r--r--. 1 santigimenez santigimenez 418 Feb 27 19:21 newhackertool
[Command]
> chmod u+x newhackertool 
[Output]
>> -rwxrw-rw-. 1 santigimenez santigimenez 418 Feb 27 19:21 newhackertool
[Command]
> chmod g+x newhackertool 
[Output]
>> -rwxrwxrw-. 1 santigimenez santigimenez 418 Feb 27 19:21 newhackertool


------------------------------------------------------------------------------

- Special Permissions - Set us er/group ID (SUID/SGID)
- Escalando privilegios 

> SUID: Program grants temporary owner permissions for a specifically file/action regardless of the user who executes it.

[Commands]

> find / -user root -perm 4000

> chmod 4655 /usr/bin/sudo (4[SUID]+644[permissions]) || (4000 the format to set the SUID+permissions)
OR
> chmod u+s /usr/bin/sudo

> ls -l

[Output]
>> -rwsr-xr-x 1 santigimenez santigimenez 418 Feb 27 19:21 sudo // ('s' == SUID)   


> SGID: Grants temporary GROUP OWNER permission even if the user doesnt have that permissions of the group. 
[Command]
> chmod 2644 /usr/bin/password.bin (2 == SGID, 644 permissions [own, grp, users])
OR
> chmod g+s /usr/bin/password.bin


