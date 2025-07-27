# Lab 1 - Basic Network Configuration

Lab 1 can be viewed by this video also by Tannet [Basic Configuration Network](https://youtu.be/1KPyAQNhztM?si=yyiC17rB1gPn6xUR)

We will use 4 PCs, 2 Switches and 1 Router

PCs of PC-PT, Switches of 2960-24TT and Router of 1941

To connect all the PCs to Switches, use the Copper Straight Through wires and connect them through Fast Ethernet

To connect Switches with the router, use the same wires but connect through Gigabyte Ethernet

As the red flags from switches to router indicate that no connection has been established, so we have to configure to make the connection

Click on the router and go to the CLI (Command Line Interface) Mode.

It asks Would you like to enter the initial configuration dialog? [yes/no], which will we do no and press Enter. We will get Router> to write our commands

Write `enable` and then `configure terminal` so we can configure our network globally

As we want to configure the connection between switche and router and its of Gigabyte Ethernet as g0/0 then write `interface g0/0`

Assign the IP address of the switch with subnet mask as `ip address 192.168.1.1 255.255.255.0`

Then write `no shutdown`

The result says that the changed state to up meaning this port has been configured, press Enter

Then `exit` to get back with the global configuration and then configure the other Gigabyte Ethernet device g0/1

`interface g0/1`

Assign the IP address with subnet mask `ip address 192.168.2.1 255.255.255.0`

Then write `no shutdown`

<img width="488" height="287" alt="image" src="https://github.com/user-attachments/assets/3f8b8936-d490-4a12-8699-a84295b2d0b6" />

<img width="327" height="201" alt="image" src="https://github.com/user-attachments/assets/bb9e58eb-310e-41c4-95a0-6662582fcd1e" />

No we will configure the PCs, with the fisrt PC, go to the Desktop and click IP Configuration

Set the following details:
- IP Address: 192.168.1.10 (you can use anything)
- Default Gateway: 192.168.1.1

Set the IP Configuration of other PC with Switch 1 will have different IP address like 192.168.1.11 and same Default Gateway

The other two PCs with other switch will IP addresses like 192.168.2.10 and 192.168.2.11 and Default Gateway will be 192.168.2.1 as the two switches indicate of two sub networks.

So all the connections have been made and test the connections by sending messages within the same network and across the network which will result in Successfull

<img width="428" height="78" alt="image" src="https://github.com/user-attachments/assets/1a1a3d28-ada7-45bc-be67-5dcc867a5e5c" />
