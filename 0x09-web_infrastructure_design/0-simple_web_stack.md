Design of Single-Server Web Infrastructure for www.foobar.com:

User Access:

A user types in "www.foobar.com" in their web browser.
Domain Name:

The domain name "foobar.com" serves as the human-readable address for the website.
The "www" subdomain is a DNS record that points to the server's IP address (8.8.8.8).
DNS Resolution:

When the user enters "www.foobar.com," their computer queries a DNS server to resolve the domain name to an IP address (8.8.8.8).
Server:

The server with IP 8.8.8.8 hosts the entire web infrastructure.
It is a physical or virtual machine responsible for processing and responding to incoming requests.
Web Server (Nginx):

The web server (Nginx) acts as the initial point of contact for incoming HTTP requests.
It handles tasks such as receiving requests, serving static files, and passing dynamic requests to the application server.
Application Server:

The application server executes the web application's logic and generates dynamic content based on user requests.
It communicates with the web server to process dynamic requests and returns the appropriate response.
Application Files (Code Base):

The application files contain the code and resources that make up the web application.
These files are stored on the server and are executed by the application server to generate responses.
Database (MySQL):

The database (MySQL) stores and manages the website's data, such as user accounts, posts, or other information.
The application server communicates with the database to retrieve or update data as required by user requests.
Communication with User:

When the user's computer sends a request to "www.foobar.com," the request travels through the Internet to the server's IP address (8.8.8.8).
The web server processes the request and communicates with the application server and database as needed.
The server generates a response, which is then sent back through the Internet to the user's computer, displaying the website in their browser.
Issues with the Infrastructure:

Single Point of Failure (SPOF):

Since there is only one server, any hardware or software failure could result in the entire website going down.
Downtime during Maintenance:

During maintenance or updates, the web server may need to be restarted, causing downtime for users accessing the website.
Limited Scalability
