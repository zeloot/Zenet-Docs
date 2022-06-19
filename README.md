# Zenet Docs
### [Zenet Library](https://github.com/zeloot/Zenet/)

## Introduction

### What is zenet?
Zenet is a socket library. This is abstract and facilitates real-time (online) application creation and development using socket.
Its strong point or motivation of creation is the ease of use and speed, that is without external dependencies and without much overhead and it is extensible.

### How to use or use “Zenet”?
In this document is the description and documentation of its use.

### Runtime and supported platforms
Zenet runs and supports all platforms, which runs dotnet the solution is based on the “dotnet standard 2.0 - library“ version of dotnet. Whether in “dll” and/or “bare source code”

### Unity runtime
As described the current library runs on all “dotnet” platforms and unity does not shy away from it! [We even have a library available in the asset store](https://example.com)

### Warning
Depending on the platform, the runtime needs to dispatch the messages on its own, relax this is so simple that it only takes 2 lines of code “1 line: it will say that the responsibility of dispatching the messages is manual. This means that when receiving a message it is not dispatched automatically but manually ” and “2nd line: it must be executed in an update or loop, so that each message received is dispatched in the dispatcher loop", that's all. necessary for runtimes like Unity, FlaxEngine, etc. but is already built in [(Unity Asset Store)](https://example.com).
See the tutorial in code, in the topic “Main Thread“.

<hr>

## Documentation

### Instance creation
- #### Unity
  - ##### Client
  ```csharp    
    using Zenet.Tcp;

    public class Example : MonoBehaviour
    {
        public TcpClient client;

        private void Awake()
        {
            // create a instance
            client = new TcpClient();
        }
    }
    ```
    - ##### Server
    ```csharp    
    using Zenet.Tcp;

    public class Example : MonoBehaviour
    {
        public TcpServer server;

        private void Awake()
        {
            // create a instance
            server = new TcpServer();
        }
    }
    ```
- #### Dotnet 6
  - ##### Client
  ```csharp    
    using Zenet.Tcp;
    
    // create a instance
    TcpClient client = new();
    ```
    - ##### Server
    ```csharp    
    using Zenet.Tcp;
    
    // create a instance
    TcpServer server = new();
    ``` 


