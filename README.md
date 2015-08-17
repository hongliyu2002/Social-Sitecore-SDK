# Telligent Community SDK for Sitecore
####Dependencies
The Telligent Community SDK for Sitecore requires that you have installed and are running Telligent Community (minimum version 8.5) and Sitecore (minimum version 7.5) or have access to cloud/SaaS versions of these products. The Telligent Community SDK for Sitecore has dependencies on libraries that, for licensing reasons, are not included. You will need to obtain the libraries listed below and copy them to the */lib* folder before compiling:

**Sitecore**
- Sitecore 7.5 or higher
- Sitecore.Client.dll
- Sitecore.Kernel.dll

**Telligent Community**
- Telligent Community (free or commercial) 8.5 or higher
- [Telligent Community REST SDK v1.0.40 or higher](/Telligent/Social-Rest-SDK/)

**.NET Framework**
- version 4.5 or higher

###What is the Telligent Community SDK for Sitecore?
The Telligent Community SDK for Sitecore is a framework to allow you to easily interact with Telligent Community content natively within Sitecore. The entire Telligent Community platform is available through these APIs and allows you to natively add blogs, forums, wikis, comments, ratings and more natively running within Sitecore. Samples are available that demonstrate how this can be done [Telligent Community SDK for Sitecore samples](https://github.com/Telligent/Social-SitecoreSDK-Samples).

The Telligent Community SDK for Sitecore adds Sitecore specific behaviors and functionality around the [Telligent Community REST SDK](https://github.com/Telligent/Social-Rest-SDK/).

####Is this the same as Telligent Connector for Sitecore?
No, the Telligent Connector for Sitecore (last release is version 3) is the predecessor to the Telligent Community SDK for Sitecore. While the technology behind the Telligent Connector for Sitecore and the Telligent Community SDK for Sitecore are the same, the Telligent Community SDK for Sitecore was built specifically from the feedback of partners and customers that had previously used the Telligent Connector for Sitecore integration. 

The Telligent Connector for Sitecore utilized remote widget rendering to allow any Telligent widget to render within Sitecore. While this enabled any Telligent widget to easily run within Sitecore, it limited the control that developers had over the rendering.

The Telligent Community SDK for Sitecore does not use the remote widget rendering, but instead is designed to give developers more direct access to the RESTful Platform APIs offered by Telligent Community. This is done though a .NET developer friendly API and integration directly with Sitecore specific functionality.

####Can I still use the Telligent Community RESTful / Platform APIs directly?
Yes, the RESTful APIs are a great way to integrate with any technology because it is platform independent, i.e Java, PHP, .NET, and because of its use of standard XML and JSON for data transfer. Developers working with Sitecore and Telligent Community can absolutely still write REST API calls themselves.

However, the Telligent Community SDK for Sitecore is designed to make this much easier as it abstracts much of the REST and authentication infrastructure. The Telligent Community SDK for Sitecore still relies on RESTful HTTPS API calls to interact with Telligent Community, however it is managing these API calls and returning .NET dynamic objects that allow the developer to interact with the data much like you would the strongly types classes inside Telligent Community. For that reason it is does require the same version of the .NET framework as your Telligent Community site. In addition the Telligent Community SDK for Sitecore handles authentication via OAuth natively and you do not have to implement the OAuth flow yourself.

Additionally, unique Sitecore specific integration will be added to the Telligent Community SDK for Sitecore over time, such as integration with the Sitecore Experience User Database.

####What about performance?
You still have to consider that the Telligent Community SDK for Sitecore is dependent on making HTTPS requests to Telligent Community. Any hinderance in that communication can cause performance issues similar to any out of process call (such as direct REST API calls or interactions with a database).

Underlying the Telligent Community SDK for Sitecore, the Telligent Community REST SDK provides features to aid developers in getting optimal performance: API data trimming, async calls and API batching (API batching allows multiple API calls to be made over a single REST request).

####Where is the documentation?
Please refer to the [wiki section](https://github.com/Telligent/Social-Sitecore-SDK/wiki/) of this repository.

####How do I report a bug?
You can use the [issues section](https://github.com/Telligent/Social-Sitecore-SDK/issues/) of this repository to report any issues.

####Where can I ask questions?
Please visit our [developer community](http://community.telligent.com/developers/) to ask questions, get answers, collaborate and connect with other developers. Plus, give us feedback there so we can continue to improve these tools for you.

####Can I contribute?
Yes, we will have more details soon on how you can contribute.
