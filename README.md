WB Objects framework
================================

WB Objects Framework is an ABAP framework. WB stands for Workbench so this framework mainly encapsulates ABAP repository objects (Classes, Interfaces, Packages, Reports, Includes etc) into classes that can be used across any project which needs this information ([ABAP2yUML](https://github.com/fabiopagoti/yuml-abap),SAPLink or similars, ABAPDoc, etc). Moreover, this framework comes with useful classes to handle frequently used logic with workbench objects such as search functionality.


### Example
Supposing you need to retrieve all details from the very famous class CL_SALV_TABLE. All you need to do is:

```ABAP
DATA o_any_class TYPE REF TO zcl_wb_class_global.
DATA wa_seoclskey TYPE﻿seoclskey.

wa_seoclskey-clsname = 'CL_SALV_TABLE'.

CREATE OBJECT o_any_class
	EXPORTING
		im_clskey = wa_seoclskey.
		
o_any_class->zif_wb_object~load( ).

 ```
... and it's done! Now you can access any detail from the class CL_SALV_TABLE using the attributes of o_any_class instance.


## System Requirements
This projects is developed using SAP NetWeaver Trial Edition (SAP NetWeaver 7.31 Support Package 4). We do our best to keep a modern project so at the moment there is no guarantee it works perfectly on previous releases. We would love your support to test it if you have older releases and tell us possible issues.

## Installation
The installation of this projects comes as SAPLink files so you should have it installed into your system. Refer to the Installation page for more details.

## Documentation
Most open source projects are not documented. This has no intentions to be another example. Refer to the Wiki if you are looking for documentation.

## Contributors

[Fábio Pagoti](http://br.linkedin.com/in/fabiopagoti/) - Product Architect

## Want to contribute? 
There are many ways to contribute. Don't worry if you are not (yet) an ABAP developer. Here are some ways you can help support this project:
* Coding
* Testing (UX, Security, Performance, Design)
* Using
* Reviewing documentation
* Reporting bugs
* Suggesting enhancements
* Sharing among friends, SCN, Facebook, Twitter, LinkedIn, etc

## Special thanks to:
* Who collaborate on this project sharing it on SAP Community Network, Facebook, Twitter, LinkedIn
* SAP developers who wrote some very useful function modules

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/fabiopagoti/wb-objects/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

