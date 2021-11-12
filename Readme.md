# An Introduction to Firewall

        You cannot cross a "wall of fire", but Hackers can.

Hey Reader! Hopefully, you were looking for an article that will help you to understand the Firewall concept. Right? If so, you are at the right place. Let's start with the basic discussion first.

![Fig1.1 image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS2P0hXdbSCpRW_xtz4GeTpdowmBKxPYbVUqA&usqp=CAU)

## What is Firewall ?

---

An introduction to a firewall is essential for a beginner. If you are not a beginner, just skip this paragraph. A Firewall as the name suggests is that it is a barrier to protect computer systems and networks from outside attacks. The answer to the question ‘**What is a Computer Firewall?**’ The purpose of a Firewall is to act as the first line of defense in network security. You can define a Firewall as a network security system that acts as a barrier between internal network and external sources like the internet to intercept and block data packets that don’t conform to its set of rules. Okay, Did you notice the term "**Data Packet**"? Don't worry about it. We will talk about it later in the article.

_A firewall is a [network security](https://en.wikipedia.org/wiki/Network_security) hardware device or a program in our computer itself that monitors incoming and outgoing network traffic and permits or blocks data packets based on a set of security rules. Its purpose is to establish a barrier between your internal network and incoming traffic from external sources (such as the internet) in order to block malicious traffic like viruses and hackers._

I Hope now you have a basic idea of What is Firewall and its the purpose? Okay then, Let's make you a **PRO !!**.

## Need of Firewall

---

Everyone loves to interact with the internet. But it also enables the outside world to interact with the internal network of the individual. This creates a threat to the security of either individual or an organization. To secure the internal network from _unauthorized traffic_, we need a Firewall.

## How does Firewall Works ?

---

Let's knows how firewalls protect us to become a victim of hackers. Internet is the source of an untrusted networks. Whenever we send a request for accessing a website from our computer to the network, the internet will give us a response to our system. But sometimes hackers get access to this network connection using some [network attacking techniques
](https://en.wikipedia.org/wiki/Network_security "Network security") and try to steal our information, but the firewall protects us from these malicious users called hackers.

![image](https://media.geeksforgeeks.org/wp-content/uploads/introduction-to-firewall-1.png)

* [_Fig 1.2: link to the image shown above_](https://media.geeksforgeeks.org/wp-content/uploads/introduction-to-firewall-1.png)

The Firewall maintained a list of some allowed and not allowed computers in the network already based on Internet Protocol (IP) addresses, protocols, and ports. If someone makes a request to the network and is not allowed the computer tries to send the response then the firewall blocks that response in between is list-based filtering is called [Packet Filtering](https://www.jigsawacademy.com/blogs/cyber-security/packet-filtering-firewall/ "Jigsawacademy.com").
The Firewall also knows which website is currently user using. So if a hacker tries to send some additional information with the required response firewall will be blocked such activities. This type of inspection is known as [Stateful Inspection](https://www.techtarget.com/searchnetworking/definition/stateful-inspection "techtarget.com").

* [Additional Reference: How Firewall Works with ruleset?](https://www.geeksforgeeks.org/introduction-of-firewall-in-computer-network/)

## Types of Firewall

---

1. Packet Filtering Firewall
2. Proxy/Application Firewall
3. Hybrid Firewall

Let's discuss one by one :

1. ### **Packet Filtering Firewall**

 Suppose we want to download some file of size 500Mb from the network, then it will download in chunks in form of a data packet instead of the whole at a time. Did you notice the word "**data packet**"? Yes, it's time to know it.

![data packet](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7WX4GRUsofSNDoisbWkh_f8K6qm7pluCpag&usqp=CAU)

**A Data packet is a bit of data that is packaged for transmission over a packet-switched network. It is a small amount of data sent over a network, such as a LAN or the Internet.**

A typical packet includes two sections, a header, and a payload. The header stores information about the packet, IP of the sender, the receiver of packet, Port number, etc. while the payload section of a packet contains the actual data being transferred.

Let's continue with our 500Mb file which receives in the local machine in form of the data packet. Before reaching the computer firewall verifies these data packet using an access list  and allow only those packets which are good to go.

Packet filtering is generally performed by a device like router.

### Limitations of packet filtering

 Packet filtering is less secure because it only checked the header part of the data packet and leaves the payload part as it is. An intruder can send some malicious information with the payload part.
</br> </br>

2. ### **Proxy/Application Firewall**

 Suppose your mother asks you to buy a pen for her. You will buy a pen from a shopkeeper and give it to your mother and shopkeeper even don't know who will use it. Now replace these real-world obejcts with a technical terms as:

Real Object| - | Terms
----------|--|------------
Mother |->|Local machine
You    | ->|Proxy Machine
Shopkeeper |->| Internet

Whenever someone made a request using the local machine, a proxy machine will be in between the local and the internet network which will take a request from the local machine send that request to the internet, and the internet will return a  response to the proxy machine and proxy then be sent to the local machine. So no computer on internet network will know which system used the response.

### Limitation of proxy firewall

 The proxy firewall is more secure than packet filtering because it checked the header part of the data packet as well as the payload part. This inspection will make it more secure. But the limitation is, it makes the verification  process of data packets slower than packet filtering.

3. ### **Hybrid Firewall**

 A Hybrid firewall is a combination of both packet filtering and a proxy firewall. In a Hybrid firewall either we connect these firewalls in parallel or series. But Wait! I have a question for you: If there have two different tracks to reach Bengaluru parallelly and police blocked one of the routes. Can you reach the city? Your answer might be - Yes, But what if we have only 1 route with 2 different check-posts. Will you make it now? The answer is no because now the security is higher. The Same thing happens with a hybrid firewall if we connect the packet and proxy firewalls in parallel then one of the firewall become redundant. So instead of using them in parallel use them in series so that it provides more security.

You can also watched the topic on youtube in case you need a better visual explanation with the topic:

 [![IMAGE ALT TEXT HERE](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQd4on3MXL-xAFSFtFeb-JkNOa1ZHfHGnXogQ&usqp=CAU)](https://www.youtube.com/playlist?list=PLBbU9-SUUCwV7Dpk7GI8QDLu3w54TNAA6)

## **Firewall Classification based on Usages**

---

Do you know which firewall we should use?

Well, it depends upon the _implementation environment_ of the firewall. We use some numbers to repersent which one is recommended for different usages:

Code | Description
--------|--------
0 | Unacceptable
1|Minimal Security
2|Acceptable
3|Effective
4|Recommended

Let's discuss it with a few example types:

Firewall Architecture (If any one of applicable) | High-Risk Environment (Hospital)| Medium-Risk Environment (University) | Low-Risk Environment (Florist shop)
--------|--------|----|--------|
 Packet Filtering | 0 | 1 | 4
Proxy | 3| 4| 2
Hybrid|4|3|2

## **Limitations of Firewall**

---

Everything has a positive and negative side. Isn't it? Yes, it is good to know that a Firewall protects us from malicious attacks. Yet it has a few limitations as well. Let's check out the following content below:

* We know Firewall only allows the  allowed section's data packets and blocked the not-allowed data packets from the access list. But a hacker can create a fake data packet with the trusted IP address and the firewall will ignore it.

* Insider's intrusion: If a hacker is already present in a public network and someone uses that network then the intruder can steal the information and the hardware device for the firewall will not be able to detect that.

* Direct Internet Traffic: If you ever tried to install the Utorrent software, you found a checkbox Add an exception for Utorrent in window firewall shown in picture below :

   ![Utorrent](https://static.packt-cdn.com/products/9781849698269/graphics/8269_01_07.jpg)

   So if we checked that checkbox, hackers can send malicious data through the firewall without its awareness.

* Firewall trusts on the trusted network, an intruder can you trusted network to attack the system.

* Firewall just provides safety based on the access list. It doesn't provide us with anti-virus or anti-malware facilities.

So it is always better to use a trusted anti-virus or anti-malware software.

### Let's do comparison between software firewall vs Hardware device firewall

## **Hardware Firewall vs Software Firewall**

---

**Software Firewall** |**Hardware Firewall**
-------------|---------------------
Software Firewall operates on the system. |Hardware Firewall does not operate on the system.
Configuration of a software firewall is easy. |Configuration of a hardware firewall is not easy.
It is more expensive.| It is cheaper than a software firewall.
It is flexible i.e., you can choose which application has to be installed. | It is not flexible like software firewall.
It is installed inside the individual system.|It is installed outside the system.
It protects one system at a time.|It protects a whole network at a time.
It makes the performance of computers slows down.|It doesn’t affect the performance of the computer.
It has needed to be installed on every individual system on a network.|It needs only one hardware to be installed for a whole network.

#### **Point to Remember**

---

If we noticed the main difference is to use a hardware firewall is it secures the whole network instead of a single computer.

* [Reference to above difference table](https://www.geeksforgeeks.org/difference-between-hardware-firewall-and-software-firewall/ "GeeksForGeeks")

Whoo-whoo Finally !! you made it. Congratulations!! for completion of the article. Now you know about firewall pretty well. I hope you enjoyed it.

                Thank you for reading the article. 

                                    Author : Hitesh
                                    Month  : Nov'21
</br></br></br>
Here are few more references to learn more about firewalls:

---

* [Jigsawacademy: What is firewall?](https://www.jigsawacademy.com/blogs/cyber-security/what-is-firewall/ "jigsawacademy")

* [ForcePoint: Explore firewall.](https://www.forcepoint.com/cyber-edu/network-security "forcepoint")

* [Wikipedia: Network Security](https://en.wikipedia.org/wiki/Network_security)

* [Geeksforgeeks: Introduction of Firewall in Computer Network](https://www.geeksforgeeks.org/introduction-of-firewall-in-computer-network/ "geeksforgeeks")
