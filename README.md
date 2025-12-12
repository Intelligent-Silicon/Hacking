# Hacking

Arguably the perfect hack is one where you can gain persistance. 

What I mean by this is, being embeded in a device beit a computer, phone, network device like a network printer, Smart TV or what have you.

These pages will discuss what I think are the best ways.


### Persistance

Persistance is a method where hackers can constantly get their malware reinstalled.

It can use techniques like infecting a chip with malicious firmware in the bios or network device or reinstalling software that has a genuine use case because corporate law prevents reverse engineering.

Infecting a programmable chip like a BIOS chip is a useful vector because there is always space on the chip for future updates which are larger in size. This spare space can then become a weakness. Early programmable chips, had a quartz window which was covered up with a sticky label to prevent UV light from erasing the firmware. The chip then had to be placed on a chip writer where the firmware was downloaded onto the chip before the chip was placed back on the circuit board.

Today modern circuit boards often enable chips to be reprogrammable from within the operating system, or by initiating a special boot mechanism/mode when the device is switched on which then enables the firmware to be reprogrammed. The need to remove the chip from the circuit board no longer exists, which is convenient, and whats convenient for you is also convenient for hackers.


### Zero days

Zero days are bugs or malicious bits of code built into firmware or software. Typically one zero day on its own wont cause the world to end, but string a number of zero days together can cause the world to end. This is why updating and patching firmware and software is important. Quite often your firmware or software is relying on a single or few individuals to have got the job right. This also makes them high value actors. The business would hopefully have code reviews before deployment by at least one other knowledgeable person familiar with the code being produced, the task the code is expected to perform and the risk factors for the code not being up to scratch. This could be outsourced but is typically performed inhouse using a variety of methods, before eventually the code is deployed to testers familiar with the expectations of the code. Obviously scale is an advantage, but with scale comes new risks in todays global world, but those risks also affect large businesses in other ways.

Another way to test for bugs in code is to bring in 3rd party solutions that are hopefully already tested, deployed and in use elsewhere. This limits the risks somewhat provided the 3rd party supplier can be trusted, but being able to view the source code always helps to allay fears. This is one of the major selling points of the Open Source world, all the source can be viewed by everyone, in practice this hasnt happened in the past and may not happen in the future. A good example of this failure was the HeartBleed attack https://en.wikipedia.org/wiki/Heartbleed
This bug also demonstrates that you dont always need to string multiple zero days together to gain control over systems, because in this case the openSSL security algorithms were heavily relied upon, instead of mixing up the use of TLS with different providers like GnuTLS, Mozilla's Network Security Services, or Microsofts Windows platform implementation.

Stringing together a number of zero days which are often seen as minor can heap rewards, this is why the legend exists that seemingly inconsequential bugs fetch far higher rewards on the dark web, than the big tech companies would typically pay out in bug bounties.

Whilst test automation frameworks exist to test code, one other factor is stress testing or load testing. Software needs to be able to handle the workload otherwise it can fall over or crash. A common example will be firewall code that manages the sessions between internet users and services behind the firewall. Some servers can only handle some many external users before the resources of the device are exhausted. This is what Distributed Denial of Service (DDOS) attacks try to exploit. The highest recorded throughput for a DDoS attack reached a peak of 29.7 terabits29.7 terabits per second (Tbps), mitigated by Cloudflare in Q3 2025. This attack was attributed to the Aisuru botnet. 

So to break this down, there appears to be a number of devices which are compromised and form a botnet (a network of robots) capable of transmitting data to a target in order to overwhelm it. The media will portray this as home users, but a military may also have agrrements in place with their telecom providers to provide additional services. Ultimately a useful idiot or group of useful of idiots will be the fall guys, after being being expertly manipulated by the real hackers. The ego's of the useful idiots could also prevent them from admitting there werent authors of malicious code or tools. 

This is like a crowd of people entering a small shop and the shopkeeping being overwhelmed resulting in members of the crowd being able to steal some of the goods for sale. Improvements in technology, like super fast fibre optic connections, make these attacks possible in greater and greater numbers resulting in a peak of nearly 30 terabits per second. 30 terabits is 3,750,000 Megabytes. You 1 Gigabit internal network is about 125 Megabytes for context. Obviously some of the commercial network hardware can handle faster speeds than your typical home or small business network, but will also operate in parallel ie side by side, its very unlikely any single piece of hardware had to handle that sort of workload. And this is where distributed code handles the workload directing traffic to the relevant servers and services. These system are highly optimised but importantly they are designed to share the workload with some communication to bring new devices online much like a company will order new agency staff to help out during busy times. 
