# Set Up Archive Link Connection
## Use

With this Customizing activity, you get an overview of the most relevant steps to set up the connection from Archive Link to the ILM Store.

The Archive Link connection with ILM Store can be used in three different scenarios: 
- as local implementation
- as a remote scenario
- or as an http server implementation.

The following configuration steps need to be done before you can use the Archive Link connection:

- Check table TILM_STOR_CMS for the following valid entry:
```
Data Source	Namespace	Name of Property		Value
<origin>	DB	DBCON.TILM.STOR_CMS		Default
```
The Default value points to the local database of the application server.

- Create ILM Store-based content server (transaction OAC0) and enter the needed values.
*For more information, see the Installation and Configuration Guide for ILM Store.*
- Link the content repository to an origin
- Enter the content repository name that has been created (<CREP_ID>) in
  ```Define the Settings for Administrative Customizing -> Modify Operational Origin```
  to assign it to a specific operational origin.
- Create needed document types (transaction OAC2)
*You need to add the document types you usually use in your project for transferring data via Archive Link to the ILM Store. You can add several document types, as PPTX or JPEG, for example. For more information, see the Archive*
- Create the links for the content repositories (transaction OAC3)
*You need to create the links of the object types to the relationship tables. For more information, see the Archive*
- Test the configuration steps
*To test the Archive Link connection, upload any document to the ILM Store for verification.*

For more detailed configuration information, please see the Installation and Configuration Guide for ILM Store on SAP Service Marketplace at http://service.sap.com/ilm -> Media Library.

[Quick Configuration Guide for the ILM Store](./21f9ec5ad170450b978d6863d2a3cbca.pdf)
