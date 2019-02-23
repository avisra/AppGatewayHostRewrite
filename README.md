# AppGatewayHostRewrite
Replaces the Host header with the X-Original-Host after Application Gateway has routed to the correct App Service.

# Installation
Install this extension using your App Service's SCM site or through the Azure Portal.

# Usage
Once installed, you will need to restart site and SCM site (through kudu). Afterwards, all requests will be rewritten so the Host header matches the X-Original-Host.

This extension limits itself to the App Service it is being installed through. It starts by unlocking the Host and X-Original-Host headers so they can be rewritten using rewrite rules. And then once the request reaches the app service, it restores the original Host header (via the X-Original-Host) so the application can remain intact.

# Notes
Version 0.0.1 and 0.0.2 only included the piece to unlock these two headers. Version 0.0.3 includes the rewrite rules piece as well to delivery a full solution.
