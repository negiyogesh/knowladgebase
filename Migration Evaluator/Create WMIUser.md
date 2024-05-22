**Create the User Account:**
    a. Open the "Computer Management" console. You can do this by right-clicking on "This PC" or "My Computer" and selecting "Manage".
    b. In the Computer Management window, navigate to "Local Users and Groups" > "Users".
    c. Right-click in the empty area and select "New User".
    d. Provide the necessary details for the new user, such as username and password.
    e. Ensure that the user is not a member of any administrative groups unless necessary for other purposes.

**Add User to Performance Monitor Users Group:**
    a. Still in the Computer Management console, navigate to "Local Users and Groups" > "Groups".
    b. Double-click "Performance Monitor Users".
    c. Click "Add" and add the user you created in the previous step.
    d. Click "OK" to close the dialog.

**Grant Permissions:**
    a. Open the "Control Panel" and navigate to "Administrative Tools" > "Component Services".
    b. In the Component Services window, expand "Component Services" > "Computers" > "My Computer".
    c. Right-click on "My Computer" and select "Properties".
    d. Go to the "COM Security" tab.
    e. Under "Access Permissions", click "Edit Limits...".
    f. Ensure that the user account you created has the following permissions:
        Execute Methods
        Enable Account
        Remote Enable
        Remote Activation
        g. Click "OK" to close the dialog.

**Grant Namespace Access:**
    a. Still in the Component Services window, expand "Component Services" > "Computers" > "My Computer".
    b. Right-click on "My Computer" and select "Properties".
    c. Go to the "COM Security" tab.
    d. Under "Launch and Activation Permissions", click "Edit Limits...".
    e. Ensure that the user account you created has the necessary permissions to access the following namespaces:
        \root\cimv2
        \root\default
        \root\standardcimv2 (if using Windows Server 2012 or greater)
        f. Click "OK" to close the dialog.

**Test Access:**
    After completing these steps, you can test the WMI access using the newly created user account to ensure that it can retrieve the required information and perform the necessary tasks.

By following these steps, you should be able to create a Windows user account with the specified access for WMI.