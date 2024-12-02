# Visualization with Ignition Edge Using Data from KepserverEX  
*Theme*: Simulation and visualization of data by integrating KepserverEX with Ignition Edge through an OPC UA server and storing data in the Edge Historian.

## Prerequisite  
* Download and install **Ignition Edge** from [this link](https://inductiveautomation.com/downloads).  
* Download and install **KepserverEX** from [this link](https://my.kepware.com/s/login/SelfRegister) for a free trial.  
* Ensure that both Ignition and KepserverEX are properly licensed or running in trial mode.

## Step 1: Configuring KepserverEX  
1. **Create or Open a Project**  
   * Open an existing project (e.g., **Oil_Industry.opf**) or create a new one in KepserverEX.  
2. **Add an OPC UA Endpoint**  
   * Navigate to **Settings** > **OPC UA Configuration** and enable the OPC UA server.  
   * Note the **Endpoint URL** (e.g., `opc.tcp://<your_ip>:49320`).  
3. **Create Tags**  
   * Add devices and configure tags as needed. Ensure the tags have the appropriate data types and addresses.

## Step 2: Configuring Ignition Edge  
1. **Enable Perspective Module**  
   * Open Ignition Edge’s **Gateway** (default URL: `http://localhost:8088`).  
   * Go to **Config** > **System**.  
   * Under the **Visualization Module** section, select **Perspective** from the dropdown menu (default is **Vision**).  
   * Click **Save Changes** to apply the new settings.  

2. **Connect to the OPC UA Server**  
   * Go to **Config** > **OPC Connections** > **Create New OPC Server Connection**.  
   * Select **OPC UA** and enter the KepserverEX OPC UA endpoint URL.  
   * Authenticate with the same credentials used in KepserverEX’s OPC UA configuration.  

3. **Add Tags to Edge Historian**  
   * Open the **Tag Browser** from the **Gateway** under the **Edge Historian**.  
   * Enable tag history by configuring storage settings and mapping tags to be logged in the **Edge Historian** database.  

## Step 3: Creating Dashboards in Ignition Perspective  
### Switch to Perspective in Ignition Edge's Gateway  
1. **Navigate to the Gateway**  
   * Open the **Ignition Edge Gateway** (default URL: `http://localhost:8088`).  
   * Go to **Config** > **System**.

2. **Select Perspective Module**  
   * Under the **Visualization Module** section, change the setting to **Perspective**. (Note: This ensures that the Perspective module is used for client visualization instead of the default **Vision** module).  
   * Click **Save Changes** to apply the new settings.  

3. **Launch Designer**  
   * Once Perspective is selected, open the **Ignition Designer** (this will open the Designer application for working with Perspective views).  
   * From the **Designer**, you can start creating the dashboard components for visualization.

4. **Create a Dashboard**  
   * Use the **Perspective** workspace to design your dashboard. Add components such as **Power Chart**, **LED Display**, or **Labels** to visualize historical and real-time data.

5. **Bind Tags to Components**  
   * Bind the tags created in the previous steps (from Edge Historian) to the components in the dashboard to display the live and historical data.

6. **Save and Publish**  
   * Save your project and publish it to make it accessible via a web browser.

## Notes  
* Ensure that both Ignition Edge and KepserverEX are running before starting visualization.
* For sample dashboard refer to the "Sample_Ignition_Dashboard".   
* For troubleshooting and deeper configuration, refer to the "Documentation.pdf" and "Flowchart.jpg."
