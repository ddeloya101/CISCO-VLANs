# CISCO-VLANs
In this tutorial, we will be creating a VLAN (Virtual Land Area Network) in the CISCO CLI.

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

That's it! You have successfully created a VLAN on a Cisco switch using the CLI. Remember to adjust the commands according to your specific network setup and VLAN requirements.
