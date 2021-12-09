Working assignment 3 is a prerequisite for assignment 4.

1. Executed assignment 3 code and used it to boot the inner VM.
2. Using a series of queries of CPUID leaf function 0x4FFFFFFD, capture total exit count information (total count for each type of exit handled by KVM) once the VM has booted. (The cpuid command's -l option indicates the leaf node(eax value), whereas the -s option specifies the subleaf node(ecx value)).
 - $cpuid -l 0x4ffffffd -s{exit_type}
3. Use the command $sudo rmmod kvm-intel to remove the 'kvm-intel' module from your operating kernel.
4. Reload the kvm-intel module with the ept=0 and vpid=0 parameters (this will disable nested paging and force KVM to use shadow paging instead). $insmod /lib/modules/5.15.0+/kernel/arch/x86/kvm/kvm-intel.ko is the command to use. ept=0 vpid=0
5. Rebooted the same test VM and used a series of queries to record total exit count information (total count for each sort of exit handled by KVM).

