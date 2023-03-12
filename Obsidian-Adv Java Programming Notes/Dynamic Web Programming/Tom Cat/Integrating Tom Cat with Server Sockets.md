To integrate Apache Tomcat with sockets in Java, you will need to create a Java web application that uses the `java.net` package to create and use sockets. You can then package this web application as a WAR file and deploy it on Apache Tomcat to run it.

Here is an example of a Java web application that uses sockets and can be deployed on Apache Tomcat:

```java
import java.io.*;
import java.net.*;
import javax.servlet.*;
import javax.servlet.http.*;

public class SocketServlet extends HttpServlet {
  @Override
  public void doGet(HttpServletRequest request, HttpServletResponse response)
      throws ServletException, IOException {
    // Create a server socket on port 8000
    ServerSocket serverSocket = new ServerSocket(8000);

    // Listen for a client connection
    Socket socket = serverSocket.accept();

    // Create a buffered reader to read data from the client
    BufferedReader reader = new BufferedReader(
        new InputStreamReader(socket.getInputStream()));

    // Read the message from the client
    String message = reader.readLine();

    // Print the message to the console
    System.out.println("Received from client: " + message);

    // Create a print writer to send data to the client
    PrintWriter writer = new PrintWriter(socket.getOutputStream());

    // Send a response to the client
    writer.println("Hello from the server!");
    writer.flush();
  }
}

```