# AppGatewayHostRewrite
Replaces the Host header with the X-Original-Host after Application Gateway has routed to the correct App Service.

# Installation
Install using your App Service's SCM site or through the Azure Portal.

# Usage
Once installed, you will need to restart site and SCM site (through kudu). Afterwards, all requests will be rewritten so the Host header matches the X-Original-Host.
