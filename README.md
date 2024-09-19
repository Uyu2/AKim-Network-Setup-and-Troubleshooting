# Network Step-By-Step Configuration Guide

This guide seeks to offer a step-by-step configuration guide for a Wide Area Network, connected by two Local Area Networks. This represents a relatively basic network, but one that allows internet access, shared information across LAN's, and a network made up of two smaller networks.

These networks also provide multiple real-world use cases. Interdepartmental communication through end devices communicating through a shared router is one example. Through having multiple computers connecting to a switch, connecting eventually then to a router, they can find and send information across their LAN to another department, through their shared access of a central router.

Connected PrintMe printers on university campuses is also a use case. Through connecting to the same WiFi network, or router, a student's wireless access device and the printer can share information, eventually leading to a printed assignment. Sharing a router between switches in this way allows for a WAN that combines smaller LAN's.

1. Choose software and hardware

Software and Hardware chosen should be compatible, and is the first step in creating and configuring a network. Hardware choices include information such as the devices you will use, in this scenario being routers, switches, end devices such as computers, mobile devices, or tablets, cables such as ethernet fiber optic cables, and wireless access points for wireless devices. Choosing between software such as operating systems for Mac or Windows is also important for this step, as configuration for some steps may differ depending on usage of your specific operating system. In this step, it may also help to use a tool such as Cisco Packet Tracer to ensure compatibility and test within a simulation your devices and connections.

<img width="306" alt="Screenshot 2024-09-18 at 10 42 04 PM" src="https://github.com/user-attachments/assets/ca07fcf8-785c-4699-811a-9807219dff07">

2. IP Assignments

Planning IP assignments helps to ensure human error is reduced in the entry of these addresses. For assignment of IP addresses, it is recommended to use static IP's, as this will help to reduce error. You will need to assess the number of devices within your network, and also assign private IP's. These are IP addresses that follow the convention 192.168.x.x, 172.16.x.x. You then need to decide what subnet will be assigned if broken up from the original IP address, as subnets offer better security and organization within larger networks spanning multiple departments. When assigning IP's to devices, also make sure your "first" IP (ex 192.168.0.1) is saved for the default gateway. This practice helps to ensure your default is the earliest possible IP assignment.

<img width="213" alt="Screenshot 2024-09-18 at 10 45 24 PM" src="https://github.com/user-attachments/assets/471aba14-531d-4576-94f1-cdf06cee0a9a">

3. Add end devices

This step entails the first interaction with your hardware. End devices, are essentially the clients of your network. They should be able to communicate with each other once configured through your switch, and serve as the end point to receive and send signals. Devices within this category include laptops, mobile devices, and tablets - they should also have some way to connect to the switch. Whether it be through a wireless or wired connection, they will need to connect to a switch in order to form your Local Area Network. Each device should be configured according to your IP Address. For the sake of simplicity, we will use 192.168.0.0/24 for this example. Your three end devices, laptops, will be assigned 192.168.0.2, 192.168.0.3, and 192.168.0.4. Keep in mind that we are saving the assignment, 192.168.0.1 for the default gateway.

<img width="217" alt="Screenshot 2024-09-18 at 10 45 37 PM" src="https://github.com/user-attachments/assets/c8f71e88-5819-4bc1-811d-bdc3aceaeaba">

4. Add switch

The switch should be in a central location that connects to all of your end devices. It essentially allows a way for your devices to communicate with each other through a Local Area Network. While unable to connect to the internet yet, once we connect the switch to our end devices, we will have a local network of connected devices.

<img width="141" alt="Screenshot 2024-09-18 at 10 45 58 PM" src="https://github.com/user-attachments/assets/9ec89fca-5ba4-48c5-bf85-626fb4eb691c">

5. Connect the end devices to the switch with ethernet cables

Using ethernet cables connecting each end device to a port on the switch, we have now effectively created a local area network. This means that once our IP addresses are assigned and each device is configured, they will be able to communicate through the switch with each other. This is known as a Local Area Network (LAN)

<img width="221" alt="Screenshot 2024-09-18 at 10 46 39 PM" src="https://github.com/user-attachments/assets/ec77c37a-0a5c-43e1-b666-977599bb5f0a">

6. Add wireless devices (if needed)

Optionally, we can add in our end devices that are wireless. While this configuration guide focuses on the use of wired connections, those devices that have a wireless card can connect to a wireless access point, enabling wireless connection within the network. Eventually when a router is inserted into this network, the wireless connection will allow internet access.

7. Add WAP (if needed)

