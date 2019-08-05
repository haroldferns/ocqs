
QuickStart with ownCloud
========================

Introduction
------------

ownCloud is a leading open source file-sharing and cloud collaboration platform offering real security and privacy for your data. With desktop clients for MacOS, Windows, and Linux, and mobile clients for iOS and Android, store and access your files securely from anywhere!

ownCloud is available in three editions: **[Online], [Enterprise], and Community**. This QuickStart guide provides instructions to install and configure the ownCloud Community Edition Server and clients quickly and easily. The clients support all three editions.

[Online]: https://owncloud.online/
[Enterprise]: https://owncloud.com/product-enterprise/

Installing ownCloud Server for non-technical users
--------------------------------------------------
The ownCloud Server appliance is the easiest and quickest way to get started with ownCloud. It is setup and configured to run securely out-of-the-box.

1. Download an appliance image for your virtualization platform. If you don't know which one to use, install [VirtualBox] and then download the appliance.

	*	Appliance for [VirtualBox]: [Ova image]
	*	Appliance for [VMware]: [ESX image], [VMware image]
	*	Appliance for [KVM]: [Kvm image]

[VMware]: https://www.vmware.com/
[VirtualBox]: https://www.virtualbox.org/
[KVM]: https://www.linux-kvm.org/page/Main_Page
[Ova image]:  https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-virtualbox.ova
[ESX image]:  https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-ESX.ova
[Kvm image]:  https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-KVM.qcow2
[VMware image]:  https://appcenter.software-univention.de/univention-apps/current/owncloud/Univention-App-owncloud-vmware.zip

	
2.	Install the appliance on your virtualization platform. Refer to the documentation for your platform if you need help with this.


3.	Setup your ownCloud Server instance
	Note: Keep a record of all the settings you provide in this section. You will need them later. 

	1. Select the appropriate Language, Locale, and keyboard settings.
	
	2. For Domain and Network configuration:
		Select the "Obtain IP address automatically (DHCP)" option.
		Use 8.8.8.8 and 8.8.4.4 for preferred and alternate DNS server, if needed.
		If use a proxy server, provide your proxy server details.

	3. For Domain setup:
		Choose "Manage users and permissions directly on this system" if you're not part of any domain or you don't know which option to choose.
		If you are part of a UCS or Active Directory domain, select your preferred option.
		
	4. For Account information:
		Provide your organization name, a real email address, and a strong password. This email address will be used to email you a license key file that will be needed for authorization.
		
	5. Host settings:
		Provide a Fully Qualified Domain Name (FQDN), if you can set one up else, use the  default values provided. 
		
	6. Confirm configuration settings: review everything and proceed.
	
	7. Wait till the install is complete and the server has rebooted. Proceed to configure ownCloud Server.


Installing ownCloud Server for experts
--------------------------------------
If you know what you're doing and choose to roll-your-own for production environments: 

OPTION 1: Download a [tarball] [tb] or [zipfile] [zp] and build. Refer to the [prerequisites] [pr] and [installation instructions] [ii] to proceed. 

OPTION 2: Add repositories or [download packages directly] [dr] and install for your preferred flavor of Linux. Refer to the [prerequisites] [pr] and [installation instructions] [ii] to proceed.  

OPTION 3: Get a [docker image] [dk] if you use Docker and install ownCloud Server using [these instructions] [dki]. 

[pr]: https://doc.owncloud.org/server/10.2/admin_manual/installation/system_requirements.html
[ii] :https://doc.owncloud.org/server/10.2/admin_manual/installation/manual_installation.html
[dr]: https://download.owncloud.org/download/repositories/production/owncloud/
[tb]: https://download.owncloud.org/community/owncloud-10.2.1.tar.bz2
[zp]: https://download.owncloud.org/community/owncloud-10.2.1.zip
[dk]: https://hub.docker.com/r/owncloud/server/
[dki]: https://doc.owncloud.org/server/latest/admin_manual/installation/docker/

Note: By default, the Docker ownCloud instance listens on port 8080 and allows HTTP (non SSL) connections. With options 1 and 2, the webserver listens on port 80 by default. For all three options, enable SSL on your webserver to ensure secure connections between server and client.


Configuring ownCloud Server
---------------------------
1. Access the ownCloud admin interface at https://<server ip or FQDN>/ from your web browser. You may receive a invalid trust certificate warning. Ignore this warning and proceed. 


2. Activation process: Supply the licence key you received at the email address that you provided during setup.  

3. Test that everything is working by navigating to https://<server ip>/owncloud and logging in with the Administrator credentials

Setting up user and groups
--------------------------
1. Log in using the username 'Administrator' and the password that you specified during setup earlier.

2. Navigate to Administrator > Users from the top right corner of the Admin console.

