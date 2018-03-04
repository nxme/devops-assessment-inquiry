# devops-assessment-inquiry
This is a list of questions and checklists to verify that the application infrastructure is healthy and fulfills scalability, monitoring, notifications, logging, backups, replication, disaster recovery, load balancing, high availability.

# 1. Is Slave Replication being used for the master SQL Server database?
If yes, what is the current setup being used?

# 2. Is a load balancer being used? How many load balancers?

# 3. Is failover provided to a passive load balancer?

# 4. What type of load balancer is being used?

# 5. Which load balancing scheme is being used (eg. Round Robin, Sticky Session)

# 6. How many web server machines are being load balanced?

# 7. How do you guarantee sessions availability during load balancing between multiple machines? Where is session data stored (eg. SQLServer, Redis, CouchBase ) ?

# 8. Where are log files stored (eg. raw log files, syslog, database or forwarded to a log management tool like splunk?)

# 9. Once an error takes place in the application log file, does the Al-Elm DevOps team get notified? How does it get notified?

# 10. What type of monitoring system are you using?

# 11. Is Apache Camel used as a single instance or do you provide clustering several instances? (To avoid Single Point of Failure)

# 12. What happens when external services (eg. SADAD, Yesser) become unreachable or go down? Does it get queued, or does an error message get returned to the user?

# 13. When an external web service is down how does the application avoid flooding connection requests to the web service? (eg. Circuit Breakers, Semaphores, etc)

# 14. Do you have a backup procedure to backup the Database and external related uploaded files together? Currently, only the database backup is being received?

# 15. Incase of a disaster incidence to the database and all it's slaves, what is the disaster RPO (Recovery Point Objective), how much data is lost when recovering (eg. Last 4 hours of data, last 7 days, last 3 days). How frequently is the data being backed
up?

# 16. Where are backups stored?

# 17. What is the backup retention policy used?

# 18. Are the backups replicated outside the data center?

# 19. How are deployments and upgrades automated? Is a CI script or solution being used?

# 20. Are development and debug flags turned off on production? How is this guaranteed? Is it guaranteed?

# 21. What are the Login Session Idle Timeout for users set after which they are forced to logout (eg. 4 hours)?

# 22. What are the Login Session Absolute Timeout used for users?

# 23. Are users forced to re-authenticate their login to change their password?

# 24. Which Operating System are you using on production servers?

# 25. What are the CPU and RAM specs for the web server machines?

# 26. What are the CPU and RAM specs for the database machine?

# 27. What are the CPU and RAM specs for the load balancer?

# 28. What are the CPU and RAM specs for the middle-tier (eg. Apache Camel) machines?

# 29. How is Business Intelligence provided through the application without breaching sensitive data such as mobile numbers, Civil IDs, full names?
