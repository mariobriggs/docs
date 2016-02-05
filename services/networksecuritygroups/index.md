# Getting started with IBM Network Security Groups (BETA)

A security group is a set of IP filter rules. You can configure {{site.data.keyword.networksecuritygroups_full}} for virtual machines (VMs) and VM groups. The service is available at IBM Bluemix&reg; > Catalog > Services > Network > Network Security Groups.

The following security groups are provided in Bluemix for IBM Virtual Machines:

* **allow_ssh**: This security group defines the IP rules that allow incoming TCP traffic on the SSH port only (22/TCP).  
* **allow_https**: This security group defines the IP rules that allow incoming TCP traffic on HTTPS port only (443/TCP).  
* **allow_rdp**: This security group defines the IP rules that allow incoming TCP traffic on remote desktop client port only (3389/TCP).  
* **allow_all**: This security group defines the IP rules that allow all incoming traffic on all ports.  
* **default**: This security group defines the IP rules that deny all incoming traffic from outside the private network.  

You can define up to 10 security groups for a space in your organization. These security groups include the five predefined security groups. 

### Adding IBM Network Security Groups Service
1. Select IBM Bluemix > Catalog > Services > Network. You will see the available network services.
2. Select **Network Security Groups** service. You will see the service description, available plans, and pricing details. 
3. Select a suitable plan. 
4. Select options in the Add Service section:  
	* **Space:**  
	* **App:**  
	* **Service Name:**
5. Select **CREATE**. The service instance is created.

### Creating a Security Group

**Note:** Use only Google Chrome 47.0.2526 or Mozilla Firefox 38.5.2 browser to create and configure IBM Network Security Groups.

1. Select IBM Bluemix > Dashboard > Services > Network Security Groups service instance tile. You will see the **Network Security Groups** page.  
![](images/service_page.png)

2. Select **CREATE SECURITY GROUP +**.  
![](images/create.png)  
3. Provide the following information:
	* **Security Group Name**: Enter a name for your security group.
	* **Instance Type**: Select the instance type for which you want to create the security group. Value: Virtual Machines.  
	* **Description**: Enter a description of your security group.

4. Select **SAVE**. The security group is created.

### Configuring Rules

You can configure rules to manage inbound traffic (ingress traffic) to a VM or VM group instance, and outbound traffic (egress traffic) from a VM or VM group instance. 

1. Select the security group for which you want to configure the rules.  
![](images/select_group.png)  
2. Select **Inbound Rules** or **Outbound Rules**, as required.
3. Select **ADD RULE**.  
![](images/add_rule.png)
4. Specify inbound or outbound rules:  
	![](images/rules.png)  
	* **Type:** Select IPv4.  
	* **Protocol:** Select the protocol from the drop-down list. If you want to specify a protocol that is not in the list, select **Other protocol** from the drop-down.  
	![](images/other_protocol.png)  
	Provide the following information:  
	  * **Protocol value:** The IP number of the protocol. For example: You enter 1 for ICMP protocol.  
	* **Port:** or **Port Range:** The port configuration parameter depends on the protocol you select.  
		* If you select **ALL ICMP**, **ALL TCP**, or **ALL UDP**, no port information is required.  
		* If you select a single protocol, the port number is automatically displayed. For example: If you select **HTTP**, port **80** is displayed.  
		* If you select **Custom TCP Rule** or **Custom UDP rule**, select a port type. Values: ANY, Port, port range. If you select **Port**, enter the port number; if you select **Port range**, enter the range of port numbers.  
		* If you select **Custom ICMP Rule**, enter the ICMP **Code** and **Type**.
	* **Select source type:** Select **IP** or **SG** or **VM**.  
		* If you select **IP**, enter an IP address in the **Source IP** or **Destination IP** field.  
		* If you select **SG**, select a security group from the **Source SG** or **Destination SG** drop-down. The list displays all the configured security groups, including the default security group.  
		* If you select **VM**, select a VM from the **Source VM** or **Destination VM** drop-down.

###Assigning Instances

Select VM or VM group instances to which you want to assign the security group.  

####Assign VM Instances

1. Select **Assigned Instances**.  
![](images/assign_vm.png)  
2. Select **ASSIGN INSTANCE +**.  
![](images/assign_icon.png)  
3. Select the VM instances as required.  
![](images/select_instance.png)  
4. Select **ADD**.
	
####Assign VM Groups

1. Select **Assigned Groups**.  
![](images/assign_group.png)
2. Select **ASSIGN GROUP +**.  
![](images/assign_group_icon.png)  
3. Select the VM groups as required.  
![](images/select_group_instance.png)
4. Select **ADD**.

###Deleting a Security Group

1. Select IBM Bluemix > Dashboard > Services > Network Security Groups service instance tile. You will see the list of security groups on the **Network Security Groups** page.  
![](images/select_group.png)
2. Expand the security group that you want to delete.
![](images/delete_sg.png)
3. Select **DELETE**.


># Related Links {:class="linklist"}
>## Related Links {:id="general"}  
>* [IBM Network Security Groups Command Line Interface](../../cli/plugins/networksecuritygroups/index.html)
>
>{:elementKind="article" id="rellinks"}
