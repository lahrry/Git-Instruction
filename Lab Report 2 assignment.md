```
import java.io.IOException;
import java.net.URI;
```

class Handler implements URLHandler{

  String str = " ";
  //initializing to an empty string
  public String handleRequest(URI url){
    System.out.println("Path: " + url.getPath());
    if(url.getPath().contains("/add-message")){
      //after the domain, "/add-message" should be contained
      String[] parameters = url.getQuery().split("=");
      //in this query, key-value is separated by =. So the key parameter will be "s"
      //and the string that we will type will be the value parameter. 
      if(parameters[0].equals("s")){ //&& (parameters.length == 2)
        //if the first parameter(key) equals to "s" and the parameter length is two 
        //parameter length has to be 2 because in "s"="How%20are%20you" there are two strings
        String type = parameters[1].replace("%20", " ");
        //Talking about the second parameter which is value parameter
        //where we are going to type after "="
 
        //replace() method: first parameter in replace(first parameter, second parameter) is replaced 
        //by the second parameter. So here %20 is replaced by space because URL encode 
        //space as %20 or +. I used %20 which is URL space character. 
        str += "\n" + type;
        //str = str + type"\n" means it will concatenate a new line after we type a string(type)
        return str;

      }
    }
    return "404 Not Found!";
  }
}

class StringServer {
  public static void main(String[] args) throws IOException {
      if(args.length == 0){
          System.out.println("Missing port number! Try any number between 1024 to 49151");
          return;
      }

      int port = Integer.parseInt(args[0]);

      Server.start(port, new Handler());
  }
}
