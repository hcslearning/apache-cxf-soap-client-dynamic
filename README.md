# Apache CXF consumo WS SOAP - Manera Dinámica

Ejemplo consumo WS SOAP de manera dinámica (sin generar stubs).

```java
import org.apache.cxf.endpoint.Client;
import org.apache.cxf.jaxws.endpoint.dynamic.JaxWsDynamicClientFactory;

String wsdlUrl = "https://www.dataaccess.com/webservicesserver/NumberConversion.wso?WSDL";
JaxWsDynamicClientFactory factory = JaxWsDynamicClientFactory.newInstance();
Client client = factory.createClient(wsdlUrl);
Object[] respuesta = client.invoke("NumberToWords", new BigInteger("33"));
System.out.println("Respuesta: "+respuesta[0]);
```


