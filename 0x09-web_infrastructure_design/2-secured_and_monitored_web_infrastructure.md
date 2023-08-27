Explanation of the Infrastructure:

Firewalls:

Added to secure servers by filtering incoming and outgoing traffic, protecting against unauthorized access.
Protects against potential security threats and attacks.
SSL Certificate and HTTPS:

SSL certificate added to the Load-Balancer to enable HTTPS, ensuring encrypted communication between users and the website.
HTTPS enhances security and user privacy by encrypting data transmitted over the network.
Monitoring Clients:

Monitoring clients (data collectors) gather performance, availability, and security data from servers and applications.
Used for real-time monitoring, issue detection, and performance optimization.
Load-Balancer (SSL Termination):

SSL termination occurs at the load balancer, decrypting incoming HTTPS traffic and forwarding it to the application servers as HTTP traffic.
This reduces the computational load on application servers and ensures encrypted traffic between users and the load balancer.
Replica Databases:

Added for data redundancy, improved read scalability, and high availability.
Follows a Primary-Replica (Master-Slave) cluster setup for data consistency and backup.
Monitoring Data Collection:

Monitoring clients collect data on server performance metrics, application response times, error rates, and more.
Data is sent to monitoring tools like Sumo Logic for analysis and visualization.
Monitoring Web Server QPS (Queries Per Second):

To monitor web server QPS, set up monitoring to track incoming HTTP requests per second to the web server.
Issues with the Infrastructure:

Terminating SSL at Load Balancer:

Terminating SSL at the load balancer can expose unencrypted data within the internal network, reducing overall security.
Single MySQL Server Accepting Writes:

Having only one MySQL server that can accept writes is a single point of failure and a potential performance bottleneck.
Uniform Components on Servers:

Servers with identical components may lead to resource contention and uneven load distribution, reducing scalability and performance.
A more robust solution could involve end-to-end SSL encryption, setting up a failover system for MySQL, and optimizing server configurations based on their roles to ensure better security, availability, and performance.
