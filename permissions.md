#     Powershell Permissions

## 1. Get-Acl 
The Get-Acl cmdlet gets objects that represent the security descriptor of a file or resource. The security descriptor contains the access control lists (ACLs) of the resource. The ACL specifies the permissions that users and user groups have to access the resource.

Beginning in Windows PowerShell 3.0, you can use the InputObject parameter of Get-Acl to get the security descriptor of objects that do not have a path.


` Get-acl`


    Directory: C:\Users


`Path  Owner               Access`


`----  -----               ------`

`kasin NT AUTHORITY\SYSTEM NT AUTHORITY\SYSTEM Allow  FullControl...`

## 2. Set-Acl

Changes the security descriptor of a specified item, such as a file or a registry key.

The Set-Acl cmdlet changes the security descriptor of a specified item, such as a file or a registry key, to match the values in a security descriptor that you supply.

To use Set-Acl, use the Path or InputObject parameter to identify the item whose security descriptor you want to change. Then, use the AclObject or SecurityDescriptor parameters to supply a security descriptor that has the values you want to apply. Set-Acl applies the security descriptor that is supplied. It uses the value of the AclObject parameter as a model and changes the values in the item's security descriptor to match the values in the AclObject parameter.

Examples

Example 1: Copy a security descriptor from one file to another
`PowerShell`

`$DogACL = Get-Acl -Path "C:\Dog.txt"`

`Set-Acl -Path "C:\Cat.txt" -AclObject $DogACL`

These commands copy the values from the security descriptor of the Dog.txt file to the security descriptor of the Cat.txt file. When the commands complete, the security descriptors of the Dog.txt and Cat.txt files are identical.

