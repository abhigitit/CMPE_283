CMPE 283, Assignment – 2

Q1) Ans) Assignment is done by Abhiteja Mandava(015786550) and Sai Santhosh Yamsani(015386683)
Santhosh worked on the the logic in the vmx.c file and also the basic set up while I worked on the cpuid.c file and the set up.
We both have worked on the two instrcutions.
Q2) Ans) Make sure you set up the environment in the first assignment before you begin. 

The CPUID exit handler code in and cupid.c and vmx.c should be changed. KVM Hypervisor changes can be made in the arch directory. Our two directories are linux/arch/x86/kvm/vmx/vmx.c and linux/arch/x86/kvm/vmx/vmx.c. 
linux/arch/x86/kvm/cupid.c 

0x4FFFFFFF is the first instruction. When the exit equals the 0x4FFFFFFF instruction, we need to know the total exits of all types. Using an if condition, we may do this by incrementing it by 1 anytime the instructions equal the value. 

In vmx.c, use u32 to create a global variable total exits and increase its value by one. To minimize the error undefined total exits, you must use EXPORT SYMBOL. 
Use extern in cupid.c to make variables like EXPORT SYMBOL more visible. To equal eax, create an if condition.

The second instruction, 0x4FFFFFFE, can now be used. In this case, we must calculate the overall time spent on low and high cycles. The rdtsc() function, which is a time stamp counter, can be used. 
Carry out the actions below. 
As before, use u32 and EXPORT to create a global variable total time in vmx.c. Give the rdtsc() function the initial time parameter. Calculate total time by subtracting the initial time from rdtsc at the exit handle index of the kvm function (). Because this number varies as we begin and the code runs. 
Initialize the else if condition under the first instruction in cupid.c. We'll also use an extern long for total time because we'll be printing it. We need to determine high 32 bits for ebx, thus total time right shift 32 is ebx, and low 32 bits for ecx, so write the criteria accordingly. 

 Now, execute the following commands to create it: 
$ make install modules 
$ make modules install
$ make INSTALL_MOD_STRIP=1 modules_install && make install
$ lsmod | grep kvm
$ modprobe kvm
 
 
'cpuid' is an Ubuntu package that provides detailed information on the CPU(s) via the CPUID instruction. 
To install it, use this command. 
$ sudo apt-get install cupid 
