# QuickStart with ownCloud

## Introduction

ownCloud is a leading open source file-sharing and cloud collaboration platform offering real security and privacy for your data. With desktop clients for MacOS, Windows, and Linux, and mobile clients for iOS and Android, store and access your files securely from anywhere!

ownCloud is available in three editions: [Online], [Enterprise], and Community. This QuickStart guide provides instructions to install and configure the ownCloud Community Edition Server and clients quickly and easily. The clients support all three editions.

[Online]: https://owncloud.online/
[Enterprise]: https://owncloud.com/product-enterprise/


## Installing ownCloud Server for non-technical users

The ownCloud Server appliance is the easiest and quickest way to get started with ownCloud. It is setup and configured to run securely out-of-the-box on standard virtualization platforms like VMware. Download an appliance image for your virtualization platform. If you don't know which one to use, install [VirtualBox] and then download the appliance.

* Appliance for [VirtualBox]: [Ova image]
* Appliance for [VMware]: [ESX image], [VMware image]
* Appliance for [KVM]: [Kvm image]

[VMware]: https://www.vmware.com/
[VirtualBox]: https://www.virtualbox.org/
[KVM]: https://www.linux-kvm.org/page/Main_Page
[Ova image]: https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-virtualbox.ova
[ESX image]: https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-ESX.ova
[Kvm image]: https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-KVM.qcow2
[VMware image]: https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-vmware.zip

1.	**Install the appliance** on your virtualization platform. Refer to the platform documentation if needed.

2.	**Setup your ownCloud Server instance**. Keep a record of all the settings you provide in this section. You will need them later. 

	2.1	**Select the appropriate Language**, Locale, and keyboard settings.
	
	2.2	**Domain and Network configuration**:
* Select the **"Obtain IP address automatically (DHCP)"** option.
* Use 8.8.8.8 and 8.8.4.4 for preferred and alternate DNS server, if needed.
* If you use a proxy server, provide your proxy server details.

	2.3 **Domain setup**:
* Choose **"Manage users and permissions directly on this system"** if you're not part of any domain or you don't know which option to choose.
* If you are part of a UCS or Active Directory domain, select your preferred option.
		
	2.4 **Account information**:
		Provide your organization name, a real email address, and a strong password. This email address will be used to email you a license key file that will be needed for authorization.
		
	2.5 **Host settings**:
		Provide a Fully Qualified Domain Name (FQDN), if you can set one up else, use the  default values provided. 
		
	2.6 **Confirm configuration settings**: review everything and proceed.
	
	2.7 Once the installation is complete and the server has rebooted, proceed to configure ownCloud Server.


## Installing ownCloud Server for experts

You know what you're doing and choose to roll-your-own for production environments using one of these three options: 

1.	Download a [tarball] or [zipfile] and build. Refer to the [prerequisites] and [installation instructions] [ii] to proceed. 

2.	Add repositories or [download packages directly] [dr] and install for your preferred flavor of Linux. Refer to the [prerequisites] and [installation instructions] [ii] to proceed.  

3.	Get a [docker image] [dk] if you use Docker and install ownCloud Server using [these instructions] [dki]. 

[tarball]: https://download.owncloud.org/community/owncloud-10.2.1.tar.bz2
[zipfile]: https://download.owncloud.org/community/owncloud-10.2.1.zip
[prerequisites]: https://doc.owncloud.org/server/10.2/admin_manual/installation/system_requirements.html
[ii]: https://doc.owncloud.org/server/10.2/admin_manual/installation/manual_installation.html
[dr]: https://download.owncloud.org/download/repositories/production/owncloud/
[dk]: https://hub.docker.com/r/owncloud/server/
[dki]: https://doc.owncloud.org/server/latest/admin_manual/installation/docker/

**Note**: By default, the Docker ownCloud instance listens on port 8080 and allows HTTP (non SSL) connections. With options 1 and 2, the webserver listens on port 80 by default. For all three options, enable SSL on your webserver to ensure secure connections between server and client.


## Configuring ownCloud Server

1. Access the ownCloud admin interface at https://\<server ip or FQDN\>/ from your web browser. You may receive a invalid trust certificate warning. Ignore this warning and proceed.

2. During activation, you will be asked to provide a license key. Supply the license key you received at the email address that you provided during setup.

3. Test that everything is working by navigating to https://\<server ip\>/owncloud and logging in with the Administrator credentials. 

## Setting up users and groups

1. Log in using the username 'Administrator' and the password that you specified during setup earlier

2. Navigate to Administrator > Users from the top right corner of the Admin console

3. Create a new group by using the '+ Add Group' button at the top left corner of the Admin console

4. Add users to the group by supplying a new username, email address, assigning a group and clicking 'Create'. You may set the quota and other details directly at a specific user's record in the list.

## Downloading and installing a client

ownCloud has clients for multiple desktop platforms including Windows, MacOS, Linux, as well as Mobile platforms iOS and Android. Download your preferred client here:

1. Desktop Clients
	*	[MacOS Client] [mc]
	*	[Windows Client] [wc]
	*	[Linux Client] [lc]
	
2.	Mobile Clients
	*	[iOS Client] [ioc]
	*	[Android Client] [ac]

[wc]: https://download.owncloud.com/desktop/stable/ownCloud-2.5.4.11654.11466.msi
[mc]: https://download.owncloud.com/desktop/stable/ownCloud-2.5.4.11456.pkg
[lc]: https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client
[ioc]: https://apps.apple.com/app/id1359583808?ls=1
[ac]: https://play.google.com/store/apps/details?id=com.owncloud.android

	
## Setting up and using your client

1. Launch your preferred client

2. At the server address prompt, enter https://\<server ip or FQDN\>/owncloud 

3. You see a warning for an untrusted certificate. Select the option **"Trust this certificate anyway"** and proceed.

4. Supply your username and password and log in.

5. Next, customize your server synchronization options and your local folder.
The message "Connected to \<server address\> as \<username\>" indicates a successful connection.



## Setting up ownCloud server to run on a non-standard port (e.g. 8080)


