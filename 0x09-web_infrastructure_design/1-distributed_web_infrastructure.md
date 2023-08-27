Explanation of the Infrastructure:

Load-Balancer (HAproxy):

Added to distribute incoming traffic across multiple servers, enhancing performance and providing high availability.
Uses Round-Robin distribution algorithm to evenly distribute requests among application servers.
Replica Databases:

Added for data redundancy and improved read scalability.
Follows a Primary-Replica (Master-Slave) cluster setup.
Server 1 - Load-Balancer and Primary Database:

Load-Balancer balances traffic across Application Servers.
Primary Database stores authoritative data and handles write operations.
Server 2 - Application Server and Replica Database:

Application Server processes requests alongside the primary server.
Replica Database serves as a read-only copy, reducing the load on the primary and improving read performance.
Server 3 - Replica Database:

Additional replica for improved read scalability and redundancy.
Load Balancer Configuration:

Round-Robin algorithm used for even distribution of requests among Application Servers.
Active-Active vs. Active-Passive Setup:

Active-Active: All servers are actively serving traffic simultaneously.
Active-Passive: One server (or component) is actively serving traffic while the others are on standby, only becoming active if the primary fails.
Primary-Replica (Master-Slave) Database Cluster:

Primary Database (Server 1) handles write operations, ensuring data consistency.
Replica Databases (Servers 2 and 3) are read-only copies, synchronized with the primary for improved read performance and redundancy.
Issues with the Infrastructure:

Single Points of Failure (SPOF):

Load-Balancer and Database can still be SPOFs if they are not redundantly configured.
Security Issues:

No firewall mentioned, leaving servers vulnerable to unauthorized access.
No HTTPS mentioned, risking data transmission security.
No Monitoring:

Lack of monitoring tools means issues might go unnoticed, impacting performance and availability.
A more robust solution would address these issues by implementing redundant load-balancers, firewalls, HTTPS encryption, and monitoring tools to ensure better security, availability, and performance.
