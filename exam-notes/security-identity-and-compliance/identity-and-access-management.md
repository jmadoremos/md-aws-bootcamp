# Exam Notes | Identity and Access Management (IAM)

* IAM is always **GLOBAL** region

* You can customize (ie, set alias) your IAM users sign-in lnk

* **root account** - email address used to sign-up in AWS; has complete admin access by default

* programmatic key access - use Access Key ID as username, then Secret Access Key as password

* for Console access - use User as username, then Password as password

* new users have **no permission** when first created

* new users are assigned **Access Key ID** & **Secret Access Key** when first created

* Security steps:

    * delete your root access keys

    * Activate MFA - select MFA able device

    * Create individual IAM users

    * Use groups to assign permissions

    * Apply an IAM password policy

* You can only **view the user credentials once**. Once you loose them, you need to regenerate them.
