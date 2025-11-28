# ace-admin-api
IBM App Connect Enterprise (ACE) provides an [administrative REST API](https://www.ibm.com/docs/en/app-connect/13.0.x?topic=enterprise-managing-resources-by-using-administration-rest-api) through which local or remote applications can administer ACE integration nodes and ACE integration servers.

When users install ACE, and then create and configure an integration node, the integration node will serve a definition of its REST API specification over http/https on a URL accessible via its administration port: 
```
https://<hostname>:<port>/apidocs
```
For example on your local laptop this could be: https://localhost:4414/apidocs

Similarly, when users install ACE, and then create and configure an independent integration server, the integration server will serve a definition of its REST API specification over http/https on a URL accessible via its administration port:

```
https://<hostname>:<port>/apidocs 
```
For example on your local laptop this could be: https://localhost:7600/apidocs

The ACE product installation provides two separate Open API definition files (one for integration nodes and one for integration servers):

* openapi-appconnectenterprise.yaml details the REST API for administering integration nodes.
* openapi-appconnectenterpriseserver.yaml details the REST API for administering integration servers.

The two files are very similar, but the integration node offers a few more URL routes, and when using the integration node's API the URL paths will frequently contain additional sections to address a specific target server which is owned by the integration node.

The above Open API files can be found in an installation of ACE in the following directories:
```
install_dir\server\nodejs\node_modules\@ibm-app-connect\ace-admin-api\docs\server
install_dir\server\nodejs\node_modules\@ibm-app-connect\ace-admin-api\docs\node
```
For the convenience of those who may not have easy access to an ACE installation but who wish to learn more about the ACE admin API, this repository provides the same Open API files discussed above, for each of the main ACE mod releases.
