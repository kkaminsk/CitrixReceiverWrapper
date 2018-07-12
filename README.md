# Summary
The Citrix MSI wrapper was something that came up when modern desktop customers were trying to install the full featured Citrix client for their users using the mobile device management protocol to deliver the software. The installers that make up the Citrix Reciever client do not conform to the constraints of single MSI deployment via MDM and the Citrix Reciever version updates with a frequent cadence. This installer builds upon a blog article by Peter Daalmans.

https://configmgrblog.com/2017/08/29/how-to-deploy-the-citrix-receiver-for-windows-10-via-microsoft-intune

# Features

**Signed**
Makes UAC happy and ensures that you can have some confidence in where the installer came from.

**Source files**
I've included source files in case you want to use advanced installer to customize this installer.

**Modern UI for manual installations**
The installer uses a touch friendly UI for modern devices.

**Supports manual installs**
Added some text to the installation in case you want to hand this installer out to technicians or end users.

**Supports uninstalls**
The blog article didn't cover it but I decided that the wrapper needed to support uninstalls as well.

**Pre-configured**
The installation command line for the wrapper is as follows:
/silent /AutoUpdateCheck=auto /AutoUpdateStream=Current /DeferUpdateCount=5 /AURolloutPriority=Medium /NoReboot /AllowAddStore=N /EnableCEIP=false