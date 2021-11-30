Q1) Ans) Assignment is done by Abhiteja Mandava(015786550) and Sai Santhosh Yamsani(015386683) Santhosh worked on the the logic in the vmx.c file and also the basic set up while I worked on the cpuid.c file and the set up.
We both have worked on the two instrcutions.
Q2) Ans) Make sure you set up the environment in the first and second assignment before you begin.

The CPUID exit handler code in and cupid.c and vmx.c should be changed. KVM Hypervisor changes can be made in the arch directory. 
Our two directories are linux/arch/x86/kvm/vmx/vmx.c and linux/arch/x86/kvm/vmx/vmx.c. linux/arch/x86/kvm/cupid.c

Q3: Comment on the frequency of exits – does the number of exits increase at a stable rate?
Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail?

Ans)External Interrupt Exit, Interrupt Window Exit, Control-register access exits, and IO Exits are just a few of the exits and he number of exits does not grow at a constant rate. 
External Interrupt Exit, Interrupt Window Exit, Control-register access exits, and IO Exits are just a few of the exits. Using dmesg, the total exits after boot up are 515,155. 

Q4: Of the exit types defined in the SDM, which are the most frequent? Least?
External Interrupt(1), CPUID(10), Control-register accesses(28), I/O instruction(30), and a few others are common in my scenario. 
The least are MOV DR(29), Exception(0), APIC access(44) etc.
