   Task 1: Introduction and Conceptual Understanding

 Introduction
Docker is a powerful platform that has revolutionized modern DevOps practices by enabling efficient software deployment, scalability, and automation. It allows developers and operations teams to build, package, and deploy applications consistently across different environments. Docker’s lightweight nature, portability, and compatibility with cloud-native technologies make it a preferred choice for modern software development and deployment.

With the rise of microservices and Continuous Integration/Continuous Deployment (CI/CD) pipelines, Docker provides a seamless way to create, manage, and scale applications while reducing infrastructure overhead. By using Docker, teams can avoid the "it works on my machine" problem, as containers ensure that applications run identically in development, testing, and production environments.

 Virtualization vs. Containerization
Both virtualization and containerization aim to provide isolated environments for applications, but they differ in their architecture and efficiency.

 Virtualization
Virtualization uses a hypervisor to create and manage virtual machines (VMs). Each VM includes a full guest operating system, binaries, libraries, and dependencies, running on top of a host operating system. This approach allows multiple applications to run on a single physical machine but comes with performance and resource overhead.

 Advantages of Virtualization:
- Hardware abstraction enables multiple OS environments on the same machine.
- Strong isolation between applications.
- Ideal for running different OS types (e.g., Linux and Windows on the same host).

 Disadvantages of Virtualization:
- High resource usage due to multiple OS instances.
- Slower startup and shutdown times.
- Increased maintenance effort for managing OS patches and updates.

 
Containerization
Containerization, as implemented by Docker, provides a lightweight alternative to virtualization. Instead of running a full OS for each application, containers share the host OS kernel but remain isolated from one another. Containers package an application along with its dependencies, ensuring consistency across different environments.

 Advantages of Containerization:
- Lightweight: Containers share the host OS kernel, reducing resource usage.
- Faster startup time: Containers launch in seconds compared to VMs.
- Improved scalability: Easily scale applications horizontally across cloud and on-premise environments.
- Consistent environments: Ensures applications run the same way in development, testing, and production.
- Better CI/CD integration: Enables automation of testing, building, and deployment.

 Why Containerization is Preferred for Microservices & CI/CD Pipelines

1. Microservices Architecture:
   - Microservices break down applications into smaller, independently deployable services.
   - Containers provide isolation, making it easy to deploy and update services independently.
   - They help scale individual services without affecting others.

2. CI/CD Efficiency:
   - Containers allow developers to package applications with dependencies, ensuring consistency.
   - They streamline automated testing and deployment, reducing delays in software release cycles.
   - Rolling updates and blue-green deployments are easier with containers.

3. Cross-Platform Portability:
   - Docker ensures that an application developed on one machine runs identically on another.
   - It supports multi-cloud environments, enabling seamless migration.

4. Resource Optimization:
   - Unlike VMs, which require significant system resources, containers consume minimal resources.
   - More containers can run on the same hardware compared to VMs.

 Conclusion
Containerization, particularly through Docker, is the foundation of modern DevOps workflows. Compared to traditional virtualization, containers offer lightweight, scalable, and efficient solutions for microservices and CI/CD pipelines. Organizations adopting containerization can achieve faster deployments, reduced infrastructure costs, and improved software consistency across environments, making it the preferred approach in today’s cloud-native world.
                                                                                             

------------------------------- Practical ---------------------------
Docker :

$ sudo apt-get install docker.io

 

docker:x:122:

  
1.	sudo – Runs the command with superuser (root) privileges, required for installing system packages.
2.	apt-get – A package management command-line tool for handling package installations, updates, and removals in Debian-based Linux distributions (e.g., Ubuntu).
3.	install – Specifies that we want to install a package.
4.	docker.io – The package name for Docker, an open-source platform for containerization. The .io suffix is used in Debian/Ubuntu repositories to distinguish it from other Docker-related packages.
Permission denied

  

- Your user didn't have permission to access the Docker daemon socket (/var/run/docker.sock), which resulted in the "permission denied" error when running docker ps.
By running newgrp docker, you switched to a new shell session with the docker group applied, granting the necessary permissions. After that, docker ps worked without issues.
This happens because Docker requires group membership (docker group) to interact with the daemon without sudo.

2 to create docker image there are two ways 
1> create Docker file
2> Docker image pull from docker hub 

 
logs - 

 
$docker run -it uduntu
	$ls 
root@04652c861a74:/ ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
~ local-win
$ docker run -d -t 80:80  nginx
$ docker ps
{ }
Ec2-ip:80 --Done
~Ec2
$ docker run -d -t 80:80 nginx
$ docker ps
{}
Localhost:80 -Done

 

2. dockerfile
Dockerfile -> image -> container
 
 

 

	/app  -  visible?

