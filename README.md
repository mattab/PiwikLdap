# Piwik LoginLdap Plugin


## Description

Piwik login that uses LDAP queries to authenticate users.

HowTo Create a new User from LDAP in Piwik:
1) Login to Piwik backend as superuser
2) Navigate to Settings->LDAP Users
3) If the LDAP Settings are correct you are now able to look up users from your directory

Note:
Everytime a user is trying to login to your Piwik, the password is first of all checked
against your LDAP, if fails the plugin will check against the database.

Note2:
Users may be modified and deleted via Settings->Users

Note3:
If you change the username in LDAP/AD it will not be updated to Piwik!

Note4:
When LDAP users are initially added on the 'Settings->LDAP Users' page their password is not entered and stored in the database.
However, when they first login via the web interface their credentials will be saved correctly in a hashed format.
From that point on they can login via mobile apps and API in general.


## FAQ

https://github.com/tehnotronic/PiwikLdap/wiki


## Changelog

LoginLdap 2.0.0:
* First release for Piwik 2.0, may contain bugs!
* Added LDAP server port configuration option

LoginLdap 1.3.5:
* Issue #20 Fixed 'kerberos is not working'
* Issue #19 Fixed 'wrong version info'

LoginLdap 1.3.4:
* Issue #18 Fixed 'iconv() expects parameter 3 to be string array given'

LoginLdap 1.3.3:
* Issue #17 Fixed 'Undefined index: phpVersion'

LoginLdap 1.3.2:
* Issue #15 Fixed 'Setting a custom mail field has no effect'
* Issue #16 Fixed 'Login fails because of non-UTF8 values passed to json_encode()'

LoginLdap 1.3.1:
* Issue #7 Added check on the activate handler to ensure the php-ldap extension is installed.
* Issue #8 Only superuser can view (and modify) LDAP configuration
* Issue #9 Fixed 'Undefined index: activeDirectory'
* Issue #11 E-Mail Address Being Required
* Issue #12 Fixed 'Undefined index: topMenu'
* Issue #13 LDAP Users were not able login using the mobile app and using API in general as their credentials were not stored in the database.
* Applied fix for Piwik Dev Zone Ticket #734: 'Correction added so Page Overlay feature works'.
* Added functionality to ensure that the Login and LoginLDAP plugins are never enabled simultaneously.
* Removed support for IE6.
* Changed log file location so to be include into the plugin directory and more easy to find.

LoginLdap 1.3.0:
* Issue #1 Only superuser can modify LDAP configuration
* Issue #2 LDAP search filters
* Issue #3 Enable Kerberos login for piwik
* Issue #4 You cannot login as superuser if LDAP connection fails
* Issue #5 Add more LDAP logging options
* Issue #6 Error while trying to read a specific config file entry 'LoginLdap'

LoginLdap 1.2.0:
* ActiveDirectory Support
* Piwik >= 1.6 Install Bug Fix

LoginLdap 1.0.0:
* Initial Version just for plain anonymous Ldap


## Support

Please direct any feedback to https://github.com/tehnotronic/PiwikLdap