# Lab Report 2: Servers and SSH Keys

## Part 1
**`ChatServer` code**
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String concatenated = "";
    String user = "";
    String message = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(concatenated);
        }
        else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            int i = 0;
            while (i < 2) {
                String[] request = parameters[i].split("=");
                if (request[0].equals("user")) {
                    user = request[1];
                }
                else if (request[0].equals("s")) {
                    message = request[1];
                }
                i++; 
            }
            concatenated = concatenated + "\n" + String.format("%s: %s", user, message);
            return concatenated;
        }
        else {
            return "404 Not Found!";
        }
        
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

**Using `/add-message` Example 1**
![Image](2Example1.png)
* Methods called: `/home`
* Relevant arguments for methods:
* Values of relevant class fields:
* Changes in values after request:

**Using `/add-message` Example 2**
![Image](2Example2.png)
* Methods called: `/home`
* Relevant arguments for methods:
* Values of relevant class fields:
* Changes in values after request:

## Part 2

**Absolute path to the *private key* for SSH key**
![Image](SSHprivate.png)

**Absolute path to the *public key* for SSH key**
![Image](SSHpublic.png)

**Terminal interaction with no password for `ieng6` account**
![Image](ieng6NoPWTerminal.png)

## Part 3

**What I learned from Week 2-3 Labs**
