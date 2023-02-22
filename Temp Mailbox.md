**How to Fix "We can't sign into your account" and 'You've been signed in with a temporary profile' Error in Windows 10**

A [**user profile**](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/legacy/bb776892(v=vs.85)) is a collection of settings that make the computer look and work the way you want it to for a user account. It is stored in the user's **C:\Users\<user name>** profile folder, and contains the account's settings for desktop backgrounds, screen savers, pointer preferences, sound settings, and other features. User profiles ensure that your personal preferences are used whenever you sign in to Windows.

If a user signs in to their account and gets [**We can't sign into your account**](https://support.microsoft.com/en-us/windows/windows-error-message-we-can-t-sign-in-to-your-account-18d55f00-a6e7-9106-29ee-54fa223c0ca8) message and **You've been signed in with a temporary profile** notification message below, then that user has been signed in to a temporary profile (ex: **C:\Users\TEMP** ) instead of the profile from their **C:\Users\<user name>** profile folder. Any changes that the user makes to the temporary profile are lost after signing.

We can't sign into your account

This problem can often be fixed by signing out of your account and then signing back in. If you don't sign out now, any files you create or changes you make will be lost.

You've been signed in with a temporary profile.

You can't access your files, and files created in this profile will be deleted when you sign out. To fix this, sign out and try signing in later. Please see the event log for more details or contact your system administrator.

This tutorial will show you how to fix the **"We can't sign into your account"** and **"You've been signed in with a temporary profile"** error for a user account in **Windows 10** and **Windows 11**.

![Note](https://www.tenforums.com/images/notesmall10.png "Note")   Note

**How to read event log details for User Profile Service error:**

-   Open **Event Viewer** (eventvwr.msc), and expand open **Windows Logs** and **Application** in the left pane.
-   Right click or press and hold on **Application** in left pane, click/tap on **Find**, type **1511** for Event ID, and click/tap on **Find Next**.
-   Close the Find dialog, and view details. Repeat to view any other listed 1511 Event IDs if needed.\
![Fix You've been signed in with a temporary profile in Windows 10-event_viewer_user_profile_service_details.png](https://www.tenforums.com/attachments/tutorials/220427d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-event_viewer_user_profile_service_details.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-event_viewer_user_profile_service_details.png")

To be extra safe, it is recommended that you back up the contents of your "C:\Users\(user-name)" profile folder before doing the steps in this tutorial.

**EXAMPLE: ["We can't sign in to your account"](https://support.microsoft.com/en-us/help/4027881/windows-10-we-cant-sign-in-to-your-account) and "You've been signed in with a temporary profile" notifications**\
![Fix You've been signed in with a temporary profile in Windows 10-we_cant_sign_into_your_account.png.png](https://www.tenforums.com/attachments/tutorials/220431d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-we_cant_sign_into_your_account.png.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-we_cant_sign_into_your_account.png.png")\
![Fix You've been signed in with a temporary profile in Windows 10-youve_been_signed_in_with_a_temporary_profile.png](https://www.tenforums.com/attachments/tutorials/220438d1547137732-fix-youve-been-signed-temporary-profile-windows-10-a-youve_been_signed_in_with_a_temporary_profile.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-youve_been_signed_in_with_a_temporary_profile.png")

**Here's How:**

1 [**Restart the computer**](https://www.tenforums.com/tutorials/7370-restart-computer-windows-10-a.html) 4 times, each time letting your PC get to the Desktop before the next restart. This will often fix this issue a lot of the time. If not, then continue on to **step 2**.

2 While signed in to the account with the temporary profile, open a [**command prompt**](https://www.tenforums.com/tutorials/3288-open-command-prompt-windows-10-a.html).

3 Enter the command below into the command prompt, and press **Enter**.\
 `whoami /user`\
4 Make note of the [**SID (Security Identifier)**](https://www.tenforums.com/tutorials/84467-find-security-identifier-sid-user-windows.html) for this current account. You will need to know the SID (ex: S-1-5-21-....-1001) for your account in the steps below. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-get_sid_command.png](https://www.tenforums.com/attachments/tutorials/220428d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-get_sid_command.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-get_sid_command.png")\
5 If this account is a [**standard user**](https://www.tenforums.com/tutorials/21680-determine-account-type-windows-10-a.html), then you will need to [**sign out**](https://www.tenforums.com/tutorials/7408-sign-out-windows-10-a.html) and [**sign in**](https://www.tenforums.com/tutorials/61963-sign-windows-10-a.html) to an [**administrator**](https://www.tenforums.com/tutorials/21680-determine-account-type-windows-10-a.html) account to be able to continue on with the steps below.

If this account is an administrator, you will be able to continue on with the steps below.

If you do not have an administrator account available to sign in to, then you could boot into [**safe mode**](https://www.tenforums.com/tutorials/2304-boot-into-safe-mode-windows-10-a.html), enable the [**built-in Administrator**](https://www.tenforums.com/tutorials/2969-enable-disable-elevated-administrator-account-windows-10-a.html) system account, [**sign out**](https://www.tenforums.com/tutorials/7408-sign-out-windows-10-a.html), and [**sign in**](https://www.tenforums.com/tutorials/61963-sign-windows-10-a.html) to the **Administrator** account.

6 Press the `Win` + `R` keys to open Run, type **regedit** into Run, and click/tap on **OK** to open Registry Editor.

7 If prompted by [**UAC**](https://www.tenforums.com/tutorials/3577-change-user-account-control-uac-settings-windows-10-a.html), click/tap on **Yes**.

8 Navigate to the **ProfileList** key at the location below in the left pane of Registry Editor. (see screenshot below)\
 **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList**

![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-1.png](https://www.tenforums.com/attachments/tutorials/220432d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-1.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-1.png")\
9 In the left pane under the expanded **ProfileList** key, look to see if the **SID** key from [**step 4**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step4) above is listed **with** (ex: S-1-5-21-....-1001.bak) and/or **without** (ex: S-1-5-21-....-1001) **.bak** at the end. (see screenshot above)

10 Do [**step 11**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#11) (Only SID without .bak), [**step 12**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#12) (Only SID with .bak), or [**step 13**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#13) (SID without and with .bak) below depending on what you see in [**step 9**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step9) above.

11 If the SID key is only listed without .bak at the end\
A) In the right pane of the SID key (ex: S-1-5-21-....-1001), double click/tap on the **ProfileImagePath** value name to modify it. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png](https://www.tenforums.com/attachments/tutorials/220437d1547137732-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-b.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png")\
B) Enter the correct path (ex: C:\Users\Brink) of the user's profile folder, and click/tap on **OK**. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png](https://www.tenforums.com/attachments/tutorials/220434d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-3.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png")

You can see the name of user profile folders in the **C:\Users** folder. Usually the user profile folder will have the same name as the account name.

If the user profile folder for the account no longer exists (ex: deleted), then you could delete the SID key instead to have a new profile folder created, and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. This new profile folder will be like starting with a new account though.\
![Fix You've been signed in with a temporary profile in Windows 10-users.png](https://www.tenforums.com/attachments/tutorials/220430d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-users.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-users.png")\
C) In the right pane of the SID key (ex: S-1-5-21-....-1001), verify that the **State** DWORD is set with a value data of **0** (number zero), and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. (see screenshot below [**step 11A**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step11A))

If the **State** DWORD is not set to **0**, then double click/tap on the State DWORD to modify it, change the value data to **0**, and click/tap on **OK**.

![Fix You've been signed in with a temporary profile in Windows 10-state.png](https://www.tenforums.com/attachments/tutorials/220429d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-state.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-state.png")

12 If the SID key is only listed with .bak at the end\
A) Right click or press and hold on the SID key (ex: S-1-5-21-....-1001.bak), click/tap on **Rename**, and rename the SID key to only remove "**.bak**" (ex: S-1-5-21-....-1001) at the end of the key's name. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-.png](https://www.tenforums.com/attachments/tutorials/220436d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-.png")\
B) In the right pane of the SID key (ex: S-1-5-21-....-1001) now without .bak at the end, double click/tap on the **ProfileImagePath** value name to modify it. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png](https://www.tenforums.com/attachments/tutorials/220437d1547137732-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-b.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png")\
C) Enter the correct path (ex: C:\Users\Brink) of the user's profile folder, and click/tap on **OK**. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png](https://www.tenforums.com/attachments/tutorials/220434d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-3.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png")

You can see the name of user profile folders in the **C:\Users** folder. Usually the user profile folder will have the same name as the account name.

If the user profile folder for the account no longer exists (ex: deleted), then you could delete the SID key instead to have a new profile folder created, and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. This new profile folder will be like starting with a new account though.\
![Fix You've been signed in with a temporary profile in Windows 10-users.png](https://www.tenforums.com/attachments/tutorials/220430d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-users.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-users.png")

D) In the right pane of the SID key (ex: S-1-5-21-....-1001), verify that the **State** DWORD is set with a value data of **0** (number zero), and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. (see screenshot below [**step 12B**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step12B))

If the **State** DWORD is not set to **0**, then double click/tap on the State DWORD to modify it, change the value data to **0**, and click/tap on **OK**.

![Fix You've been signed in with a temporary profile in Windows 10-state.png](https://www.tenforums.com/attachments/tutorials/220429d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-state.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-state.png")

13 If the SID key is listed twice without and with .bak at the end\
A) Right click or press and hold on the SID key without .bak (ex: S-1-5-21-....-1001), and click/tap on **Delete**. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-2.jpg](https://www.tenforums.com/attachments/tutorials/220433d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-2.jpg?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-2.jpg")\
B) Click/tap on **Yes** to confirm. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-5.png](https://www.tenforums.com/attachments/tutorials/220435d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-5.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-5.png")\
C) Right click or press and hold on the SID key with .bak (ex: S-1-5-21-....-1001.bak), click/tap on **Rename**, and rename the SID key to only remove "**.bak**" (ex: S-1-5-21-....-1001) at the end of the key's name. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-.png](https://www.tenforums.com/attachments/tutorials/220436d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-.png")\
D) In the right pane of the SID key (ex: S-1-5-21-....-1001) now without .bak at the end, double click/tap on the **ProfileImagePath** value name to modify it. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png](https://www.tenforums.com/attachments/tutorials/220437d1547137732-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-b.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-b.png")\
E) Enter the correct path (ex: C:\Users\Brink) of the user's profile folder, and click/tap on **OK**. (see screenshot below)\
![Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png](https://www.tenforums.com/attachments/tutorials/220434d1547137726-fix-youve-been-signed-temporary-profile-windows-10-a-windows_10_temporary_profile_fix-3.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-windows_10_temporary_profile_fix-3.png")

You can see the name of user profile folders in the **C:\Users** folder. Usually the user profile folder will have the same name as the account name.

If the user profile folder for the account no longer exists (ex: deleted), then you could delete the SID key instead to have a new profile folder created, and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. This new profile folder will be like starting with a new account though.\
![Fix You've been signed in with a temporary profile in Windows 10-users.png](https://www.tenforums.com/attachments/tutorials/220430d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-users.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-users.png")

F) In the right pane of the SID key (ex: S-1-5-21-....-1001), verify that the **State** DWORD is set with a value data of **0** (number zero), and go to [**step 14**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step14) below. (see screenshot below [**step 13D**](https://www.tenforums.com/tutorials/48012-fix-youve-been-signed-temporary-profile-windows-10-a.html#step13D))

If the **State** DWORD is not set to **0**, then double click/tap on the State DWORD to modify it, change the value data to **0**, and click/tap on **OK**.

![Fix You've been signed in with a temporary profile in Windows 10-state.png](https://www.tenforums.com/attachments/tutorials/220429d1547137696-fix-youve-been-signed-temporary-profile-windows-10-a-state.png?s=b945ec43d88af7c80fb8c8c0f4713295 "Fix You've been signed in with a temporary profile in Windows 10-state.png")

14 Close Registry Editor.

15 [**Restart the computer**](https://www.tenforums.com/tutorials/7370-restart-computer-windows-10-a.html), and [**sign in**](https://www.tenforums.com/tutorials/61963-sign-windows-10-a.html) to the account that got the temporary profile error to see if it is now fixed.

If the account's profile is still not fixed, then repeat the tutorial again making sure that the **ProfileImagePath** value has the correct path for the account's user profile folder (ex: C:\Users\Brink).

If the profile just cannot be fixed, then you can use [**option 2 here**](https://www.tenforums.com/tutorials/145678-fix-user-profile-service-failed-sign-error-windows-10-a.html#option2) to create a new profile for the account, and copy over any files you want from the old profile folder to the new one afterwards.