3. Create a new group by using the '+ Add Group' button at the top left corner of the Admin console.

4. Add users to the group by supplying a new username, email address, assigning a group and clicking 'Create'. You may set the quota and other details directly at a specific users record in the list.	

Downloading and installing a client
-----------------------------------
ownCloud has clients for multiple desktop platforms including Windows, MacOS, Linux, as well as Mobile platforms iOS and Android. Download your preferred client here:

	Desktop
	
	[Windows Client] [wc]
	[MacOS Client] [mc]
	[Linux Client] [lc]
	
	Mobile
	
	[iOS Client] [ioc]
	[Android Client] [ac]

[wc]: https://download.owncloud.com/desktop/stable/ownCloud-2.5.4.11654.11466.msi
[mc]: https://download.owncloud.com/desktop/stable/ownCloud-2.5.4.11456.pkg
[lc]: https://software.opensuse.org/download/package?project=isv:ownCloud:desktop&package=owncloud-client
[ioc]: https://apps.apple.com/app/id1359583808?ls=1
[ac]: https://play.google.com/store/apps/details?id=com.owncloud.android

	
Setting up and using your client with your ownCloud server instance
---------------------------------------------------------------------
1. Launch your preferred client.

2. At the server address prompt, enter https://<server ip or FQDN>/owncloud. 

3. You see a warning for an untrusted certificate. Select the option 'Trust this certificate anyway' and proceed.

4. Supply your username and password and log in.

5. Next, customize your server synchronization options and your local folder.
You see a message "Connected to <server address> as <username>. This indicates a successful connection.



Setting up ownCloud server to run on a non-standard port (e.g. 8080)
--------------------------------------------------------------------





















































































Markdown is a text-to-HTML conversion tool for web writers. Markdown
allows you to write using an easy-to-read, easy-to-write plain text
format, then convert it to structurally valid XHTML (or HTML).

Thus, "Markdown" is two things: (1) a plain text formatting syntax;
and (2) a software tool, written in Perl, that converts the plain text
formatting to HTML. See the [Syntax][] page for details pertaining to
Markdown's formatting syntax. You can try it out, right now, using the
online [Dingus][].

  [syntax]: /projects/markdown/syntax
  [dingus]: /projects/markdown/dingus

The overriding design goal for Markdown's formatting syntax is to make
it as readable as possible. The idea is that a Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters, the single biggest source of inspiration for Markdown's
syntax is the format of plain text email.

The best way to get a feel for Markdown's formatting syntax is simply
to look at a Markdown-formatted document. For example, you can view
the Markdown source for the article text on this page here:
<http://daringfireball.net/projects/markdown/index.text>

(You can use this '.text' suffix trick to view the Markdown source for
the content of each of the pages in this section, e.g. the
[Syntax][s_src] and [License][l_src] pages.)

  [s_src]: /projects/markdown/syntax.text
  [l_src]: /projects/markdown/license.text

Markdown is free software, available under a BSD-style open source
license. See the [License] [pl] page for more information.

  [pl]: /projects/markdown/license


Discussion List <a id="discussion-list" />
---------------

I've set up a public [mailing list for discussion about Markdown] [ml].
Any topic related to Markdown -- both its formatting syntax and
its software -- is fair game for discussion. Anyone who is interested
is welcome to join.

It's my hope that the mailing list will lead to good ideas for future
improvements to Markdown.

  [ml]: http://six.pairlist.net/mailman/listinfo/markdown-discuss


Installation and Requirements <a id="install" />
-----------------------------

Markdown requires Perl 5.6.0 or later. Welcome to the 21st Century.
Markdown also requires the standard Perl library module [Digest::MD5]
[md5], which is probably already installed on your server.

  [md5]: http://search.cpan.org/dist/Digest-MD5/MD5.pm


### Movable Type ###

Markdown works with Movable Type version 2.6 or later (including
Movable Type 3.0).

1.  Copy the "Markdown.pl" file into your Movable Type "plugins"
	directory. The "plugins" directory should be in the same directory
	as "mt.cgi"; if the "plugins" directory doesn't already exist, use
	your FTP program to create it. Your installation should look like
	this:

        (mt home)/plugins/Markdown.pl

2.  Once installed, Markdown will appear as an option in Movable Type's
	Text Formatting pop-up menu. This is selectable on a per-post basis:
	
	![Screenshot of Movable Type 'Text Formatting' Menu][tfmenu]
	
	Markdown translates your posts to HTML when you publish; the posts
	themselves are stored in your MT database in Markdown format.

3.	If you also install SmartyPants 1.5 (or later), Markdown will
	offer a second text formatting option: "Markdown With
	SmartyPants". This option is the same as the regular "Markdown"
	formatter, except that it automatically uses SmartyPants to create
	typographically correct curly quotes, em-dashes, and ellipses. See
	the [SmartyPants web page][sp] for more information.

