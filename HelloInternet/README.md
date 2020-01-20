# HelloInternet
Say Hello to a remote friend in all the languages!
## Compile server
gcc hellosrvCpp.cpp -lstdc++ -o hellosrvCpp
## Compile client
gcc helloCpp.cpp -lstdc++ -o helloCpp
## Run
Start server with listen port and backlog
   ```
   ./hellosrvCpp 12345 1024
   epollserver startup,port 12345, max connection is 10000, backlog is 1024
   ```
   Start client with the server ip and port
   ```
   ./helloCpp 127.0.0.1 12345
   connected to server 127.0.0.1:12345
   Sending " Hello in Cpp "
   Received: " Goodbye  Cpp from Cpp "
   ```
The client first connects to the server, then send a message "Hello in Cpp" to the server, and the server will response it with "Goodbye  Cpp from Cpp".
On the server platform, it will print the following infomation:

   

