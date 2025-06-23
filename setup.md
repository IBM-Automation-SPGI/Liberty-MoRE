**Modernized Runtime Extension (MoRE) Demo setup guide**

This demo script walks through the prerequisite steps to setup demo environment for the MoRE demo.

MoRE provides the capability to continue using traditional WebSphere Application Server (tWAS) Operational Model to manage Java 17 and Java 8 applications within the same traditional WebSphere administrative environment

1.  Reserve demo environment

> The demo environment runs in IBM techzone via VMware on IBM Cloud. You can reserve the environment using the steps below:

a.  Launch the IBM Technology Zone **Create a reservation** URL:

> <https://techzone.ibm.com/my/reservations/create/67d484e5d2cb378858943c9b>

b.  Use your **IBM ID** to login to the IBM Technology Zone, the **Create a reservation** page is displayed.

c.  Select "**Reserve for Now**" Radio button.

> ![](./media_setup/media/image1.png){width="4.218222878390201in" height="2.5413484251968503in"}

d.  Follow the on-screen dialog to reserve an environment in IBM Cloud data center in the closest Geography (US-Central, EMEA, Asia Pacific).

- The environment **name** should be pre-filled with "**Managed Liberty MoRE-AMA-WCA environment-3.15.2025**"

- **Purpose**: Practice / Self-Education or Demo

  - **Note:** If choosing Demo as the purpose, you must also include a valid ***sales opportunity number***.

- **Description**: Enter a description. The is a required field

- **Preferred Geography**: Choose an IBM Cloud datacenter in the closest geography (US, EMEA, Asia Pacific)

- **End date and time**: Use the calendar widget and select the maximum date available and select a time of day for reservation to expire and select a **timezone** nearest to you.

<!-- -->

- **VPN Access**: Select **Disable** from the dropdown list.

  a.  Once complete, check the agreement box (A) and click on the "**Submit**" button (B).

> ![A screenshot of a computer error Description automatically generated](./media_setup/media/image2.png){width="3.790489938757655in" height="2.2079604111986in"}

b.  The reservation could take 30 minutes or more to become available. You can check its status by selecting **My library** (A) then clicking **My reservations** (B) in Techzone.

> ![A screenshot of a computer Description automatically generated](./media_setup/media/image3.png){width="4.009635826771653in" height="2.7729035433070868in"}
>
> When the environment is ready for use, it's status will indicate **Ready**.
>
> ![A screenshot of a computer AI-generated content may be incorrect.](./media_setup/media/image4.png){width="2.9371325459317585in" height="3.937007874015748in"}

2.  Access demo environment.

<!-- -->

a.  When the demo environment is ready, click the "**Open this Environment**" link on the reservation tile.

> ![A screenshot of a computer AI-generated content may be incorrect.](./media_setup/media/image5.png){width="2.539851268591426in" height="3.404481627296588in"}

b.  In the reservation details page, click the **Published services noVNC** URL link to open the URL in a new browser window.

> ![A close-up of a computer screen AI-generated content may be incorrect.](./media_setup/media/image6.png){width="4.374453193350831in" height="0.9894597550306212in"}

c.  Click the **Connect** button (A).

> ![A screenshot of a computer Description automatically generated](./media_setup/media/image7.png){width="3.130942694663167in" height="2.164695975503062in"}

d.  Enter the password as: **IBMDem0s!** (A). Then click the **Send Credentials** button (B) to access the lab environment.

> **Note**: That is a numeric zero in IBMDem0s!
>
> ![A screen shot of a login box Description automatically generated](./media_setup/media/image8.png){width="2.61873687664042in" height="1.9505818022747157in"}
>
> Once you log in to the Demo VM, you will see the Desktop, which contains all the programs that you will be using (browsers, terminal, etc.)
>
> The login credentials for the **student** VM are:

- User ID: **techzone**

- Password: **IBMDem0s!**

> ![A screenshot of a computer Description automatically generated](./media_setup/media/image9.png){width="5.125761154855643in" height="3.3662456255468065in"}

3.  Tips for working in the Demo environment

<!-- -->

a.  You can resize the viewable area using the **noVNC Settings** options to resize the virtual desktop to fit your screen.

    i.  From the Demo VM, click the **twisty** on the noVNC control pane (A) to open the menu. 

> ![A screen shot of a video game Description automatically generated](./media_setup/media/image10.png){width="2.388888888888889in" height="2.111111111111111in"}

ii. To increase the visible area, click the **Settings** icon (A) and select **Remote Resizing** from the **Scaling Mode** (B).

> ![A screenshot of a computer Description automatically generated](./media_setup/media/image11.png){width="3.3178958880139984in" height="3.2971587926509187in"}

b.  You can copy / paste text from the Demo guide into the Demo environment using the clipboard in the noVNC viewer. 

    a.  Copy the text from the Demo guide that you want to paste into the Demo environment.

    b.  Click the **Clipboard** icon (A) and **paste** the text into the noVNC clipboard (B).

> ![A screenshot of a computer Description automatically generated](./media_setup/media/image12.png){width="4.219089020122484in" height="2.6824562554680664in"}

c.  Paste the text into the VM, such as to a terminal window, browser window, etc. 

d.  Click on the **clipboard** icon again to close the clipboard

<!-- -->

4.  Start the WebSphere environment

    a.  Start the deployment manager

> /home/techzone/IBM/WebSphere/AppServer/bin/startManager.sh

b.  Start the node agent

> /home/techzone/IBM/WebSphere/AppServer/profiles/AppSrv01/bin/startNode.sh

c.  Login to the WebSphere Admin Console

- Launch Chrome Browser in the demo environment

- Go to: <https://localhost:9043/ibm/console>

- Enter credentials as:

  - Use ID: techzone

  - Password: IBMDem0s!

**Note:** If you open the browser, you might get a pop-up that Authentication is required.

In that case enter **IBMDem0s!** and click on **Unlock**.

![](./media_setup/media/image13.png){width="4.34375in" height="2.8229166666666665in"}

**Start AMA in the demo environment**

1.  Change to the directory where AM is installed

cd /home/techzone/ama/ta_local_dev/build/distributions/application-modernization-accelerator-local-4.1.0

 

2.  Launch AMA

> ./launch.sh

3.  Select option **#5** to START AMA

4.  From the Web Browser on the VM, open AMA using the URL below:

> http://localhost:3000
>
> The demo environment setup is complete.
>
> **\<END OF DOCUMENT\>**