4.	To make Markdown (or "Markdown With SmartyPants") your default
	text formatting option for new posts, go to Weblog Config:
	Preferences.

Note that by default, Markdown produces XHTML output. To configure
Markdown to produce HTML 4 output, see "Configuration", below.

  [sp]: http://daringfireball.net/projects/smartypants/



### Blosxom ###

Markdown works with Blosxom version 2.0 or later.

1.  Rename the "Markdown.pl" plug-in to "Markdown" (case is
    important). Movable Type requires plug-ins to have a ".pl"
    extension; Blosxom forbids it.

2.  Copy the "Markdown" plug-in file to your Blosxom plug-ins folder.
    If you're not sure where your Blosxom plug-ins folder is, see the
    Blosxom documentation for information.

3.  That's it. The entries in your weblog will now automatically be
	processed by Markdown.

4.	If you'd like to apply Markdown formatting only to certain
	posts, rather than all of them, Markdown can optionally be used in
	conjunction with Blosxom's [Meta][] plug-in. First, install the
	Meta plug-in. Next, open the Markdown plug-in file in a text
	editor, and set the configuration variable `$g_blosxom_use_meta`
	to 1. Then, simply include a "`meta-markup: Markdown`" header line
	at the top of each post you compose using Markdown.

  [meta]: http://www.blosxom.com/plugins/meta/meta.htm


### BBEdit ###

Markdown works with BBEdit 6.1 or later on Mac OS X. It also works
with BBEdit 5.1 or later and MacPerl 5.6.1 on Mac OS 8.6 or later. If
you're running Mac OS X 10.2 (Jaguar), you may need to install the
Perl module [Digest::MD5] [md5] from CPAN; Digest::MD5 comes
pre-installed on Mac OS X 10.3 (Panther).

1.  Copy the "Markdown.pl" file to appropriate filters folder in your
	"BBEdit Support" folder. On Mac OS X, this should be:

        BBEdit Support/Unix Support/Unix Filters/

    See the BBEdit documentation for more details on the location of
    these folders.

    You can rename "Markdown.pl" to whatever you wish.

2.  That's it. To use Markdown, select some text in a BBEdit document,
	then choose Markdown from the Filters sub-menu in the "#!" menu, or
	the Filters floating palette



Configuration  <a id="configuration"></a>
-------------

By default, Markdown produces XHTML output for tags with empty elements.
E.g.:

    <br />

Markdown can be configured to produce HTML-style tags; e.g.:

    <br>


### Movable Type ###

You need to use a special `MTMarkdownOptions` container tag in each
Movable Type template where you want HTML 4-style output:

    <MTMarkdownOptions output='html4'>
        ... put your entry content here ...
    </MTMarkdownOptions>

The easiest way to use MTMarkdownOptions is probably to put the
opening tag right after your `<body>` tag, and the closing tag right
before `</body>`.

To suppress Markdown processing in a particular template, i.e. to
publish the raw Markdown-formatted text without translation into
(X)HTML, set the `output` attribute to 'raw':

    <MTMarkdownOptions output='raw'>
        ... put your entry content here ...
    </MTMarkdownOptions>


### Command-Line ###

Use the `--html4tags` command-line switch to produce HTML output from a
Unix-style command line. E.g.:

    % perl Markdown.pl --html4tags foo.text

Type `perldoc Markdown.pl`, or read the POD documentation within the
Markdown.pl source code for more information.


Acknowledgements <a id="acknowledgements" />
----------------

[Aaron Swartz][] deserves a tremendous amount of credit for his feedback on the
design of Markdown's formatting syntax. Markdown is *much* better thanks
to Aaron's ideas, feedback, and testing. Also, Aaron's [html2text][]
is a very handy (and free) utility for turning HTML into
Markdown-formatted plain text.

[Nathaniel Irons][], [Dan Benjamin][], [Daniel Bogan][], and [Jason Perkins][]
also deserve thanks for their feedback.

[Michel Fortin][] has ported Markdown to PHP; it's a splendid port, and highly recommended for anyone looking for a PHP implementation of Markdown.

  [Aaron Swartz]:		http://www.aaronsw.com/
  [Nathaniel Irons]:	http://bumppo.net/
  [Dan Benjamin]:		http://hivelogic.com/
  [Daniel Bogan]:		http://waferbaby.com/
  [Jason Perkins]:		http://pressedpants.com/
  [Michel Fortin]:		http://www.michelf.com/projects/php-markdown/
  [html2text]:          http://www.aaronsw.com/2002/html2text/
 
  [tfmenu]: /graphics/markdown/mt_textformat_menu.png
