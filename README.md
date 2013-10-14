ssl-utils
=========

Various SSL related utilities

## Trust All TrustManager

This is a TrustManager that trusts all certificates that it receives. This can be useful in a development or testing
environment when dealing with self signed certificates or in a servlet container that handles certificate verification
internally.

### Tomcat configuration

TrustAllTrustManager can be used in Tomcat:

```xml
<Connector port="8443"
           protocol="org.apache.coyote.http11.Http11Protocol"
           trustManagerClassName="net.unicon.ssl.TrustAllTrustManager"
           scheme="https"
           SSLEnabled="true"
           clientAuth="want" />
```
