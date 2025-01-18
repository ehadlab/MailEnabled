# MailEnabled
Installing and configuring MailEnable

SUMMARY

Guide to installing and configuring MailEnable. Includes basic pre and post installation requirements.
DETAIL

Configuring the environment
Before installing MailEnable, ensure that the environment has been configured correctly. This includes configuring network connectivity and the public DNS Server. MailEnable should be configured in an environment with a static IP address.

1. Before installing MailEnable, ensure that the machine can access the Internet (i.e.: ping www.mailenable.com). Ensure that other computers can ping the server's IP address from the Internet (technically computers do not need to be able to ping the server, but they will need to be able to connect to TCP/IP ports 110 and 25 of the server). In most cases, this requires some firewall configuration. You will need to allow the following ports through your firewall, depending on the services you are running. If you have configured MailEnable to listen or send on other ports, you will of course need to permit these through the firewall. These ports listed below are the defaults you would normally use, and will change depending on your needs. Remember to keep port 25 inbound though, as remote servers will only deliver to port 25.

Service 	Port 	Inbound 	Outbound
POP 	110 	allow 	allow
POP (SSL) 	995 	allow 	allow
SMTP 	25 	allow 	allow
SMTP Alternate Port 	587 	allow 	allow
SMTP (SSL) 	465 	allow 	allow
IMAP 	143 	allow 	deny
IMAP (SSL) 	993 	allow 	deny
LDAP 	389 	allow 	deny
Webmail 	80 	allow 	deny
Webmail (SSL) 	443 	allow 	deny
CalDAV/CardDAV 	8080 	allow 	deny
CalDAV/CardDAV SSL 	8443 	allow 	deny
XMPP 	5222 	allow 	allow

LDAP is only available in the Enterprise editions of MailEnable and XMPP/CalDAV/CardDAV require at least the Professional version.

2. Ensure that the correct entries are registered in the DNS. The first step to doing this is to determine who has control of your public DNS records. Contact your ISP or DNS provider to determine who holds the records for the domain. This will allow you to determine who can create new DNS records for the domain. When hosting mail for a domain, each domain being hosted requires a number of DNS records to be created. The DNS records that need to be created are listed here: Article ME020048

It is important to understand the role of DNS and how it relates to running mail servers. This is outlined in the following Knowledge Base article:   Article ME020190

Installing the MailEnable software
Now that the environment is configured, MailEnable can be installed. The product manuals explain how to install MailEnable.  These are installed with the product or available from our website here: https://www.mailenable.com/references.asp

Once MailEnable has been installed, check the MailEnable Diagnostic Report to ensure that all services are configured correctly. Instructions on accessing this report can be found here: Article ME020136

Configuring the MailEnable software
MailEnable provides a 'quick start' guide with basic instructions on configuring and running the MailEnable software.
Quick Start Guide: https://www.mailenable.com/support/MailEnable_Quick_Start_Guide.pdf

Exploring and configuring MailEnable features
Each version of MailEnable has specific features. Review the manual of each respective edition to review and configure some of the more advanced features. See https://www.mailenable.com/references.asp
MORE INFORMATION

Which DNS Server should be used with MailEnable?: Article ME020043

Product:	MailEnable (All Versions)
Article:	ME020202
Module:	General
Keywords:	Installation,DNS,configuration,configure,configuring,installing,install
Class:	HOWTO: Product Instructions
Revised:	Thursday, January 11, 2024
Author:	MailEnable
Publisher:	MailEnable


created by mayank
mail:mayak@ad.lab:mayank@ad.lab
