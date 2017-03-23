### Atmosphere WebSockets Samples for for Jersey, Jersey2, GWT, JavaScript, JQuery, Netty, Guice, Spring, RMI, RabbitMQ, Redis, Hazelcast, JGroups, jsr 356, Sockjs, Socket.IO, JMS, Vert.x, Play Framework, Java EE, Tomcat, Jetty, Undertow, JBoss, etc...

One sample to rule them all!

The table below describes every Atmosphere's sample by defining the server and client API used to build it. You can download the sample by clicking on its name or clone the workspace, build it and then do

```bash
  mvn jetty:run
```
or

```bash
  mvn tomcat7:run
```

Recommended samples for getting started are the chat, which demonstrate usage of all transports using an AtmosphereHandler, or the jquery-pubsub, which demonstrate how to switch from one transport to another using a Jersey Resources. If you are interested to write WebSocket only application, take a look at the atmosphere-websockethandler-pubsub sample. The pubsub sample contains a lot of small demonstration on how the Jersey extension can be used. If you are interested to write HTML5 Server Sent Events application, take a look at the atmosphere-sse-xxx samples.

If you plan to use Spring or GWT, take a look at their specific samples.

[![Analytics](https://ga-beacon.appspot.com/UA-31990725-2/Atmosphere/atmosphere-samples)]

<font color="green">**All sample supports WebSocket and Long Polling by default. Streaming and JSONP are supported by the majority of pubsub samples. If you are interested to write HTML5 Server Sent Events application, take a look at the atmosphere-sse-xxx samples.**</font>

| Sample Name | Description | Server Components | Client Components |
|-------------|-------------|-------------------|-------------------|
| [all-api-pubsub](http://search.maven.org/#artifactdetails%7Corg.atmosphere.samples%7Catmosphere-all-api-pubsub%7C0.9.4%7Cwar) | This sample implements a pubsub example that demonstrates all Atmosphere's API and extension. The use of AtmosphereResource, Meteor, Annotation like @Suspend and @Broadcast are demonstrated | [AtmosphereHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/all-api-pubsub/src/main/scala/org/atmosphere/samples/pubsub/websocket/AtmosphereHandler.scala) [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/all-api-pubsub/src/main/scala/org/atmosphere/samples/pubsub/websocket/Resource.scala) [Meteor](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/all-api-pubsub/src/main/scala/org/atmosphere/samples/pubsub/websocket/Meteor.scala) [WebSocketProtocol](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/all-api-pubsub/src/main/scala/org/atmosphere/samples/pubsub/websocket/DevoxxWebSocketProtocol.scala) | Single [Callback](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/all-api-pubsub/src/main/webapp/index.html) supporting WebSocket, Long-Polling, JSONP, Http-Streaming |
| [async-annotation-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-async-channel%22) | This sample demonstrates the use of the @Asynchronous annotation combined with the Callable API, showing how an application can be fully asynchronous in its execution. The sample implements the pubsub concepts. | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/async-annotation-pubsub/src/main/java/org/atmosphere/samples/pubsub/AsynchronousExecution.java) | Single [Callback](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/async-annotation-pubsub/src/main/webapp/index.html#L36) supporting WebSocket, Long-Polling, JSONP, Http-Streaming |
| [atmosphere-ee6](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-ee6%22) | This sample demonstrates the use of @Suspend with Java EE's 6 annotation like @Resource and EJB Timer | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/atmosphere-ee6/src/main/java/org/jersey/devoxx/samples/ee6/atmosphere/TimerResource.java) | Http-Streaming |
| [channel](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-channel%22) | This sample demonstrate the use of @Subscribe and @Publish annotation using a pub sub application. If you are migrating from CometD, this sample is for you. | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/channel/src/main/java/org/atmosphere/samples/pubsub/TypedChannel.java) |
| [chat-guice](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-guice-chat%22) | This sample demonstrate the use of Google Guice with Atmosphere. The Chat application is implemented using @Suspend and @Broadcast annotation | [Guice](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/guice/chat-guice/src/main/java/org/atmosphere/samples/guice/GuiceChatModule.java) [Jersey Resource](https://github.com/Atmosphere/atmosphere-extensions/blob/master/guice/samples/chat-guice/src/main/java/org/atmosphere/samples/guice/ResourceChat.java#L31) | Javascript Functions demonstrating [WebSocket, falling back to Long-Polling](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/guice/chat-guice/src/main/webapp/jquery/application.js) |
| [chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-chat%22) | This sample demonstrates the use of WebSocket (falling back to SSE and Long-Polling) using the [@ManagedService](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/service/ManagedService.html) annotation. The sample also demonstrates how to detect which transport are supported by the client and server by negotiating with the server. | [Chat](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/chat/src/main/java/org/atmosphere/samples/chat/Chat.java) | Javascript Functions demonstrating [WebSocket, falling back to Long-Polling](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/chat/src/main/webapp/javascript/application.js). This is the recommended sample to start with. |
| [chat-multiroom](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-chat-multiroom%22) | This sample demonstrates the use of WebSocket (falling back SSE and to Long-Polling) using the [@ManagedService](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/service/ManagedService.html) annotation with [Encoder](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/managed/Encoder.html) and [Decoder](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/managed/Decoder.html). The sample also demonstrates how to detect which transport are supported by the client and server by negotiating with the server. | [Chatroom](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/chat-multiroom/src/main/java/org/atmosphere/samples/chat/ChatRoom.java) | Javascript Functions demonstrating [WebSocket, falling back to Long-Polling](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/chat/src/main/webapp/javascript/application.js). This is the recommended sample to start with. |
| [cxf-node-client](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-chat-node-client%22) | This sample demonstrates atmosphere.js with node.js. This client can be used agaist various samples such as chat, websocket-chat, ... | | [Javascript Functions](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/chat-node-client/src/main/resources/chat-client.js)|
| [cxf-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-cxf-chat%22) | This sample demonstrates the use of WebSocket (falling back SSE and to Long-Polling) in other framework using Atmosphere. | [CXF](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/cxf-chat/src/main/java/org/atmosphere/samples/chat/cxf/ChatResource.java) | [Javascript Functions](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/cxf-chat/src/main/webapp/javascript/application.js)|
| [cxf-chat-osgi](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-cxf-chat-ogi%22) | This sample is an OSGi version of cxf-chat that demonstrates the use of Atmosphere in an OSGi container. The code is identical to that of cxf-chat and it only differs in its pom.xml file so that the appropriate bundle descriptor is generated in its manifest.mf file.| [CXF OSGi](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/cxf-chat-osgi/src/main/java/org/atmosphere/samples/chat/cxf/ChatResource.java) | [Javascript Functions](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/cxf-chat-osgi/src/main/webapp/javascript/application.js)|
| [di-guice-sample](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-di-guice-sample%22) | The sample demonstrates the use of Atmosphere's Dependencies Injection using Guice | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/guice/di-guice-sample/src/main/java/org/atmosphere/samples/di/guice/MessageResource.java) [Guice](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/di-guice-sample/src/main/java/org/atmosphere/samples/di/guice/GuiceContextListener.java) | [Javascript Callback](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/guice/di-guice-sample/src/main/webapp/index.html#L46) |
| [jersey2-chat](http://search.maven.org/#search%7Cga%7C1%7Ca%3A%22atmosphere-jersey2-chat%22) | This samples demonstrates the use of JAX RS Specification 2 with [@AtmosphereService](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/service/AtmosphereService.html) | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jersey2-chat/src/main/java/org/atmosphere/samples/chat/jersey/Jersey2Resource.java) | Javascript Functions demonstrating [WebSocket, falling back to Long-Polling](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jersey2-chat/src/main/webapp/jquery/application.js) |
| [atmospherehandler-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-atmospherehandler-pubsub%22) | This sample demonstrate the use of AtmosphereHandler for implementing a pub sub application. The sample supports Long-Polling, Http Streaming and WebSocket | [AtmosphereHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/atmospherehandler-pubsub/src/main/java/org/atmosphere/samples/pubsub/AtmosphereHandlerPubSub.java#L39) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/atmospherehandler-pubsub/src/main/webapp/index.html) |
| [atmosphere-meteor-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-meteor-pubsub%22) | This sample demonstrate the use of the Meteor API, from a Servlet, for implementing a pub sub application. The sample supports Long-Polling, Http Streaming and WebSocket | [Meteor](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-meteor-pubsub/src/main/java/org/atmosphere/samples/pubsub/MeteorPubSub.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-meteor-pubsub/src/main/webapp/index.html#L8) |
| [jquery-multirequest](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-multirequest%22) | This sample demonstrates how multi requests can be made using the jQuery.atmosphere.js. The sample implements the pub sub application. | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-multirequest/src/main/java/org/atmosphere/samples/multirequest/handlers/Subscriber.java#L33) | [Per Request and Global callback](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-multirequest/src/main/webapp/js/main.js) |
| [jquery-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-jquery-pubsub%22) | This sample demonstrates all transports (WebSockets, Server Side Events, Long-Polling, Http Streaming and JSONP using a super simple Jersey Resource. The sample implements a pub sub application. | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-pubsub/src/main/java/org/atmosphere/samples/pubsub/JQueryPubSub.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-pubsub/src/main/webapp/index.html) |
| [jquery-websockethandler-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-websockethandler-pubsub%22) | This sample demonstrates how to write WebSocket only application | [WebSocketHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-websockethandler-pubsub/src/main/java/org/atmosphere/samples/pubsub/WebSocketPubSub.java#L36) | [Javascript Funtion](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/jquery-websockethandler-pubsub/src/main/webapp/index.html#L36) |
| [jquery-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-pubsub%22) | This sample demonstrates a lot of server side functionality like broadcast/suspend/resume using a Jersey Resource. | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/pubsub/src/main/java/org/atmosphere/samples/pubsub/PubSub.java) |
| [meteor-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-meteor-chat%22) | This sample demonstrates of the Meteor API, from a Servlet, can be used to implement a chat application | [Meteor](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/meteor-chat/src/main/java/org/atmosphere/samples/chat/MeteorChat.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/meteor-chat/src/main/webapp/jquery/application.js) |
| [meteor-pubsub](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-meteor-pubsub%22) | This sample demonstrates of the Meteor API, from a Servlet, can be used to implement a chat application | [Meteor](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/meteor-pubsub/src/main/java/org/atmosphere/samples/chat/MeteorPubSub.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/meteor-pubsub/src/main/webapp/index.html) |
| [rest-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-rest-chat%22) | This sample demonstrates the use of a Jersey Resource for implementing a chat application | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/rest-chat/src/main/java/org/atmosphere/samples/chat/jersey/ResourceChat.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/rest-chat/src/main/webapp/jquery/application.js) |
| [scala-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-scala-chat%22) | This sample demonstrates how to use Scala to write a chat application | [Scala Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/scala-chat/src/main/scala/org/atmosphere/samples/scala/chat/ScalaChat.scala) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/scala-chat/src/main/webapp/jquery/application.js) |
| [spring-tiles](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-spring-tiles%22) | This sample demonstrates how to use the Spring and Tiles Framework with AtmosphereHandler. The sample implements a pubsub application | [Spring Controller](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/spring/spring-tiles/src/main/java/org/atmosphere/samples/pubsub/spring/PubSubController.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/spring/spring-tiles/src/main/webapp/pages/pubsubHeader.jsp#L6) |
| [spring-websocket](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-spring-websocket%22) | This sample demonstrates the use of Spring with Atmosphere WebSocketHandler, Meteor and AtmosphereHandler | [Meteor](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/spring/spring-websocket/src/main/java/org/atmosphere/samples/pubsub/utils/AtmosphereUtils.java#L31) [Service](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/spring-websocket/src/main/java/org/atmosphere/samples/pubsub/services/ChatService.java) [WebSocketProtocol](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/spring-websocket/src/main/java/org/atmosphere/samples/pubsub/config/protocol/DelegatingWebSocketProtocol.java) | [Spring View](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/spring/spring-websocket/src/main/webapp/WEB-INF/views/home.jsp#L9) |
| [sse-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-chat-sse%22) | This sample demonstrates how to use HTML 5 Server Sides Events to build a chat application using an AtmosphereHandler | [AtmosphereHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/sse-chat/src/main/java/org/atmosphere/samples/chat/ChatAtmosphereHandler.java) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/sse-chat/src/main/webapp/jquery/application.js) |
| [sse-rest-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-sse-rest-chat%22) | This sample demonstrates how to use HTML 5 Server Sides Events to build a chat application using a Jersey Resource | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/sse-rest-chat/src/main/java/org/atmosphere/samples/chat/jersey/ResourceChat.java#L33) | [Javascript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/sse-rest-chat/src/main/webapp/jquery/application.js) |
| [twitter-live-feed](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-twitter-live-feed%22) | This sample demonstrates how to use jQuery.atmosphere.js to implements a real time Twitter Search using a simple Jersey Resource. It also demonstrate how BroadcastFilter can be used to mark to handle large set of data to send back to the client | [Jersey Resource](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/twitter-live-feed/src/main/java/org/atmosphere/samples/twitter/TwitterFeed.java#L48) | [JavaScript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/twitter-live-feed/src/main/webapp/index.html#L34) |
| [socketio-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-socketio%22) | This sample demonstrates how the SocketIO library can be used, trsnaparently, using an AtmosphereHandler | [AtmosphereHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/socketio/socketio-chat/src/main/java/org/atmosphere/samples/chat/SocketIOChatAtmosphere.java) | [SocketIO](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/socketio/socketio-chat/src/main/webapp/javascript/application.js#L1) |
| [native-socketio-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-socketio%22) | This sample demonstrates how the SocketIO library and natively extending the SocketIO protocol on the server side | [AtmosphereHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/socketio/native-socketio-chat/src/main/java/org/atmosphere/samples/chat/ChatAtmosphereHandler.java) | [SocketIO](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/socketio/native-socketio-chat/src/main/webapp/index.html#L1) |
| [cometd/bayeux protocol](https://oss.sonatype.org/content/repositories/snapshots/org/atmosphere/samples/atmosphere-cometd-demo/) | This sample deploy the [Cometd official](http://cometd.org/) demo on top of Atmosphere |
| [websocket-chat](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-websocket-chat%22) | This sample demonstrates how to write WebSocket ONLY applications | [WebSockerHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/websocket-chat/src/main/java/org/atmosphere/samples/chat/WebSocketChat.java#L33) | [JavaScript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/websocket-chat/src/main/webapp/jquery/application.js#L1) |
| [websocket-stream](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22atmosphere-websocket-stream%22) | This sample demonstrates how to write WebSocket streaming applications | [WebSockerHandler](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/websocket-stream/src/main/java/org/atmosphere/samples/stream/WebSocketStream.java#L33) | [JavaScript Function](https://github.com/Atmosphere/atmosphere-samples/blob/master/samples/websocket-stream/src/main/webapp/jquery/application.js#L1) |
| [gwt2-jersey-rpc](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22gwt20-jersey-rpc%22) | GWT RPC with Jersey | [Server](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-json/src/main/java/org/atmosphere/samples/client/GwtJsonDemo.java) | [Client](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/qwt20-jersey-rpc/src/main/java/org/atmosphere/samples/client/GwtJerseyDemo.java) |
| [gwt20-json](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22gwt20-json%22) | GWT with JSON | [Server](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-json/src/main/java/org/atmosphere/samples/server/JerseyGwtRpc.java) | [Client](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-json/src/main/java/org/atmosphere/samples/client/GwtJsonDemo.java) |
| [gwt20-managed-rpc](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22gwt20-json%22) | GWT RPC using the [@ManagedService](http://atmosphere.github.io/atmosphere/apidocs/org/atmosphere/config/service/ManagedService.html) annotation | [Server](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-managed-rpc/src/main/java/org/atmosphere/samples/server/ManagedGWTResource.java#L40) | [Client](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-managed-rpc/src/main/java/org/atmosphere/samples/client/GwtRpcDemo.java#L82) |
| [gwt20-rpc](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22gwt20-json%22) | GWT RPC using the an AtmosphereHandler | [Server](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-rpc/src/main/java/org/atmosphere/samples/server/GwtRpcAtmosphereHandler.java) | [Client](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-websockets/src/main/java/org/atmosphere/samples/client/GwtWebsocketsDemo.java) |
| [gwt20-websockets](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.atmosphere.samples%22%20AND%20a%3A%22gwt20-websockets%22) | GWT client websockets using com.sksamuel.gwt | [websocket-stream](./samples/websocket-stream) | [Client](https://github.com/Atmosphere/atmosphere-samples/blob/master/extensions-samples/gwt/gwt20-websockets/src/main/java/org/atmosphere/samples/client/GwtWebsocketsDemo.java) |


Note that for those samples using jQuery, version 2.x is used and they are not compatible with IE 6, 7, and 8. Try other browsers. For more information, see [https://jquery.com/browser-support/](https://jquery.com/browser-support/)
