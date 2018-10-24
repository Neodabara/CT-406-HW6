# Marcus Brock
## CT-406-HW4-Razor
### The fourth homework assignment for CT-406


This assignment required two different security examples. The first being an example of authentication and ASP.NET core Identity and the
second being on authorization and secure-data. The first was just a simple log-in system, and the second is a more complex system that 
shows ASP.NET Core's ability to control what users are able to view due to securing data based on the user's owner ID and their status.

# **Questions**

1. Pick a vulnerability from the OWASP Top Ten (2017 edition is preferable) that we have not discussed in class. Explain it and how to use 
ASP.NET Core utilities to prevent it.

  One of the top ten web application security risks is cross site scripting. This is when an attacker is able to inject scripts from  
  their client into other pages that can be viewed publically by other people. They come in three forms, **Reflected XSS** , **Stored  
  XSS**, and **DOM XSS**. Luckily, the Razor MVCs in ASP.NET Core automatically encodes all output sourced from variables, meaning it 
  catches anything that you do not trust and encodes them so they no longer have the same value.   

2. Explain how passwords are stored in ASP.NET Core and how this relates to the concept of "Cryptographic Agility".

  Passwords are automatically hashed in ASP.NET Core. Passwords go through ten thousand iterations of the RFC2898 algorithm. This means 
  that as soon as the system recieves a password, it secures the password so that it is safely stored for the user. This also helps, 
  since it means that their is less of a need to change existing systems to include encrpytion and can easily be added upon with another 
  encryption method.

3. The Microsoft.AspNetCore.Identity defines the following domain classes. Please explain each:

+ IdentityRole
  uses a string as the primary key
+ IdentityUserRole
  Represents the link bbetween user and role
+ IdentityUserClaim
  Represents a claim that a user possesses
+ IdentityUserLogin
  Represents a login and its associated provider for a user
+ IdentityUserToken
  Represents an authentication  token for a user
+ IdentityRoleClaim
  Represents a claim that is granted to all users within a role
