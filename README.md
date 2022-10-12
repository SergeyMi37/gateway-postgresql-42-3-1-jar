[![Repo-GitHub](https://img.shields.io/badge/dynamic/xml?color=gold&label=GitHub%20module.xml&prefix=ver.&query=%2F%2FVersion&url=https%3A%2F%2Fraw.githubusercontent.com%2Fsergeymi37%2Fgateway-postgresql-42-3-1-jar%2Fmaster%2Fmodule.xml)](https://raw.githubusercontent.com/sergeymi37/gateway-postgresql-42-3-1-jar/master/module.xml)
 
![OEX-zapm](https://img.shields.io/badge/dynamic/json?url=https:%2F%2Fpm.community.intersystems.com%2Fpackages%2Fgateway-postgresql-42-3-1-jar%2F&label=ZPM-pm.community.intersystems.com&query=$.version&color=green&prefix=gateway-postgresql-42-3-1-jar)
 
## gateway-postgresql-42-3-1-jar
Module for importing instances of the %Library.SQLConnection class into the %SYS namespace, copying the jdbс driver `postgresql-42.3.1.jar`.

## Installation with ZPM

If ZPM the current instance is not installed, then in one line you can install the latest version of ZPM.
```
s r=##class(%Net.HttpRequest).%New(),proxy=$System.Util.GetEnviron("https_proxy") Do ##class(%Net.URLParser).Parse(proxy,.pr) s:$G(pr("host"))'="" r.ProxyHTTPS=1,r.ProxyTunnel=1,r.ProxyPort=pr("port"),r.ProxyServer=pr("host") s:$G(pr("username"))'=""&&($G(pr("password"))'="") r.ProxyAuthorization="Basic "_$system.Encryption.Base64Encode(pr("username")_":"_pr("password")) set r.Server="pm.community.intersystems.com",r.SSLConfiguration="ISC.FeatureTracker.SSL.Config" d r.Get("/packages/zpm/latest/installer"),$system.OBJ.LoadStream(r.HttpResponse.Data,"c")
```
If ZPM is installed, then `gateway-postgresql-42-3-1-jar` can be set with the command
```
zpm:%SYS>install gateway-postgresql-42-3-1-jar
```