A wireless access point (WAP) is a networking device that will allow the connection of wireless end devices to the switch. Essentially, it creates a point in which these "unwired" devices can wire into the switch, and creates the same functionality as our originally wired devices. This does require more work and connections, as well as a wireless card, but can be integrated into this guide if needed.

8. Connect WAP to a switch (if needed)

Using an ethernet cable, the WAP can then connect to the switch. This connection to the WAP will now enable the devices to act like any other wired device on the network. We can now receive and send signals or packets once everything is configured correctly. 

9. Set IP address on end devices (mobile devices included)

For this example where we are using static IP addresses under the 192.168.0.0/24 naming convention, we now need to assign the proper assignments of IP's to our devices. Our three end devices, 192.168.0.2, 192.168.0.3, and 192.168.0.4, will statically be assigned through their network settings. Since our subnet mask is /24, we have started at .0.2, since the lowest number of our 255.255.255.0 subnet mask is .0.1. We are saving 192.168.0.1 for the default gateway, which will be set up as well in this step.

For each of our devices we can see the assignments below:

Computer 1:

IP Address: 192.168.0.2
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.0.1

Computer 2:

IP Address: 192.168.0.3
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.0.1

Computer 3:

IP Address: 192.168.0.4
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.0.1

<img width="250" alt="Screenshot 2024-09-18 at 10 49 06 PM" src="https://github.com/user-attachments/assets/e3ad7534-690b-43b5-b984-89d67976415b">

For MacOS these settings can be found in the TCP/IP tab under network. After setting IPv4 to manual, this information can be changed.

Similarly, Windows can be found under TCP/IPv4 under network adapter Properties.

As we move into the usage of routers and step outside of LAN's, let's assume that we have a second LAN, with the IP, mask, and gateway assignments listed below:

Computer 1:

IP Address: 172.16.0.2
Subnet Mask: 255.255.0.0
Default Gateway: 172.16.0.1

Computer 2:

IP Address: 172.16.0.3
Subnet Mask: 255.255.0.0
Default Gateway: 172.16.0.1

Computer 3:

IP Address: 172.16.0.4
Subnet Mask: 255.255.0.0
Default Gateway: 172.16.0.1

<img width="197" alt="Screenshot 2024-09-18 at 10 49 25 PM" src="https://github.com/user-attachments/assets/8483c0d2-da27-4c59-9e25-b228ffa3785f">

Now that we have ensured two separate LAN's, we can try to connect the two using a router.

10. Add a router to talk to different networks

To access a Wider Area Network (WAN) or even other networks unconnected to our original switch, it is important to add a router. This router will allow the usage of the internet, access to other connected LAN's, and allow us to have a properly set up WAN. This step relies on our previous steps working as intended, and having our LAN(s) set up with assigned IP addresses.

Before this step is taken on, you should take a moment to ensure that your LAN(s) works as intended. You can ping other devices on your network, test and double check your IP addresses, and ensure that all current end devices can detect each other. 

11. Connect the switches to the router with ethernet cables

Connect both of your switches to the router in this step. This will allow your two LAN's to communicate with each other if you have effectively set up your IP addresses and configurations correctly. You will still need to configure the IP on the router, however.

<img width="945" alt="Screenshot 2024-09-18 at 10 50 47 PM" src="https://github.com/user-attachments/assets/4d76dece-f6df-4d53-a536-6b48e374bf97">


12. Configure IP’s on router

Your router's IPv4 address and subnet mask should now be configured. Which switch it connects to will dictate which default gateway the IPv4 matches with, and how the subnet should interact. Using our example, here is how they should look:

<img width="692" alt="Screenshot 2024-09-18 at 10 51 13 PM" src="https://github.com/user-attachments/assets/d71c567c-5da9-4519-833b-d4923a5ff32a">

<img width="699" alt="Screenshot 2024-09-18 at 10 51 03 PM" src="https://github.com/user-attachments/assets/0f1e5939-e275-4884-bd6f-d1216407ccae">

13. Set port status to on on router

Once the port status on each side is turned on, you should be able to communicate information across the WAN, and from LAN to LAN. You can test this by sending a ping with an end device's IP address across your router to the other side, and gauging if you receive a reply.

The finished network can be seen here:

<img width="893" alt="Screenshot 2024-09-18 at 10 58 39 PM" src="https://github.com/user-attachments/assets/07acccfc-dbd6-43ee-9237-3c611d5a57b9">





# FAQ

1. What do I try if my LAN isn't working?

There are many issues that relate to your LAN not working as intended. Assuming your first LAN is three end devices connected to a switch here are a few different solutions you can try:

