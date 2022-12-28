## ESXi Network Traffic Explained
![VM Network Traffic](https://user-images.githubusercontent.com/111991325/209737771-87e5f408-5e49-46be-a849-8c46d539be29.png)

### Key Terms
- vNICs
- Port Groups
- vSwitch

 1. Hosts (indivdual VMs) use vNICs -> 
 2. vNICs are assigned to Port Groups that are defined on the vSwitch(vShpere Standard Switch) -> 
 3. Port Groups are linked to a VMNIC as an uplink to the physical switch in the network (best practice to aggregate links) 

