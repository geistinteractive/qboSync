## 1.5.0

released 10/11/2016

First release of a new file which converts data sent to the same script names (and internal id's) as earlier versions of fmQBO but translates those parameters into a format that fmQBO2 can accept, then translates fmQBO2's response into the same format earlier versions of fmQBO returned. More info available here: http://docs.fmqbo.com/article/87-migrating-from-fmqbo-version-1



### 1.2.1

released 7/5/2016

fmQBODeveloper 1.2.1

  - bug fixes:
    - Report Query does't show appropriate options

qboInvoicer 2016-JUL-05

  - bug fixes:
    - duplicate line items exist after pushing an Invoice
	- properly autosize portal on Invoice Detail layout



### 1.2.0

released 5/17/2016

fmQBO

  - enhancements:
    - update BaseElements plugin to version 3.2
    - log fmQBO version on error
    - add fmQBO logo as launch center icon
    - update multiple json custom functions
    - update JSON module to version 1.0.5
  - bug fixes:
    - deleting a connection shows error if connection is not in web app
    - error returned if fmQBO is on a layout with no records when calling an API script

fmQBODeveloper 1.2.0

  - enhancements:
    - in generated script steps: return $result from Exit Script step when testing for an error
    - update custom functions: jsonModify, jsonOp
    - validate user json before creating a request
    - strip returns/whitespace from email/license in Settings
  - bug fixes:
    - don't show error on close when fmQBO isn't found
    - close file when BaseElements is not valid
    - update links to QBO documentation

Custom Functions 2016-MAY-04

  - enhancements:
  	- add jsonFilter function
  	- update jsonModify
  	- update jsonOp

qboInvoicer 2016-MAY-05

  - enhancements:
    - update custom functions: jsonModify, jsonOp
  - bug fixes:
    - Pull From QuickBooks: some buttons leave user on other layout
    - minor layout/UI discrepancies
    - Builder module's config script



### 1.1.2

released 6/17/2015

fmQBO

  - bug fixes:
    - Intermittent failures when two copies of fmQBO are open at the same time.
    - Deactivating a device fails if the license is not selected by clicking on it first.

qboInvoicer 2015-JUN-17

  - bug fixes:
    - Only the first line from the Customers billing address is extracted.



### 1.1.1

released 5/20/2015

fmQBO

  - bug fixes:
    - Some script steps that are not server compatible are being run on the server.
    - Global search field defaults to "test".
    - Under certain circumstances, when the plugin isn't installed, the error returned says "parameter was not json" instead of "plugin invalid".
    - Authentication error after disconnecting a connection record. Will now disconnect when deleting the portal row.
    - FileMaker error 3 shown after clicking refresh license data button in Licenses portal and Device portal under certain circumstances.
    - Not disconnected from QBO when a license record is deleted from the portal. 

fmQBODeveloper 1.1.1

  - bug fixes:
    - Generated request script steps for a query include a request parameter, which isn't needed. They also do not use the variable set at the top of this section (the query exists in two places).

qboInvoicer 2015-MAY-15

  - bug fixes:
    - Opening script contains invalid perform script steps.



### 1.1.0

released 5/13/2015

fmQBO

  - enhancements:
    - Don't require password change on first login.
    - Add "send logs to support" button to licenses portal.
    - Install the 64 bit BaseElements plugin in FileMaker Pro 14 x64.
    - Add icon to Saved Logs layout for performing a find, show all, and delete.
    - Change most buttons to popovers as a means of confirmation and showing additional information about the action that will be performed.


fmQBODeveloper 1.1.0

  - enhancements:
    - Add "test jsonGet" tab to full screen response viewer.
    - Add "send logs to support" button to Settings layout.
    - Add link to open fmQBO from main navigation.
    - Faster loading of a Field Map.
  - bug fixes:
    - Minor interface issues.
    - Generated Parse and Build script steps have the wrong $variableName under certain circumstances.
    - New Field Map does not load when navigating records via toolbar, menu, or keyboard shortcut.


fmQBO Client Helper Scripts 1.0.1

  - enhancements:
  	- Refresh cache to be sure the license data is accurate.



### 1.0.3

released 5/1/2015

fmQBODeveloper 1.0.2

  - bug fixes:
    - Copying fmQBO scripts ddo not copy the selected email/license/sandbox state.



### 1.0.2

released 4/29/2015

fmQBODeveloper 1.0.1

  - bug fixes:
    - Attribution does not default to user name.
    - Field map does not show records in portal for a new mapping record.
    - Generated request script steps do not set $request for Delete or Query action.
    - Generated request script steps set $request to "?" when invalid json entered for Create and Update action.
    - Request details layout replaced query on record load.



### 1.0.1

released 4/24/2015

fmQBO

  - bug fixes:
    - Cannot query count(*).



### 1.0.0

released 4/22/2015

fmQBO

  - bug fixes:
    - `fmQBO Connect if Required` script only returns a result if a connection was required.


fmQBODeveloper 1.0.0

  - bug fixes:
    - Wrong field on Find Script Generator.
    - Can't delete license records.
    - Reports request generator extracts the wrong value from the response.
  - enhancements:
    - Add full screen popover for viewing response.


qboInvoicer

  - enhancements:
    - Add Changelog script.


fmQBO Client Helper Scripts 1.0.0

  - enhancements:
  	- Add readme and version script.


Custom Functions 2015-APR-22

  - enhancements:
  	- Return ? on error.
  	- Store error message in $json.error.
  	- Normalize whitespace.



### 1.0.0-beta5

released 3/30/2015

fmQBO

  - bug fixes:
    - Connecting with an empty email/licenseString returns an incorrectly formatted error.
  - enhancements:
    - Add web viewer for viewing logs.


fmQBODeveloper

  - bug fixes:
  	- Can't connect to fmQBO running on a server.
  	- Can't delete parameters from reports.
  	- Reports request generator with multiple parameters creates an invalid request.
