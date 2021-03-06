
# Frequently Questions

## 1. How to get AccessKey and SecretKey?

Refer to JD Cloud OpenAPI Help page for pre-condition sections: https://www.jdcloud.com/help/detail/355/isCatalog/0



## 2. How do I select RegionId?

Refer to the JD Cloud OpenAPI Help page for the local coding section:https://www.jdcloud.com/help/detail/355/isCatalog/0



## 3. Does the CLI command line open source?

JD Cloud CLI is open-source and can be downloaded from GitHub. Address: https://github.com/jdcloud-api/jdcloud-cli



## 4.    What happens when you return an error?

Print details using the overview option debug and feed back to the destination of the GitHub library of the JD Cloud CLI, or open a ticket in JD Cloud.

Example:

	jdc --debug command sub-command
   

## 5.    Is the CLI paid?

No charge for now.



## 6.    How to do feed back and help when you encounter problems?

Open a ticket in JD Cloud Console

Refer to JD Cloud official network for feedback on the way provided by our page. The address is: https://www.jdcloud.com/help/detail/129/isCatalog/1

Submit Issue at GitHub, Address: https://github.com/jdcloud-api/jdcloud-cli/issues



## 7.    How to Install JD Cloud Python SDK?

pip Installation


	pip install jdcloud_sdk
 This command installs the latest version, specifies a version installation, please refer to the following example. The CLI is installed at the same time and is not described in detail.

	pip install jdcloud_sdk==1.1.2
   

Source Code Installation

Download Address: https://github.com/jdcloud-api/jdcloud-sdk-python

After unzip, it is performed in the project directory:

	python setup.py install
It is recommended that a stable version of the release be downloaded as the version number.