- Check the connections between cables and ports
- Pinging each device (computer 1 to 2, computer 1 to 3, computer 2 to 3)
- Check your IP configuration and assignment for typos

Human error makes up a bulk of issues when it comes to setting up a network. Ensuring you have the proper cables connected to the proper ports, network settings such as MacOS's built in firewall are not enabled, and your IP assignments are correct can all help in diagnosing and fixing your LAN issue.

2. How can I test compatibility with the hardware I am choosing?

Cisco Packet Tracer offers a simulation where you can test your hardware, and gain an overhead view of the different connections you are going to be working with. While extremely different in practice, using this application can help you choose applicable and compatible hardware.

3. Apart from my LAN, when I ping end device X, I still don't receive a response. What can I try? How do I diagnose an issue?

While it may be frustrating to not know where your network is going wrong, there is often a very clear reason why issues are arising. Before looking into higher level solutions here are some things to consider and look at:

- Device X has the correct subnet mask, IP Address, and default gateway through -ifconfig and other methods
- Firewall settings on device X
- Try using different cables, to ensure there is not an issue with your cable's hardware
- Checking other devices on the network or WAN to ensure it is not a device specific issue
- Ping using both IP and DNS to diagnose the issue properlu

These are some common solutions that may help in diagnosing how to fix your network and get it up and running.

4. How do I know if I assigned my IP Addresses correctly?

Each device in this static IP scenario should have a unique IP address within the range specified. As long as your default gateway is set, and duplicates do not exist, your IP addresses should be assigned correctly. It is good practice to start your end devices +1 from your default gateway, and +1 from there for each consecutive end device.

Try communicating with your end devices using ping, and if this still does not work, there may be issues with your subnet. Check this to ensure both addresses are correctly, and lastly check the hardware. If all three of these are correct, alongside your default gateway, your LAN should work as intended, unless there are outside factors like a firewall or device-specific issue.

5. I setup everything, why can't my devices communicate with each other?

Again, human error and hardware issues may be the simplest way to check your work.

- Checking cable connections and the correct ports has been the most frustrating but most common issue I have experienced, and it may be necessary to check this
- Verifying network settings such as IP address, subnet mask, and default gateway, alongside firewall settings may be beneficial
- Testing using ping between multiple devices across networks may help to see which devices can communicate with each other
- Swapping out end devices/hardware/cables to ensure there is a network issue, rather than a hardware issue

# Retrospective

Looking back on the process of not only creating and configuring my first network, but also creating a step-by-step guide to recreate it, my retrospective includes many challenges and a new approach to solving these when they come up in the future.

When moving from Cisco Packet Tracer to actual hardware, I realized how different the two were. Main challenges included, actually finding where the configurations on computers were, firewall issues, connecting end devices to the proper ports, and diagnosing issues related to IP addresses outside of a simulation or vacuum. What I realized, however, through this process, is that technology issues are not as “magical” as I first thought. Going through the steps on the slides over and over again and checking for information, I was able to at a certain point, understand where we had gone wrong, and reapplied the information in a way that was able to solve the issue.

Many of the issues were overcome through reframing the solution in our previous simulation, and then trying to find the steps to complete it on the specific computer that was acting as an end device. What I learned from this was that issues within a network are almost always diagnosable, and issues can even tell you where they are going wrong. Rather than looking at an issue, and trying to instantly have the solution, it is better to ask questions and solve from there. Questions like, “Is my default gateway configured?” “Can I ping other devices on the network?” and “Are my IP addresses configured correctly?” Are all possible solutions or variations on the same ping failure issue, and after walking through the issues enough times, I think my biggest insight through this project is my ability to diagnose my own issues.

The biggest improvement or future change I can offer is to not give up so easily when working on a network. A lot of the time when trying to diagnose issues, I felt lost because the solution felt very far away, and in a way I would not be able to solve. My main area for improvement is likely related to a belief and methodology for solving and diagnosing issues, which is something I feel is much more achievable after this project. Through creating a step-by-step guide, I feel I now understand the process of creating a network better, and can diagnose my own issues better if faced with the same hardware.

Many of the issues I took away from this project ended up being the questions I used in my “FAQ” section. I feel that many of the issues I had originally run into with my group, could have been diagnosed with enough effort by ourselves. In the future I seek to be able to bring a solution-oriented mindset to future projects and assignments, even when I may not know the answer. Using online resources, we were able to find information such as where to change an IP address on a Mac, how to properly designate a subnet, and the differences between which computers get which IP addresses. Knowing that we can find the solution to issues, and diagnosing the actual issue is often the hardest part, I will carry this improvement with me into future projects, and I believe that it is also a great insight I gained through this.
