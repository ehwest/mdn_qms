# Security Audit Template

*Instructions*

Prior to the audit, the employee being audited should read these documents:

1. [Medical Data Networks HIPPA Policy Overview]()
2. [Medical Data Networkss Privacy and Confidentality Training]()
3. [Medical Data Networks Employee Security Practices]()

The auditor (not the employee being audited) should make a copy of this document and is responsible for filling it out.
Then share it with the employee being audited can then edit the document in suggestion mode and add screen shots.

For each line, the auditor should observe the item and mark one of:
* [ ] YES (auditor has observed that this is done)
* [ ] NO-PENDING (auditors have observed that this is NOT done and needs to be done).
* [ ] N/A (This line is not applicable because the employee does not use this service).

***How To Take Screen Shots***
* On Mac, use the Command+Control+Shift+4 to copy a region to the clipboard and paste to the document.
* Windows users can use the Snipping Tool or various shortcuts to capture screenshots.
* IOS Devices can capture screenshots by pushing the Home + Power button simultaneously
* Android devices vary, but frequently use Power + Volume Down

** Auditor **
Make a copy of this document.  Name it like this: 

YY-MM-DD Employee --
Full Name  --
Medical Data Networks Security Audit Checklist

Medical Data Networks Employee Full Name:  _full name_
Auditors (at least 1 auditor is required):

Auditor 1:  _name_

Auditor 2:  _name_

Date audit started:  _date_

Date audit completed:  _date_

Audit Passed:  [ ] YES  [ ] NO-PENDING

Auditor Digital Signature Line (/s/_name_date):

_

***Training Materials***

[ ] YES  [ ] NO  Employee confirms that they have read and understood these training documents:

* [Medical Data Networks HIPAA Policy_Overview]()
* [Medical Data Networks Privacy and Confidentiality Training]()
* [Medical Data Networks Employee Security Practices]()

Employee Digital Signature Line (/s/_name_date):

***Account Security***

[ ] YES  [ ] NO  TWO-FACTOR or MULTI_FACTOR authentication and password security for Google cloud based accounts is implemented.  Screen shots showing this shall be provided in the audit record.


***Password Strength***

[ ] YES  [ ] NO  Password strength for all passwords used for Google cloud shall meet the test of 1Password.  Screen shots showing this shall be provided in the audit record.

***Applications NOT USED***

[ ] YES  [ ] NO  Employee certifies that NONE of these services are used to store data for Medical Data Networks:  Dropbox, iCloud Drive, Microsoft 365, Office Online, Slack, Rollbar, Shopify, Contentful

***Added Applications***

* [ ] YES  [ ] NO  Employee certifies that any new or additional accounts will be protected with TWO-FACTOR or MULTI_FACTOR Authentication.

Auditor Digital Signature Line (/s/_name_date):

***AWS Applications***

[ ] YES  [] NO  [ ] N/A  Employee has access to AWS Administration and therefore AWS protections are applicable.

_[ ] YES  [ ] NO  [ ] N/A Do all ssh key pairs use a strong keyprase?  Attach screenshot of passphrase settings.
_[ ] YES  [ ] NO  [ ] N/A Have SSH key pairs been rotated in the last year?
_[ ] YES  [ ] NO  [ ] N/A Have employees with AWS ssh access read and agreed to follow and demonstrate the use of appropriate ssh policy?  [SSH Key_Handling_Practices.md(https://github.com)   [Runbook_modified.md(https://github.com)


_[ ] YES  [ ] NO  [ ] N/A   Employee certifies that all system admin accounts will be protected with TWO_FACTOR or MULTI_FACTOR for all critical accounts and that keys will be stored in accordance with Medical Data Network's password and authentication policies.

Show screenshots

_[ ] YES  [ ] NO  [ ] N/A npm (show output of npm profile get, should say auth-and-writes).

_[ ] YES  [ ] NO  [ ] N/A npm Digital Ocean.

_[ ] YES  [ ] NO  [ ] N/A MongoDB Atlas.

Auditor Digital Signature Line (/s/_name_date):


* [ ] YES  [ ] NO  [ ] N/A   BAA In place for Medical Data Networks for Google Email.

* [ ] YES  [ ] NO  [ ] N/A   When employee sends or forwards and email that includes PHI, employee agrees to edit the subject line to preface it with 
"PHI".  Employee Digital Signature Line (/s/_name_date):


* [ ] YES  [ ] NO  [ ] N/A   Employee agrees to set up a "PHI"  mail filter to segregate email with PHI by using email subject line and "skip inbox" filter.  Screenshot attached.

**Computer Security**
For each computer used to access Medical Data Networks, repeat the following series of audit questions:

* [ ] YES  [ ] NO  [ ] N/A   Hard drive is secured with FileVault (Mac), or BitLocker/VeraCrypt (for windows).  Provide screenshot showing evidence.

* [ ] YES  [ ] NO  [ ] N/A   Screensaver is set to lock your computer after no longer than 5 minutes and requie a password immediately after sleep or screensaver begins.  Provide screenshot showing evidence.

* [ ] YES  [ ] NO  [ ] N/A   Employee verbally confirms they use a strong password for computer login.  A strong password includes multiple words, 10 characters and no trivial substitutions of numbers for letters or letters for numbers.

* [ ] YES  [ ] NO  [ ] N/A   For MAC computers, "enable iCloud Find my Mac"  Provide screenshot showing location.

* [ ] YES  [ ] NO  [ ] N/A   For any local backups, be sure to encrypt the backups.  Provide screenshot of backup showing it is encrypted.

