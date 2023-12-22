
# Azure Network Monitoring Tool

This tool allows you to perform various operations related to Azure network monitoring using the Azure SDK for Python. It leverages Azure Identity and Azure Resource and Network Management libraries to interact with Azure services.
<img width="1710" alt="Screenshot 2023-12-20 at 2 59 42 PM" src="https://github.com/cobrakai2007/FRTPROJECT/assets/154581587/8eeac399-90ba-4729-99a1-61d05afee4e5">


## Azure Services Usage

This tool utilizes several Azure services to streamline Azure networking management:

### 1. Azure Identity

The script uses [Azure Identity](https://docs.microsoft.com/en-us/python/api/azure-identity/) to handle secure authentication to Azure services. This ensures that the interactions with Azure resources are authenticated securely.

### 2. Azure Resource Management

[Azure Resource Management](https://docs.microsoft.com/en-us/python/azure/python-sdk-azure-resource?view=azure-python) is employed to manage Azure resources programmatically. The script leverages this library to create and manage Azure resources such as virtual networks and network watchers.

### 3. Azure Network Management

The [Azure Network Management](https://docs.microsoft.com/en-us/python/api/azure-mgmt-network/azure.mgmt.network?view=azure-python) library facilitates the configuration and monitoring of Azure network components. The tool uses this library to create virtual networks, establish network watchers, and manage packet capture activities.

### 4. Azure Functions App

To enhance the accessibility of the Azure Networking Tool, we've integrated it with Azure Functions.

### 4. Matplotlib

[Matplotlib](https://matplotlib.org/) is a widely used plotting library in Python. It plays a crucial role in the project by enabling the generation of dynamic graphs that visually represent the number of packet captures over time. This feature enhances user comprehension and aids in performance analysis, security insights, and capacity planning.


## Prerequisites

Before using this tool, make sure you have the following prerequisites installed:

- Python 3.x
- Azure Identity (`pip install azure-identity`)
- Azure Management (`pip install azure-mgmt-network azure-mgmt-resource`)
- matplotlib (`pip install matplotlib`)

## Configuration

Before running the tool, make sure to set the following configuration parameters in the script:

- Subscription ID (`subs_id`)
- Resource Group (`resource_group`)


## Features

### 1. **Create Virtual Network**
<img width="1710" alt="Screenshot 2023-12-20 at 3 01 01 PM" src="https://github.com/cobrakai2007/FRTPROJECT/assets/154581587/375d7559-8256-43ae-acf4-a54d99f5fcc9">

Effortlessly create a virtual network with a specified name and IP range. This feature streamlines the process of establishing the foundation for your Azure network architecture.

### 2. **Create Network Watcher**
<img width="1710" alt="Screenshot 2023-12-20 at 3 11 46 PM" src="https://github.com/cobrakai2007/FRTPROJECT/assets/154581587/23f731bf-48d8-4eaf-84dd-b22e24c9773d">

Establish a network watcher with a user-defined name, providing a crucial component for monitoring and diagnosing network issues in your Azure environment.

### 3. **Get Packet Capture**
<img width="1710" alt="Screenshot 2023-12-20 at 3 06 25 PM" src="https://github.com/cobrakai2007/FRTPROJECT/assets/154581587/e3b342c9-4eb7-4c8a-bbb6-92cb137a9762">

Retrieve detailed information about packet captures, including their start time. This feature is invaluable for analyzing network traffic patterns and identifying potential issues.

### 4. **Delete Packet Capture**
Enhance control over your network monitoring data by selectively deleting packet captures. This function ensures efficient data management and compliance with your organization's policies.

### 5. **Generate Graph**
<img width="1710" alt="Screenshot 2023-12-20 at 3 08 29 PM" src="https://github.com/cobrakai2007/FRTPROJECT/assets/154581587/1a2b1f3e-297d-489a-81ce-c72ca8e6d032">

Unleash the power of data visualization with the graph feature. This dynamically generated graph showcases the number of packet captures over time. Real-life implications of this feature include:

- **Performance Analysis:** Understand how network activity fluctuates over time, enabling proactive performance optimization.
  
- **Security Insights:** Identify irregularities or spikes in packet captures, aiding in the detection of potential security threats or anomalies.

- **Capacity Planning:** Plan network resources effectively by analyzing historical data trends and making informed decisions about scaling resources.


## Usage

```bash
python azure_network_monitoring_tool.py [options]
```

Options:
- `create virtual network`: Create a virtual network.
- `create network watcher`: Create a network watcher.
- `get packet capture`: Retrieve packet capture details.
- `delete packet capture`: Delete a packet capture.
- `graph`: Create a graph for the number of packet captures over a virtual network against time

## Examples

```bash
# Create a virtual network
python azure_network_monitoring_tool.py create virtual network

# Create a network watcher
python azure_network_monitoring_tool.py create network watcher

# Get packet capture details
python azure_network_monitoring_tool.py get packet capture

# Delete a packet capture
python azure_network_monitoring_tool.py delete packet capture
```


