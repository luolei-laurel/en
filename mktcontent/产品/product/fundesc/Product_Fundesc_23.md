[
	{
		"funcName":"Customized Network",
		"funcContent":[
			{
				"funcName":"",
				"funcTitle":"Customize VPC ranges and sub-network segments",
				"funcP":"Users can customize the network segment of a VPC, and then further divide the VPC into multiple subnets, and deploy applications and services on the corresponding network to meet various application scenarios."
			}
		]
	},
	{
		"funcName":"Customized Routing",
		"funcContent":[
			{
				"funcName":"",
				"funcTitle":"Editable routing function",
				"funcP":"Users can configure the next hop type, next hop and destination of the routing rule in the Route Table according to the service requirements. After the Route Table is associated with a subnet, the management of the network traffic forwarding path can be achieved."
			}
		]
	},
	{
		"funcName":"Comprehensive Security Control",
		"funcContent":[
			{
				"funcName":"",
				"funcTitle":"Realize multi-level security protection through security groups and network ACLs",
				"funcP":"Network ACL: When operating at the subnet level, it supports the allow rule and the deny rule. Data flow return must be explicitly allowed by the rules. \n Security group: When operating at the instance level, it only supports the allow rule. Data flow return is automatically allowed, not affected by any rule."
			}
		]
	},
	{
		"funcName":"Flexible Access to EIP",
		"funcContent":[
			{
				"funcName":"",
				"funcTitle":"EIP and self-built NAT gateway for public network access",
				"funcP":"If the resources in VPC have requirement to visit the Internet, EIP access can be realized by binding the elastic EIP or self-building the NAT gateway and configuring corresponding routing policy."
			}
		]
	}
]