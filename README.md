# Creating VLANs with CISCO
In this tutorial, we will be creating a VLAN (Virtual Land Area Network) in the CISCO CLI.
<p align="center">
<img src="https://i.imgur.com/QF54hvv.png" width = "370" height= "200">
</p>

What are VLANs? A VLAN (Virtual Local Area Network) is a virtual network infrastructure that allows you to logically segment a physical network into multiple isolated networks. It is created by grouping devices together based on certain criteria, such as department, function, or security requirements, regardless of their physical location within the network.

Here is a step-by-step guide to creating a VLAN on Cisco CLI (Command-Line Interface):

1. Access the Cisco CLI: Connect to the Cisco switch or router using a terminal emulator application (e.g., PuTTY, Terminal). Enter the appropriate credentials to access the command-line interface.

2. Enter privileged EXEC mode: Type `enable` and enter the privileged EXEC mode password to access administrative privileges.

3. Enter global configuration mode: Type `configure terminal` or `conf t` to enter global configuration mode.

4. Create the VLAN: To create a VLAN with a specific VLAN ID (for example, VLAN 10), use the following command:

   ```
   vlan <vlan-id>
   ```

   Replace `<vlan-id>` with the desired VLAN ID. For example, to create VLAN 10, you would enter `vlan 10`.

5. Assign a name to the VLAN (optional): To assign a descriptive name to the VLAN, use the following command:

   ```
   name <vlan-name>
   ```

   Replace `<vlan-name>` with the desired name for the VLAN. For example, to name VLAN 10 as "Sales," you would enter `name Sales`.

6. Assign ports to the VLAN: To assign switch ports to the newly created VLAN, use the following command:

   ```
   interface <interface-type> <interface-number>
   switchport mode access
   switchport access vlan <vlan-id>
   ```

   Replace `<interface-type>` and `<interface-number>` with the specific switch port you want to assign to the VLAN. For example, `interface GigabitEthernet0/1` selects GigabitEthernet port 0/1.

   Replace `<vlan-id>` with the VLAN ID to which you want to assign the port. For example, to assign VLAN 10, you would enter `switchport access vlan 10`.

   Repeat this step for each port you want to assign to the VLAN.

7. Exit interface configuration mode: Type `exit` to exit the interface configuration mode.

8. Verify the VLAN configuration: To verify the VLAN configuration, use the following command:

   ```
   show vlan brief
   ```

   This command will display a summary of the VLANs configured on the switch, including the VLAN ID, name, and associated ports.

9. Save the configuration: To save the configuration changes, use the following command:

   ```
   write memory
   ```

   Alternatively, you can use the shortcut command `copy running-config startup-config` or `copy run start`.

That's it! You have successfully created a VLAN on a Cisco switch using the CLI.
By leveraging VLANs, network administrators can efficiently manage and control network traffic, enhance security, improve performance, and adapt to changing network requirements. VLANs are a fundamental tool for network segmentation and play a crucial role in modern network architectures. Remember to adjust the commands according to your specific network setup and VLAN requirements.

<div> What are some advantages a network has by leveraging VLANs? </div>
<div> <b>Segmentation: </b> Separate devices into different networks for better performance, manageability, and security. </div>
<div> <b> Security: </b> Isolate sensitive resources and restrict communication between devices. </div>
<div> <b> Broadcast Control: </b> Limit broadcast traffic to each VLAN, improving network efficiency and stability. </div>
<div> <b> Quality of Service (QoS): </b> Prioritize traffic and ensure a consistent user experience. </div>
<div> <b> Flexibility and Scalability: </b> Easily add, move, or modify devices without rewiring the network. </div>
<div> <b>Virtualization: </b> Create isolated virtual networks within a shared infrastructure. </div>
<div> These VLAN benefits enhance network performance, security, efficiency, and flexibility. </div>
