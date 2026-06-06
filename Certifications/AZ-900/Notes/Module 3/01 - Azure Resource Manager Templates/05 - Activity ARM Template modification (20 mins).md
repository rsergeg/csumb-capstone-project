## Activity Solution Notes

**ARM Template Structure Explanation**

### Overall Structure

This ARM template is a JSON file used to deploy Azure resources. It defines the template version, configurable deployment values, reusable variables, resources to create, and optional outputs.

The main sections are:

- $schema
- contentVersion
- parameters
- variables
- resources
- outputs

---

### $schema

`"$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"`

The $schema property identifies the ARM template schema being used. It tells Azure Resource Manager and tools like Visual Studio Code how to validate and interpret the file.

---

### contentVersion

`"contentVersion": "1.0.0.0"`

The contentVersion property defines the version of the template itself. This helps track changes when the template is updated over time.

---

### parameters

The parameters section defines values that users can provide during deployment. This makes the template reusable and customizable.

This template includes three parameters:

**vmSize**  
Defines the size of the virtual machine. It has:

- Type: string
- Default value: Standard_DS1_v2
- Allowed values: Standard_DS1_v2 and Standard_DS2_v2

**adminUsername**  
Defines the administrator username for the virtual machine.

**adminPassword**  
Defines the administrator password for the virtual machine. It uses securestring, which protects the password from being exposed as plain text.

---

### variables

`"subnetRef": "[resourceId('Microsoft.Network/virtualNetworks/subnets', 'myVNet', 'mySubnet')]"`

The variables section stores reusable values used inside the template.

In this template, subnetRef stores the resource ID for the subnet named mySubnet inside the virtual network named myVNet.

---

### resources

The resources array defines the Azure resources that will be deployed.

This template creates two resources:

- A virtual machine named myVM
- A network interface named myNIC

---

### Virtual Machine Resource

The virtual machine resource uses:

`"type": "Microsoft.Compute/virtualMachines"`

This tells Azure that the resource being deployed is a virtual machine.

Important VM settings include:

- apiVersion: Specifies the Azure API version used for the VM
- name: Names the VM myVM
- location: Deploys the VM in the same location as the resource group
- hardwareProfile: Sets the VM size using the vmSize parameter
- osProfile: Sets the computer name, admin username, and admin password
- storageProfile: Uses a Windows Server 2019 Datacenter image
- networkProfile: Connects the VM to the network interface named myNIC

---

### Network Interface Resource

The network interface resource uses:

`"type": "Microsoft.Network/networkInterfaces"`

This tells Azure that the resource being deployed is a network interface card, or NIC.

Important NIC settings include:

- apiVersion: Specifies the Azure API version used for the NIC
- name: Names the NIC myNIC
- location: Deploys the NIC in the same location as the resource group
- ipConfigurations: Defines the NIC’s IP configuration
- subnet: Connects the NIC to the subnet referenced by subnetRef

---

### outputs

`"outputs": {}`

The outputs section is empty in this template. Outputs can be used to return useful information after deployment, such as a public IP address, VM name, or resource ID.

---

### Key Takeaway

This ARM template deploys a basic Azure virtual machine and network interface. Parameters make the template flexible, variables simplify repeated references, and the resources section defines the actual Azure infrastructure to be created.