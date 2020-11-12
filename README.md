# arista-cvp-evpn-builder
This is used by Arista CVP to generate EVPN and VXLAN configs.

## Steps
1. You must run the generate_yaml.py builder configlet first. This will generate a yaml file that contains a bunch of device information for actually building/deploying EVPN and VXLAN.
2. After you generate the yaml file, you can then generate the EVPN configs using the generate_evpn.py builder configlet.
3. Next you can generate the VXLAN configs using the generate_vxlan.py builder configlet.
4. Each script will generate a configlet for each device and attach the configlet to the devices. They will append evpn or vxlan to the configlet named after the device.

# Notes:
* These are actual builder configlets for CVP. These have been tested and work on CVP 2020.2.0 or higher.
* These are designed to be ran independently of each other.
