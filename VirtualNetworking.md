## ESXi Basci Network Traffic Explained
![VM Network Traffic](https://user-images.githubusercontent.com/111991325/209737771-87e5f408-5e49-46be-a849-8c46d539be29.png)

#### Key Terms
- vNICs
- Port Groups
- vSwitch
- VMkernal Ports
- 


#### Key term relation
 1. Hosts (indivdual VMs) use vNICs -> 
 2. VM vNICs are assigned to Port Groups that are defined with VLANs on the vSwitch(vShpere Standard Switch or Distributed Switch) -> 
 3. Port Groups are linked to a VMNIC which servers as an uplinks to the physical switch in the network (best practice to aggregate links on) 

Notes: VMkernel Ports are port on the vSwitch used for special traffic (not host traffic) such as Management, Stroage, vMotion, this is how vCenter and the hosts communicate. 
