# CMPE_283

1) Abhiteja Mandava(015786550) worked on MSRs : IAM_VMX_PROCBASED_CLTS, IAM_VMX_PROCBASED_CLTS2
Sai Santhosh(015386683) worked on MSRs : IAM_VMX_EXIT_CLTS, IAM_VMX_ENTRY_CLTS

2)
Installed all development tools to build a kernel

Step 1:
VM ware--Go into properties for the virtual machine, underneath CPU, there is a checkbox enable nested hardware assisted virtualization (here we are running hypervisor insdie a hypervisor)

Check after step 1:
To check if we have nested virtualization done properly cat /proc/cpuinfo
If we can see vmx flags, it means this vm has hardware assisted virtualization .
If we are running it on bare hardware, these vmx flags will be present by default without actually creating a vm..

step 2: Enter command free to know the memory.

Step 3:
Enter command htop to know how many cpus are assigned.

Step 4:
Download kernel source code
github.com/torvalds/linux

Step 5: Fork the linux source code

Step 6:
Fabricate the file cmpe283.c according to the requirements in the question.(We did our coding in init_module(void))

Step 7:
Copy pin based capabilities from SDM and enter in the code accordingly.

Execute the code and view the message outputs for PINBASED, PROCBASED, PROCBASED2, EXIT and ENTRY features on the terminal.
