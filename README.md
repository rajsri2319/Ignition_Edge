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
1. **Connect to the OPC UA Server**  
   * Open Ignition Edge’s **Gateway** (default URL: `http://localhost:8088`).  
   * Go to **Config** > **OPC Connections** > **Create New OPC Server Connection**.  
   * Select **OPC UA** and enter the KepserverEX OPC UA endpoint URL.  
   * Authenticate with the same credentials used in KepserverEX’s OPC UA configuration.  
2. **Add Tags to Edge Historian**  
   * Open **Ignition Designer** and go to the **OPC Browser**.  
   * Browse the connected KepserverEX server and drag the required tags into the **Tag Browser**.  
   * Right-click the tags and select **Edit Tag** > **History** tab.  
   * Enable **Tag History** and select the **Edge Historian** as the storage provider.  

## Step 3: Creating Dashboards in Ignition Perspective  
1. **Design a Dashboard**  
   * In Ignition Designer, switch to the **Perspective** workspace.  
   * Drag and drop components such as **Power Chart**, **LED Display**, or **Labels** into a view.  
2. **Bind Tags to Components**  
   * Bind the components to the historian tags added earlier to visualize historical data trends.  
3. **Save and Publish**  
   * Save the project and publish it for web-based access.  

## Notes  
* Ensure that both Ignition Edge and KepserverEX are running before starting visualization.  
* For troubleshooting and deeper configuration, refer to the "Documentation.pdf" and "Flowchart.jpg."

