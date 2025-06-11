### Minimum Viable Product (MVP):
Goal: Create a minimal functional product that can be brought to market and receive feedback from users. In our case, this is a demonstration of the AsciiArtify application

Documentation content: MVP documentation should include more details compared to PoC. Typically, this includes defining functional requirements, interface design, technical architecture, execution plan, test plan, scaling plan, and implementation strategy.

Checking the operation of the AsciiArtify application
Forward the ports with the following command:

$k port-forward svc/ambassador 8081:80 
Forwarding from 127.0.0.1:8081 -> 80
Forwarding from [::1]:8081 -> 80
Handling connection for 8081

$ curl curl -F 'image=@Linux.png' localhost:8081/img/

✗ k get svc -n demo
NAME                     TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)                                                 AGE
demo-api                 ClusterIP      10.43.133.224   <none>        80/TCP                                                  25d
demo-ascii               ClusterIP      10.43.79.61     <none>        80/TCP                                                  25d
demo-data                ClusterIP      10.43.121.255   <none>        80/TCP                                                  25d
demo-img                 ClusterIP      10.43.243.125   <none>        80/TCP                                                  25d
demo-mysql               ClusterIP      10.43.94.99     <none>        3306/TCP                                                25d
demo-nats                ClusterIP      None            <none>        4222/TCP,6222/TCP,8222/TCP,7777/TCP,7422/TCP,7522/TCP   25d
demo-redis-headless      ClusterIP      None            <none>        6379/TCP                                                25d
demo-redis-master        ClusterIP      10.43.75.43     <none>        6379/TCP                                                25d
envoy-demo-eg-0d68e7be   LoadBalancer   10.43.134.167   <pending>     80:31890/TCP                                            25d
envoy-gateway            ClusterIP      10.43.28.41     <none>        18000/TCP,18001/TCP,18002/TCP,19001/TCP                 25d
envoy-test-eg-9483c8f2   LoadBalancer   10.43.217.212   <pending>     80:31105/TCP                                            17d
express                  ClusterIP      10.43.223.70    <none>        8081/TCP                                                30d


Let's check the changes:

curl -F 'image=@g.png' localhost:8081/img/
We will get the result directly in the console:
Result

