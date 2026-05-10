### Load Balancers : 

* A load balancer is a system that distributes incoming network traffic or requests across multiple servers so that no single server becomes overloaded.

* Without load balancer :
    * Users → One Server

* With load balancer :
    * Users → Load Balancer → Multiple Servers
 
* Main Purposes of Load Balancing :
    * Prevent Server Overload : Traffic is shared among servers.
    * High Availability : If one server fails, traffic goes to others.
    * Scalability : New servers can be added easily.
    * Better Performance : Users experience faster response times.
    * Fault Tolerance : System keeps working even during failures.

* Types of Load Balancers :
    * 1. Hardware Load Balancer :Dedicated physical devices, examples : F5 BIG-IP ,Cisco load balancers.
    * 2. Software Load Balancer : Runs as software on servers, examples : NGINX, HAProxy,Traefik
    * 3. Cloud Load Balancer : Managed by cloud providers, emamples : Amazon Web Services ELB, Google Cloud Load Balancer, Microsoft Azure Load Balancer 

* Load Balancing Layers :
    
    * Layer 4 Load Balancing (Transport Layer) : Works using: IP addresses -> TCP/UDP ports, Fast but less intelligent.
    * Layer 7 Load Balancing (Application Layer) : Works using: URLs, HTTP headers, Cookies, Content type, More intelligent.
 
* Load Balancer in Cloud Architecture :

    * Users -> Load Balancer -> Web Servers -> Database Servers
    * Auto Scaling + Load Balancing
         * Cloud systems combine: Load balancers and Auto scaling
         * When traffic increases: New servers added automatically
         * When traffic decreases: Servers removed
  

