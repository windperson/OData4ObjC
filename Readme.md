OData4ObjC
==================
OData4ObjC is an open-source toolkit to access and manipulate OData in Objective C.

This SDK supports up to iOS 6.


SetUp Instructions
==================
* Dowload latest zip edition
* Unzip folder and move to suitable location (ex: Documents folder, renamed folder to ODataSDK)

Set-up XCode:
* Open XCode project
* Add framework "libMSODataLib.a" (ex: found at ODataSKD/Framework/bin/odatalib/lib/iPhoneDeviceLibs/iPhone_Device_6.1/release )
* Add Search Paths
	- Select Project
	- Select project under TARGETS
	- Go to Build Settings -> Search Paths
	- Add include folder to "Header Search Paths" and choose recursive
	  (ex: "$(SRCROOT)/../../../../Documents/ODataSDK/Framework/bin/odatalib/include")
	- Add appropriate iPhoneSimulatorLibrary and choose non-recursive
	  (ex "$(SRCROOT)/../../../../Documents/ODataSDK/Framework/bin/odatalib/lib/iPhoneSimulatorLibs/iPhone_Simulator_6.1/release")
* In Build Settings -> Linking
  - Set "Mach-O Type" to "Executable"

Build OData Proxy:
* Validate OData endpoint is up and running. Copy the url
* In the command line, navigate to MacOSX10.8.sdk/Release (ex: ODataSDK/Framework/bin/ODatagenBinary/MacOSX10.8.sdk/Release)
* Execute "./odatagen /uri=http://MYURL/example.svc/ /out=."
* Move generated .h and .m files to XCode folder
* Add .h and .m files to XCode (right-click project file and select "Add Files")


Usage Instructions
==================

The SDK will run on Mac OSX machines only.

Further documentation on how to use the OData toolkit (the original version that only supported up to iOS 4) for Objective-C can be found in the [project web site](http://odata.github.com/OData4ObjC/).


Getting Help
============

Do you need help using the project, or do you want to request a feature or bug fix?

* To get some help: use the [Discussions tool on our CodePlex project page](http://odataobjc.codeplex.com/discussions).



Contributing
============

Fork and go. To contribute back, send me a pull request. 

Directory Structure
====================

	|-- framework
	|   |
	|	|
	|	|----- bin
	|		|
	|		|-- ODatagenBinary
	|		|	|
	|		|	|-- odatagen			[Proxy generation tool]
	|		|
	|		|
	|		|-- odatalib
	|			|
	|			|-- lib
	|			|   |
	|			|   |-- iPhoneDeviceLibs	[OData toolkit static library built for different device SDK versions]
	|		    |   |
	|			|   |
	|			|   |-- iPhoneSimulatorLibs	[OData toolkit static library built for different simulator SDK versions]
	|			|
	|			|
	|			|
	|			|-- include
	|				|
	|				|-- Azure       	[contains files for using OData toolkit library against Windows Azure tables]
	|  				|
	|			        |-- Common      	[contains commonly used class definition files for dictionary, collection, 
	|        			|			 guid, http proxy, reflection helper.Utility classes for Azure ACS and Azure
	|        			|               	 Table authentication and xsl file for code generation]
	|        			|
	|			        |-- Context     	[Contains class definition files for context tracking, AtomPub generation,
	|			        |               	  query and stream processing files]
	|			        |
	|				|-- Credential  	[Contains class definition files for credentials]
	|				|
	|			        |-- Exception  		[Contains class definition files for exceptions]
	|        			|
	|			        |-- Interfaces  	[Interface definitions]
	|			        |
	|			        |-- Parser     		[AtomPub parser]
	|        			|
	|			        |-- WebUtil     	[Utility files for handling normal and batch http request-response]
	|
	|
	|-- Sample	[Contains sample iPhone application]
	|	|
	|	|----- DataMarket					[NEW: Azure datamarket sample program]
	|	|
	|	|----- Netflix						[Netflix sample program]
	|	|
	|	|----- OData.org					[Sample client for OData website demo producers]
	|	
	|-- Readme.txt	[This file, one which is being read, contains files and directory information]
	|
	|-- License.txt	[Contains license information]
