About:
------
	This package has set of examples to understand how to use HMC REST APIs. For each operation it has a Python module. Target audiance are the user interested in exploiting the HMC REST APIs. The objective is to provide a starter kit for creating REST clients. The users can take the source code and modify it according to their needs.
	
Disclaimer:
-----------
	These examples are shared as is and they not fomrally supported by IBM or any of the authors and contributors. User assumes complete ownership and responsibility upon executing them.
	
Installation:
-------------	
	"python setup.py install" - the script files will be created in {Python installation directory}/scripts
	"python setup.py install --install-scripts={Target location}" -the script files will get created in the specified location.

Requirements:
-------------
	Power Hardware Management Console Version 8 Release 8.2
	Python Version >= 3.4.2
	Python Libraries:
		Requests version >= 2.5.3
		PyXB version = 1.2.4
		feedparser version >= 5.1.3

Execution:
----------
	Go to the install script directory and execute "HmcRestClient" from the command prompt. It starts interactive command line interface with main menu with options like ManagedSystem, Cluster, Performance and capacity monitoring, Help, etc. 

	The ManagedSystem have options for ManagedSystem operations such as List, PowerOn, PowerOff, RemoveConnection. It also has its child objects LogicalPartition, VirtualIOServer, NetworkBridge, VirtualNetwork, VirtualSwitch, SRIOVEthernetPhysicalPort, etc.
	
	Each option provides the operation on that object such as List, Create, Modify, Delete.
	
	List operation on objects provides the details of the object. The operations such as Create, Modify requires set of values. The source code has the values hard coded into it. Before performing these operations the user should check and if required set appropriate values in the source code. E.g.
	1. Create LogicalPartition module creates partition with min, max and desired memory 256MB and shared processor in capped mode.
	2. List operation on LogicalPartition lists logical partition name, its state, memory attributes, shared/dedicated processor, partition type and uuid.

	Performance and Capacity Monitoring have options enabling/disabling performance monitoring on a managed system. It also has options for downloading the JSON files of Long term, Short term and Processed Metrics.

	Help option gives the overview of each usecase.


Reference to useful resources:
------------------------------
PowerHMC developerworks community: https://www.ibm.com/developerworks/community/groups/community/powerhmc
Link to PowerVM Python SDK: https://github.com/pypowervm/pypowervm
