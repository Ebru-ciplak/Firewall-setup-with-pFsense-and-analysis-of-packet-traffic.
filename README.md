# Firewall Setup With PfSense and Analysis of Packet Traffic.
## _About Firewall_

**Firewall is a wall between the internet and us users today and it is intended to provide security. The software or devices that are responsible for stopping all malicious attacks that may come to our device over the internet and manage our connection with other network devices that will communicate with us in accordance with the rules we have previously determined are called Firewall.**
**Firewalls are a filter between the internet and the user, we can say. The internet comes directly to the firewall, and the content that is allowed to pass through is filtered and shown to us.**
**If we look at the network scope, firewalls DROP incoming network packets that they detect as harmful. That is, they do not pass them in any way, they completely block them. And they do not return any response to the IP owner who sent the packet.**

## _About PfSense_

**PfSense is a Firewall distribution and is FreeBSD Based. With PfSense, we can protect our devices against attacks that may come from an internet connection. You can restrict the pages that users in your network can access. We can make time restrictions. We can block certain applications.**

**In our project, we first uploaded the PfSense ISO file on VMW.Since PfSense runs on the FreeBSD operating system, we click the other option in our virtual machine. We choose FreeBSD as the version. Then we write 40GB instead of 20GB in the Max Disk Size section. Then we click on the Customize Hardware option. In this section, we first select the memory as 256MB. We write 2 in the Processors section and tick the Virtualize Intel option. In the next step, we install the ISO file that we downloaded. The network adapter part is important. Since there should be 2 adapters in this part, the first adapter will be NAT. For the other adapter, we choose Bridged. We have uploaded our ISO file to the virtual machine.**
 * _PfSense IOS FILE Uploaded and customize on VMW_ 

![1WMV kurulum](https://user-images.githubusercontent.com/80758830/121806591-27fd4f00-cc59-11eb-9c58-62642fcbca15.gif)

 * _PfSense Uploaded on VMW_ 

**First, we run our virtual machine with FreeBSD operating system. In this part we will need to perform some installation process. In the Copyright and distribution notice section, we click the Accept option. Click on PfSense Install and continue. Select to Continue with default keymap. OK to Auto (UFS) BIOS. Then some installation process is performed. Click No for Manual Configuration. Click on the Reboot option and complete this part.**

![2 sanala pfsense yükleme](https://user-images.githubusercontent.com/80758830/121807481-030adb00-cc5d-11eb-8389-1f3e2c0827e1.gif)

* _PfSense Setup in System Prompt_


**First, we type ipconfig in the command prompt. In this section, it is important to learn our IPv4 and Default Gateway addresses. Then it asks us to choose option for PfSense loading screen in console. We choose 2 for the installation and we choose 2 again because we will operate over the LAN. It then asks us for our IPv4 address. We write our IPv4 address in this part. Then it asks us to select bits from 1 to 31. We choose 24. In the next step, we write our IPv4 address again. It asks if I want to define IP version 6. Leave it blank and press enter. It asks if I want to open a DHCP server on the LAN leg, and we click Y. We choose Y for the WebConfigurator question. Finally, we click ENTER.**

![3 konsola pfsense kurulum](https://user-images.githubusercontent.com/80758830/121808933-7879aa00-cc63-11eb-9dec-c1ead24897cf.gif)


* _PfSense Web Interface Settings_

**First I opened wifi settings to change adapter options. I disabled and reconnected the wifi 4-5 times. Thus, my uploads will be defined.I connected to the pfSense interface with my web browser at http://192.168.1.140. When I entered the address, the PfSense login page appeared. I typed admin for username and pfsense for password. We accepted the text that came out and continued. The installation interface comes up, we continue with next. We set the dns servers that pfsense will use. For Primary DNS Server we write 8.8.8.8 and for Second DNS Server we write 8.8.4.4. We enter my time settings and choose Istanbul. On the page that appears, click Next and continue. It wants us to set my lan leg, we already made the lan leg settings on the console. We continue with Next. It asks us to create a new password so I enter a new password. We call reload for the settings we made to be valid. And my pfsense installation completed successfully.**

![4 ağ ayarları](https://user-images.githubusercontent.com/80758830/121808712-7a8f3900-cc62-11eb-97c7-dac5d37cd5c2.gif)

**And pfsense installation completed successfully. As you can see,our wan and lan interfaces are working.**

![DASHBOARD](https://user-images.githubusercontent.com/80758830/121812710-a49c2780-cc71-11eb-9425-fc200a6a0a01.png)

![ntop](https://user-images.githubusercontent.com/80758830/121812715-a9f97200-cc71-11eb-83b0-6fdcc3e73589.png)








