OData4ObjC edited by Elizabeth Duncan
==================

This SDK is IN PROGRESS to support up to iOS 6.


Usage Instructions
==================

The SDK will run on Mac OSX machines only.

Documentation on how to use the OData toolkit (the original version that only supported up to iOS 4) for Objective-C can be found in the [project web site](http://odata.github.com/OData4ObjC/).

Getting Help
============

Do you need help using the project, or do you want to request a feature or bug fix?

* To get some help: use the [Discussions tool on our CodePlex project page](http://odataobjc.codeplex.com/discussions).

I monitor this forum.


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
