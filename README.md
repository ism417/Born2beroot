# Born2beRoot

### Summary
	This project aims to introduce you to the wonderful world of virtualization.

### Virtualization
	Is a technology that allows us to create multiple simulated environments of dedicated resources from a single physical hardware system.

### Virtual machine
	Is a sub computer (guest) with  it own OS, in your computer (host). the hypervisor provide the guest whit the hardware (CPU, RAM, Memory ...) needed,

### Hypervisor
	A hypervisor is software that virtualizes real physical resources and acts as a medium to make them available to virtual machines.
<p align="center">
<img src="Hypervisor-Types.png" style="width:500px">
</p>

### Operating system
	Most of the time, there are several different computer programs running at the same time, and they all need to access your computer’s central processing unit (CPU), memory, and storage. The operating system coordinates all of this to make sure each program gets what it needs. ( it acts as an intermediary between computer software and hardware).
<p align="center">
<img src="OS.png" style="width:500px">
</p>
	When a program makes a call to the OS saying "Yo! i need to use a particular resource", the context switch happens where the user mode switch to kernel mode so that the program can use that resource. So the call that the program make in order to access that resource called System call.

	User and kernel modes are modes of operation where a program can be executed. When a program executing in the Privileged mode(Kernel mode) and it's happens to crash during execution, then the whole system would crash. but it's not the case for the user mode.
<p align="center">
<img src="System-call-working.jpeg" style="width:500px">
</p>

### Debian
	Is an operating system that have a lot of sources whitch make it easier for us to work with it, can run on every architecture available in the market, Support for an extensive list of architectures means that it can run on older and newer computer systems and processors.

#### Difference between Debian & Rocky

#### 🔴Debian
- Debian can be easily upgraded from one stable version to another.

- Supported 32bit.

- Debian uses apt as its package manager.

- Debian has a vast amount of packages in its default repository.

- The mother of many descendant operating systems such as Ubuntu.

#### 🔴Rocky

- it is better to install a new Rocky version rather than go to upgrade the older version, and (this is difficult).

- Does not support 32bit.

- Rocky uses YUM & DNF as its package manager.

- Rocky has limited packages.

- Based on RHEL (READ HAT ENTERPRISE LINUX).

### Aptitude&Apt

	both are package manager a software tools that automates the process of installing, upgrading, configuring, and moving computer programs.

#### 🔴apt

- low-leve.

- Without a user interface.

- New.

- Apt requires a specific command to remove files eligible for a particular package.

- If the action(installing…) is failed the aptitude can suggest other solutions, reverse apt it will say I can't allow you to do that.

- can moo.

#### 🔴aptitude

- High-level.

- With a user interface.

- Old.

- while aptitude removes them automatically.

- We can use apt in aptitude.

- Can't moo.

### Apparmor

<p align="center">
<img src="knight.jpeg" style="width:500px">
</p>
	AppArmor is a Mandatory Access Control (MAC) system built on Linux's LSM (Linux Security Modules) interface. In practice, the kernel queries AppArmor before each system call to know whether the process is authorized to do the given operation. Through this mechanism, AppArmor confines programs to a limited set of resources.
	AppArmor applies a set of rules (known as “profile”) on each program. The profile applied by the kernel depends on the installation path of the program being executed. Contrary to SELinux, the rules applied do not depend on the user, Each profile can be loaded either in enforcing or complaining mode. The former enforces the policy and reports violation attempts, while the latter does not enforce the policy but still logs the system calls that would have been denied.
	for more detiles :https://askubuntu.com/questions/236381/what-is-apparmor
<p align="center">
<img src="apparmor.png" style="width:500px">
</p>

### UFW

<p align="center">
<img src="wall.gif" style="width:500px">
</p>
	UFW (Uncomplicated Firewall) is, as its name suggests, a simple command-line firewall. A firewall is a program that monitors and controls data traffic between a local computer and the network at large. It decides whether to allow or block the traffic according to a set of security rules.
	When we talk about traffic and networks, we must understand two things: IP addresses and ports. On the internet, data is transferred from one computer to the other using their IP addresses, which look something like this: 109.234.160.5.
	But to avoid conflicts between the various internet protocols, every computer separates the access paths thanks to specified ports, marked after the IP address, like this: 109.234.160.5:80 (port #80).

### SSH

	Ssh or (Secure Shell Protocol) is a protocol(a set of rules) that allows 2 machines to communicate securely over a network(Client(Local machine) and Server(Remote machine)). It uses TCP to establish a stable connection and reliable data transfer between the client and the server. It leverages TCP's features such as error checking and congestion control to ensure data integrity and reliability. TCP is a transport layer protocol that manages the individual 'conversations' between web servers and web clients. It ensures data is sent and received in the order it was transmitted and that no data is lost or dropped.
	The significant advantage offered by SSH is the use of encryption to ensure a secure transfer of information between the host and the client.
	Encryption Techniques:
##### Symmetrical encryption
<p align="center">
<img src="sym.png" style="width:500px">
</p>

##### Asymmetrical encryption
<p align="center">
<img src="asym.png" style="width:500px">
</p>
for more detils : https://www.adsmurai.com/en/articles/how-to-generate-secure-ssh-keys

### SUDO

	<p align="center">
	<img src="sudo.gif" style="width:500px">
	</p>

#### the what

	sudo or (super-user do) is a program(group) that allows system administrators to give specific users some permissions of the root such as executing some root’s commands so (make a user most powerful). Not all users could use Sudo only Sudo's group members.
	The root is the user name or account that by default has access to all commands and files on a Linux or other Unix-like operating system. It is also referred to as the root account, root user, and superuser.

#### the why

	It's easy to run only the commands that require special privileges via Sudo; the rest of the time, you work as an unprivileged user, which reduces the damage that mistakes can cause. Auditing/logging: when a Sudo command is executed, the original username and the command are logged.