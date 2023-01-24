7 Fixes for the Outlook Stuck on Loading Profile Problem
========================================================

BY[AMIR M. BOHLOOLI](https://www.makeuseof.com/author/amir-bohlooli/?_locale=en)

UPDATED APR 18, 2022

Are you experiencing problems with Outlook's loading profiles screen? Check out these solutions and fix this issue.

Microsoft's Outlook is a great asset and offers an arsenal of features. With Outlook, you get an email, calendar, contacts, and much more, all in a single app. Yet, like all other apps, Outlook isn't flawless and runs into issues at times.

One of these issues is when you can't open the app, and it gets stuck on the Loading Profile screen. This can be quite frustrating, as you can't even get into the app to figure out what's wrong with it. Fortunately, this issue also has a remedy. Getting stuck on Loading Profile can be a result of several problems, and there are plenty of solutions for it.

1\. Run Outlook as an Administrator
-----------------------------------

Though Outlook usually doesn't need admin access to function, there's a chance that your problem might be because of Outlook's lack of permission to access the profile. In that case, running Outlook as administrator will fix things up.

1.  In the search bar, type in **Outlook**.
2.  In the search results, **right-click** on Outlook and then select **Run as administrator**.
3.  Click **Yes** in the dialog asking for confirmation. This will run Outlook as administrator.

2\. Disconnect Your Device From the Internet
--------------------------------------------

Outlook might be trying to access something online and failing. This can be a possible cause, as Outlook can't finish loading the profile, so it'll stay stuck on the Loading Profile screen.

The workaround for this is to force Outlook into offline mode by cutting off your internet connection. Cutting off your internet every time you want to open Outlook is obviously not a solution, but this gives you a chance to get inside Outlook and alter the settings that might be causing the issue.

### Disconnecting Wi-Fi

1.  Click the notification icon in the bottom right to open the **Action Center**.
2.  In the Action Center, click on **Network**.
3.  Click on **Wi-Fi** to turn it off. Enabling **Airplane Mode** will also turn off Wi-Fi.

### Disconnecting LAN

The simplest way to disconnect your LAN connection is to just unplug the Ethernet cable from your computer. However, if the Ethernet port is inaccessible, or you don't want to physically unplug anything, you can disable the Ethernet adapter from the control panel instead.

1.  Open the **Start menu**, then search for **Control Panel**.
2.  Select **Control Panel** from the search results.
3.  In Control Panel, go to **Network and Sharing Center**.
4.  In the left bar, click on **Change adapter settings**.
5.  Right-click on your Ethernet adapter and then select **Disable**. This will disconnect your LAN connection. You can enable the connection by right-clicking the adapter and selecting **Enable**.

3\. Kill Office-Related Processes in Task Manager
-------------------------------------------------

Restarting Outlook might not be completely effective if other Office-related services are still running. To ensure a fresh start for everything, you can kill the Office-related processes in Task Manager.

1.  Press **Ctrl** + **Shift** + **Esc** on your keyboard to bring up the Task Manager.
2.  Find Office-related processes, select them, and then click **End Task**. This includes other Office apps and Office processes such as **Click-to-Run**.
3.  Launch **Outlook**.

4\. Turn Off Hardware Acceleration
----------------------------------

Hardware acceleration is a built-in feature in Outlook designed to increase the overall efficiency of the program. However, if you're using Outlook on older hardware, this can cause problems and, in some cases, can make Outlook unusable.

Luckily, you can solve this problem by running Outlook in safe mode and then disabling hardware acceleration.

1.  On your keyboard, press **Win** + **R** to bring up **Run**. You can also search for Run in the Start menu.
2.  Type the **following code** in the text box and press **Enter**:

    Outlook.com /safe

    This will open Outlook in safe mode.
3.  In Outlook, click the **File** tab and then head to **Options**.
4.  In the Outlook Options window, go to the **Advanced** tab.
5.  Scroll down to **Display**, and check **Disable hardware graphic acceleration**.
6.  Click **OK**.
7.  Close Outlook and launch it without safe mode.

If you couldn't run Outlook in safe mode due to account restrictions, read our in-depth guide on [how to start Outlook in safe mode](https://www.makeuseof.com/outlook-safe-mode/).

5\. Repair Corrupted Outlook Files
----------------------------------

Outlook won't function properly and could get stuck in the Loading Profile screen if one or more of its files are corrupted. Outlook files can be repaired using an executable in the Outlook installation directory.

1.  Right-click the Outlook shortcut, then select **Properties**. This will open the Properties window.
2.  In the **Shortcut** tab, click on **Open File Location**. This will open the installation directory.
3.  Locate **SCANPST.EXE** and then open it. The Microsoft Outlook Inbox Repair Tool will open and ask for a file to scan and repair.
4.  Click on **Browse** and then navigate to the directory below:

    ```
    C:\Users\*username*\AppData\Local\Microsoft\Outlook
    ```

    Replace *username* with your own username.
5.  Select the profile you want to repair, then click on **Start**. The profiles are stored as **OST **files. The program will now start scanning the file for errors.
6.  Once SCANPST is finished scanning and repairing, click **OK**.
7.  Launch Outlook.

If you couldn't get SCANPST to work, read our thorough article on [how to repair corrupted PST and OST files in Outlook](https://www.makeuseof.com/how-to-repair-corrupted-pst-and-ost-files-in-microsoft-outlook-using-recovery-toolbox/).

6\. Fix Office Files That Are Corrupted
---------------------------------------

Outlook is, after all, a part of Microsoft's Office, and successfully repairing Office will also fix the Outlook issues. You don't need to install any additional software to repair Office. You can achieve this repair through the control panel.

1.  Find **Control Panel** using the search bar.
2.  In Control Panel, select **Programs and Features**.
3.  From the list, find Microsoft Office and select it.
4.  Click on **Change**. This will open a window.
5.  Select **Quick Repair** and then click **Repair**.

Once the repair process is complete, launch Outlook and see if the issue is resolved. If not, repeat the process and conduct the Online Repair.

7\. Create a New Outlook Profile
--------------------------------

If none of the solutions above worked for you, it's possible that your Outlook profile is corrupted beyond possible recovery. Creating a new profile and making it the default is the only way to fix this problem.

1.  Select **Control Panel** from the search results.
2.  In Control Panel, find and select **Mail**. This will bring up the Mail Setup window.
3.  In the Mail Setup window, click on **Show Profiles**. This will open another window.
4.  Click on **Add**.
5.  Type in a name for your new profile.
6.  Configure your email settings, then click **Next**. Outlook will check and connect to the mail servers.
7.  Once your new profile is set, change **Always use this profile** from Outlook to your new profile.
8.  Click **OK** and then launch Outlook.