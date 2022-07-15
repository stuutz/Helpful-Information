<h1>Commands to get the Team ID and Code Requirement</h1>

<b>Input (binary)</b><br>
command: <i>codesign -dr - /usr/local/bin/jamf</i>

<b>Output</b><br>
Executable=/usr/local/jamf/bin/jamf designated => identifier "com.jamfsoftware.jamf" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] / exists / and certificate leaf[field.1.2.840.113635.100.6.1.13] / exists / and certificate leaf[subject.OU] = "483DWKW443"

<b>Input (app)</b><br>
command: <i>codesign -dr - /Library/Application\ Support/JAMF/Jamf.app</i>

<b>Output</b><br>
Executable=/Library/Application Support/JAMF/Jamf.app/Contents/MacOS/Jamf designated => identifier "com.jamf.management.Jamf" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] / exists / and certificate leaf[field.1.2.840.113635.100.6.1.13] / exists / and certificate leaf[subject.OU] = "483DWKW443"


<h1>Required data for Extension or PPPC paylod settings:</h1>

<b>Team ID:</b>
483DWKW443

<b>Identifier Type:</b><br>
Bundle ID (app) or Path (binary)

<b>Receiver Identifier</b><br>
com.jamfsoftware.jamf

<b>Code Requirement:</b><br>
identifier "com.jamfsoftware.jamf" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] / exists / and certificate leaf[field.1.2.840.113635.100.6.1.13] / exists / and certificate leaf[subject.OU] = "483DWKW443" 

or

anchor apple generic and identifier "com.jamf.management.service" and (certificate leaf[field.1.2.840.113635.100.6.1.9] /* exists */ or certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = "483DWKW443")

<h1>Resource:</h1>
https://docs.jamf.com/technical-articles/Preparing_Your_Organization_for_User_Data_Protections_on_macOS_10-14.html
