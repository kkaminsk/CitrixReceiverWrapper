# Summary
The Citrix MSI wrapper was something that came up when modern desktop customers were trying to install the full-featured Citrix client for their users using the mobile device management protocol to deliver the software. The installers that make up the Citrix Reciever client do not conform to the constraints of single MSI deployment via MDM and the Citrix Reciever version updates with a frequent cadence. This installer builds upon a blog article by Peter Daalmans.

https://configmgrblog.com/2017/08/29/how-to-deploy-the-citrix-receiver-for-windows-10-via-microsoft-intune

And another article by Aaron Parker:
https://stealthpuppy.com/deploy-citrix-receiver-intune/

See my blog article over here:
http://www.checkyourlogs.net/?p=54093

# Features

**Always installs latest version:**
By downloading the underlying installer from Citrix this wrapper always installs the latest version of the Citrix Receiver.

**Signed:**
Provides a better UAC experience by using a code signing certificate from Starfield Technologies (GoDaddy) and ensures that you can have some confidence in the contents of the installation package.

**Source files:**
I've included source files in case you want to use Advanced Installer to recompile this installer from the original project files.

**Modern UI for manual installations:**
The installer uses a touch-friendly UI for modern devices.

**Supports manual installs:**
Added some text to the installation in case you want to hand this installer out to technicians or end users.

**Modern installer UI:**
The installer uses a touch friendly UI for modern devices.

**Supports uninstalls:**
I decided that the wrapper needed to support uninstalls as well.

**Pre-configured:**
The installation command line for the wrapper is as follows:
/silent /AutoUpdateCheck=auto /AutoUpdateStream=Current /DeferUpdateCount=5 /AURolloutPriority=Medium /NoReboot /AllowAddStore=N /EnableCEIP=false
