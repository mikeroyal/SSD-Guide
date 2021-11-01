
<h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/139736353-e57ed239-8ec4-464a-9da7-203e604abcce.png">
  <br />
  Solid-State Drive (SSD) Guide
</h1>

#### A guide covering  including the applications, libraries and tools that will make you a better and more efficient with your powered device.

**Note: You can easily convert this markdown file to a PDF in [VSCode](https://code.visualstudio.com/) using this handy extension [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf).**

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/139736361-753bbc0b-76a8-471b-b721-f53793b9f029.png">
<br />
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/139736363-a4776914-aa56-41be-af3d-0ea38bf72fbe.png">
<br />
 Solid-State Drive (SSD) Architecture.
</p>


# Table of Contents

1. [SSD Learning Resources](https://github.com/mikeroyal/SSD-Guide#SSD-learning-resources)

      - [System Memory](https://github.com/mikeroyal/SSD-Guide#System-memory)
      - [SSD Interfaces](https://github.com/mikeroyal/SSD-Guide#SSD-interfaces)
      - [PCIe Protocols](https://github.com/mikeroyal/SSD-Guide#PCIe-protocols)
      - [Fabrics](https://github.com/mikeroyal/SSD-Guide#Fabrics)

2. [File systems & Storage](https://github.com/mikeroyal/SSD-Guide#file-systems--storage)

3. [Virtualization Tools](https://github.com/mikeroyal/SSD-Guide#virtualization-tools)

4. [Emulation Tools](https://github.com/mikeroyal/SSD-Guide#emulation-tools)

5. [Firmware Development](https://github.com/mikeroyal/SSD-Guide#firmware-development)

6. [Verilog/SystemVerilog Development](https://github.com/mikeroyal/SSD-Guide#VerilogSystemVerilog-development)

7. [Assembly Development](https://github.com/mikeroyal/SSD-Guide#assembly-development)

8. [C/C++ Development](https://github.com/mikeroyal/SSD-Guide#cc-development)

9. [Electric charge, field, and potential](https://github.com/mikeroyal/SSD-Guide#electric-charge-field-and-potential)

     - Charge and electric force (Coulomb's law): Electric charge, field, and potential
     - Electric field: Electric charge, field, and potential
     - Electric potential energy, electric potential, and voltage: Electric charge, field, and potential

10. [Circuits](https://github.com/mikeroyal/SSD-Guide#Circuits)

    - Ohm's law and circuits with resistors: Circuits
    - Circuits with capacitors: Circuits

11. [Magnetic forces, magnetic fields, and Faraday's law](https://github.com/mikeroyal/SSD-Guide#magnetic-forces-magnetic-fields-and-Faradays-law)

    - Magnets and Magnetic Force: Magnetic forces, magnetic fields, and Faraday's law
    - Magnetic field created by a current: Magnetic forces, magnetic fields, and Faraday's law
    - Electric motors: Magnetic forces, magnetic fields, and Faraday's law
    - Magnetic flux and Faraday's law

12. [Electromagnetic waves and interference](https://github.com/mikeroyal/SSD-Guide#electromagnetic-waves-and-interference)

    - Introduction to electromagnetic waves: Electromagnetic waves and interference
    - Interference of electromagnetic waves


# SSD Learning Resources
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[Solid-State Drive (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive) is a solid-state storage device that uses integrated circuit assemblies to store data persistently, typically using flash memory. SSDs store data in semiconductor cells. where cells can contain between 1 and 4 bits of data. Starting with **single-bit cells ("Single Level Cells" or "SLC")** is generally the most reliable, durable, fast, and expensive type, compared with **2- and 3-bit cells ("Multi-Level Cells/MLC" and "Triple-Level Cells/TLC")**, and finally **quad-bit cells ("QLC")**.

[Solid State Disk - Disk Partition Schema | Coursera](https://www.coursera.org/lecture/windows-os-forensics/solid-state-disks-tHvMt)

[Disk Schedulers for Solid State Drives (PDF)](http://gauss.ececs.uc.edu/Courses/c4029/code/files/SSD_disk_scheduler.pdf)

[Introduction to Storage and Peripherals | Linkedin Learning](https://www.linkedin.com/learning/comptia-a-plus-220-1001-cert-prep-4-storage-and-peripherals/introduction-to-storage-and-peripherals)

[SATA vs SSD vs NVMe: Types of Hard Drives | Pluralsight](https://www.pluralsight.com/blog/it-ops/types-of-hard-drives-sata-ssd-nvme)

## System Memory
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[NAND Flash](https://en.wikipedia.org/wiki/NAND_Flash) is a type flash memory where cells are connected in series, resembling a [CMOS](https://en.wikipedia.org/wiki/CMOS) NAND gate. Flash memory is used in computers, PDAs, digital audio players, digital cameras, mobile phones, synthesizers, video games, scientific instrumentation, industrial robotics, and medical electronics.

[3D Vertical NAND (V-NAND)](https://www.samsung.com/semiconductor/global.semi.static/2bit_V-NAND_technology_White_Paper-1.pdf) is a unique NAND flash memory design by Samsung where planar NAND (single planes of NAND cells) are stacked vertically and boasts a cell-to-cell interference-free structure using Charge Trap Flash (CTF) technology. This change in vertical arrangement of cells these SSDs have better capacities at lower production costs, half the power requirements, twice the speed and ten times the longevity of planar NAND.

[Charge trap flash (CTF)](https://en.wikipedia.org/wiki/Charge_trap_flash) is a semiconductor memory technology used in creating non-volatile NOR and NAND flash memory. It's a type of floating-gate MOSFET memory technology, but differs from the conventional floating-gate technology in that it uses a silicon nitride film to store electrons rather than the doped polycrystalline silicon typical of a floating-gate structure.

[NOR Flash](https://en.wikipedia.org/wiki/Flash_memory#NOR_flash) is a type flash memory where each cell has one end connected directly to ground, and the other end connected directly to a bit line.

[Universal Flash Storage (UFS)](https://www.jedec.org/standards-documents/focus/flash/universal-flash-storage-ufs) is an open standard, high-performance interface designed for use in applications where power consumption needs to be minimized, including mobile systems such as smartphones and tablets as well as automotive applications. Its high-speed serial interface and optimized protocol enable significant improvements in throughput and system performance.

[Flash Translation Layer (FTL)](https://mydatarecoverylab.com/flash-translation-layer/) is designed and tested to handle unexpected system resets cleanly. If a write is initiated during a system reset, and not completed, then the old state of the logical sector being addressed will be presented on start-up. If the write operation was complete, then the new state of the logical sector will be read. No in-between states or complex recovery procedures are required.

[Intel® Optane™ memory](https://www.intel.com/content/www/us/en/products/details/memory-storage/optane-memory.html) is a standalone memory device that is different from all the rest. It streamlines your computing experience by combining storage capacity and intelligent system acceleration.

[Memory module](https://en.wikipedia.org/wiki/Memory_module) is a printed circuit board on which memory integrated circuits are mounted. Memory modules permit easy installation and replacement in electronic systems such as personal computers, workstations, and servers.

[CMOS (Complementary Metal-Oxide Semiconductor)](https://www.computerhope.com/jargon/c/cmos.htm) is a small amount of memory on a computer motherboard that stores the BIOS settings. These BIOS settings include the system time and date, as well as hardware settings.

[Random Access Memory (RAM)](https://en.wikipedia.org/wiki/Random-access_memory) is a form of computer memory that can be read and changed in any order, typically used to store working data and machine code. A random access memory device allows data items to be read or written in almost the same amount of time irrespective of the physical location of data inside the memory, in contrast with other direct-access data storage media.

[Non-Volatile Random Access Memory (NVRAM)](https://www.techopedia.com/definition/2794/non-volatile-random-access-memory-nvram) is a category of Random Access Memory (RAM) that retains stored data even if the power is switched off. NVRAM uses a tiny 24-pin dual inline package (DIP) integrated circuit chip, which helps it to gain the power required to function from the CMOS battery on the motherboard.

[Embedded MultiMediaCard (eMMC)](https://www.enterprisestorageforum.com/hardware/emmc-storage/)  is an internal data storage card, built using flash storage.Its tiny size and low price make it a popular choice for data storage in portable devices like smartphones, tablets, cameras, and laptops.

[Error Correction Code (ECC) memory](https://www.crucial.com/products/memory/server/ecc) is a method of detecting and then correcting single-bit memory errors. A single-bit memory error is a data error in server output or production, and the presence of errors can have a big impact on server performance. The two types of single-bit memory errors: **hard errors and soft errors**. **Hard errors** are caused by physical factors, such as excessive temperature variation, voltage stress, or physical stress brought upon the memory bits. **Soft errors** occur when data is written or read differently than originally intended, such as variations in voltage on the motherboard, to cosmic rays or radioactive decay that can cause bits in the memory to flip.

There are two types of single-bit memory errors: hard errors and soft errors. Hard errors are caused by physical factors, such as excessive temperature variation, voltage stress, or physical stress brought upon the memory bits.

Soft errors occur when data is written or read differently than originally intended, such as variations in voltage on the motherboard, to cosmic rays or radioactive decay that can cause bits in the memory to flip.

[Virtual memory](https://en.wikipedia.org/wiki/Virtual_memory) is a memory management technique that is implemented by using both hardware (central processing unit (CPU)) and software. It makes a program think it has available storage space or address space. When actually virtual memory usually is divided into several physical memory fragments, and stored on the disk storage(SSD or HDD) which can be used to exchange data when needed. On Windows this is called a [Pagefile](https://docs.microsoft.com/en-us/windows/client-management/introduction-page-file) or on Linux a [Swap space](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-swapspace).

[Secure virtual memory](https://support.apple.com/guide/mac-help/what-is-secure-virtual-memory-on-mac-mh11852/mac) is a technique used in macOS that encrypts the data in virtual memory. Secure virtual memory is always on, so data is kept secure while it’s swapped between your hard disk and RAM. The RAM on your Mac contains no information when it’s off.

[Memory-Mapped Files](https://docs.microsoft.com/en-us/dotnet/standard/io/memory-mapped-files) is a technique that contains the contents of a file in virtual memory. This mapping between a file and memory space enables an application, including multiple processes, to modify the file by reading and writing directly to the memory. You can use managed code to access memory-mapped files in the same way that native Windows functions access memory-mapped files

[Bcache](https://en.wikipedia.org/wiki/Bcache) is a cache in the Linux kernel's block layer, which is used for accessing secondary storage devices. It allows one or more fast storage devices, such as flash-based solid-state drives (SSDs), to act as a cache for one or more slower storage devices, such as hard disk drives (HDDs). This effectively creating hybrid volumes and provides performance improvements.

## SSD Interfaces
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[Serial ATA (SATA)](https://en.wikipedia.org/wiki/SATA) is a computer bus interface that connects host bus adapters to mass storage devices such as hard disk drives, optical drives, and solid-state drives.

[M.2](https://en.wikipedia.org/wiki/M.2) is a specification for internally mounted computer expansion cards and associated connectors. M.2 replaces the [mSATA](https://en.wikipedia.org/wiki/MSATA) standard, which uses the PCI Express Mini Card physical card layout and connectors.

[NVM Express (NVMe)](https://en.wikipedia.org/wiki/NVM_Express) is an open, logical-device interface specification for accessing a computer's non-volatile storage media usually attached via PCI Express (PCIe) bus.

[PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express) is a high-speed serial computer expansion bus standard, designed to replace the older PCI, PCI-X and AGP bus standards.

## PCIe Protocols
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[Transaction Layer Packets (TLPs)](https://www.oreilly.com/library/view/pci-express-system/0321156307/0321156307_ch04lev1sec5.html) is the starting point in the assembly of outbound Transaction Layer Packets (TLPs), and the end point for disassembly of inbound TLPs at the receiver. Along the way, the Data Link Layer and Physical Layer of each device contribute to the packet assembly and disassembly.

[Physical layer](https://osi-model.com/physical-layer/) is the lowest layer in the seven-layer OSI model of computer networking. It provides mechanical, electrical and other functional aids available to enable or disable, they maintain and transmit bits about physical connections. This may for example be electrical signals, optical signals (optical fiber, laser), electromagnetic waves (wireless networks) or sound. The techniques used are called technical transmission process. Devices and network components that are associated with the physical layer, for example, the antenna and the amplifier, plug and socket for the network cable, the repeater, the stroke, the transceiver, the T-bar and the terminator.

[Network interface cards (NICs)](https://www.ni.com/en-us/support/documentation/supplemental/11/best-practices-for-using-multiple-network-interfaces--nics--with.html) is a network interface controller, network adapter, or Local Area Network ( LAN) adapter. It provides network connections for devices like computers and servers.

[Enumeration](https://resources.infosecinstitute.com/topic/what-is-enumeration/) is defined as a process which establishes an active connection to the target hosts to discover potential attack vectors in the system, and the same can be used for further exploitation of the system.

## Fabrics
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[NVMe over Fabrics (NVMeOF)](https://www.samsung.com/us/labs/pdfs/nvmf-disaggregation-preprint.pdf) is a recent protocol standard for accessing NVMe devices over RDMA-capable networks. By leveraging RDMA, NVMf offloads data movement to the network card (NIC), thus reducing the processing overheads involved in handling remote I/O requests on both the host and the target.

[Non-Transparent Bridging (NTB)](https://docs.nvidia.com/drive/drive_os_5.1.6.1L/nvvib_docs/index.html#page/DRIVE_OS_Linux_SDK_Development_Guide/System%20Programming/sys_components_non_transparent_bridging.html#) is a process that enables a inter-domain communication, facilitating communication between devices in different switch partitions. This ability enables both hosts and EPs to initiate transactions to hosts and/or EPs in another switch partition. An NTB or NT Interconnection consists of two or more PCI functions each defined by a Type 0 PCI header that are interconnected by a bridging function. The Type 0 PCI functions are referred to as Non-Transparent EPs (NT EP). Each partition can have at most one NT EP.

[Compute Express Link™ (CXL™)](https://www.computeexpresslink.org/about-cxl) is an industry-supported Cache-Coherent Interconnect for Processors, Memory Expansion and Accelerators. CXL technology maintains memory coherency between the CPU memory space and memory on attached devices, which allows resource sharing for higher performance, reduced software stack complexity, and lower overall system cost.

[Gen-Z](https://genzconsortium.org/about-us/gen-z-technology/) is an open-systems fabric-based architecture designed to interconnect processors, memory devices and accelerators. The fabric enables resource provisioning and sharing to support a diverse range of applications and provide flexibility for system reconfiguration as application demands for different resources change.

[Remote Direct Memory Access(RDMA)fabrics](https://core.vmware.com/resource/basics-remote-direct-memory-access-rdma-vsphere) is an extenion of the Direct Memory Acces (DMA) technology, which is the ability to access host memory directly without CPU intervention. RDMA allows for accessing memory data from one host to another. A key charateric for RDMA is that it greatly improves throughput and performance because less CPU cycles are needed to process the network packets.

# File systems & Storage
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[Flash file system](https://en.wikipedia.org/wiki/Flash_file_system) is a file system designed for storing files on flash memory–based storage devices.

[NAS (Network Attached Storage)](https://www.synology.com/en-us/solution/what_is_nas) is an intelligent storage device connected to your home or office network. You can store all your family and colleagues' files on the NAS, from important documents to precious photos, music and video collections.

[GlusterFS](https://www.gluster.org/) is a free and open source scalable network filesystem. Gluster is a scalable network filesystem. Using common off-the-shelf hardware, you can create large, distributed storage solutions for media streaming, data analysis, and other data- and bandwidth-intensive tasks.

[Ceph](https://ceph.io/) is a software-defined storage solution designed to address the object, block, and file storage needs of data centers adopting open source as the new norm for high-growth block storage, object stores and data lakes. Ceph provides enterprise scalable storage while keeping [CAPEX](https://corporatefinanceinstitute.com/resources/knowledge/modeling/how-to-calculate-capex-formula/) and [OPEX](https://www.investopedia.com/terms/o/operating_expense.asp) costs in line with underlying bulk commodity disk prices.

[Hadoop Distributed File System (HDFS)](https://www.ibm.com/analytics/hadoop/hdfs) is a distributed file system that handles large data sets running on commodity hardware. It is used to scale a single Apache Hadoop cluster to hundreds (and even thousands) of nodes. HDFS is one of the major components of Apache Hadoop, the others being [MapReduce](https://www.ibm.com/analytics/hadoop/mapreduce) and [YARN](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html).

[ZFS](https://docs.oracle.com/cd/E19253-01/819-5461/zfsover-2/) is an enterprise-ready open source file system and volume manager with unprecedented flexibility and an uncompromising commitment to data integrity.

[OpenZFS](https://openzfs.org/wiki/Main_Page ) is an open-source storage platform. It includes the functionality of both traditional file systems and volume manager. It has many advanced features including:

  - Protection against data corruption.
  - Integrity checking for both data and metadata.
  - Continuous integrity verification and automatic "self-healing" repair.

[Btrfs](https://btrfs.wiki.kernel.org/index.php/Main_Page) is a modern copy on write (CoW) filesystem for Linux aimed at implementing advanced features while also focusing on fault tolerance, repair and easy administration. Its main features and benefits are:

  - Snapshots which do not make the full copy of files
  - RAID - support for software-based RAID 0, RAID 1, RAID 10
  - Self-healing - checksums for data and metadata, automatic detection of silent data corruptions

[Apple File System (APFS)](https://support.apple.com/guide/disk-utility/file-system-formats-available-in-disk-utility-dsku19ed921c/mac) is  the default file system for Mac computers using macOS 10.13 or later, features strong encryption, space sharing, snapshots, fast directory sizing, and improved file system fundamentals.

[NTFS(New Technology File System)](https://docs.microsoft.com/en-us/windows-server/storage/file-server/ntfs-overview) is the primary file system for recent versions of Windows and Windows Server—provides a full set of features including security descriptors, encryption, disk quotas, and rich metadata, and can be used with Cluster Shared Volumes (CSV) to provide continuously available volumes that can be accessed simultaneously from multiple nodes of a failover cluster.

[exFAT(Extended File Allocation Table )](https://docs.microsoft.com/en-us/windows/win32/fileio/exfat-specification) is the file system that was the successor to FAT32 in the FAT family of file systems. It was optimized for flash memory such as USB flash drives and SD cards.

# Virtualization Tools
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[HVM (Hardware Virtual Machine)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/virtualization_types.html) is a virtualization type that provides the ability to run an operating system directly on top of a virtual machine without any modification, as if it were run on the bare-metal hardware.

[PV(ParaVirtualization)](https://wiki.xenproject.org/wiki/Paravirtualization_(PV)) is an efficient and lightweight virtualization technique introduced by the Xen Project team, later adopted by other virtualization solutions. PV does not require virtualization extensions from the host CPU and thus enables virtualization on hardware architectures that do not support Hardware-assisted virtualization.

[Network functions virtualization (NFV)](https://www.vmware.com/topics/glossary/content/network-functions-virtualization-nfv) is the replacement of network appliance hardware with virtual machines. The virtual machines use a hypervisor to run networking software and processes such as routing and load balancing. NFV allows for the separation of communication services from dedicated hardware, such as routers and firewalls. This separation means network operations can provide new services dynamically and without installing new hardware. Deploying network components with network functions virtualization only takes hours compared to months like with traditional networking solutions.

[Software Defined Networking (SDN)](https://www.vmware.com/topics/glossary/content/software-defined-networking) is an approach to networking that uses software-based controllers or application programming interfaces (APIs) to communicate with underlying hardware infrastructure and direct traffic on a network. This model differs from that of traditional networks, which use dedicated hardware devices (routers and switches) to control network traffic.

[Virtualized Infrastructure Manager (VIM)](https://www.cisco.com/c/en/us/td/docs/net_mgmt/network_function_virtualization_Infrastructure/3_2_2/install_guide/Cisco_VIM_Install_Guide_3_2_2/Cisco_VIM_Install_Guide_3_2_2_chapter_00.html) is a service delivery and reduce costs with high performance lifecycle management Manage the full lifecycle of the software and hardware comprising your NFV infrastructure (NFVI), and maintaining a live inventory and allocation plan of both physical and virtual resources.

[Management and Orchestration(MANO)](https://www.etsi.org/technologies/open-source-mano) is an ETSI-hosted initiative to develop an Open Source NFV Management and Orchestration (MANO) software stack aligned with ETSI NFV. Two of the key components of the ETSI NFV architectural framework are the NFV Orchestrator and VNF Manager, known as NFV MANO.

[Magma](https://www.magmacore.org/) is an open source software platform that gives network operators an open, flexible and extendable mobile core network solution. Their mission is to connect the world to a faster network by enabling service providers to build cost-effective and extensible carrier-grade networks. Magma is 3GPP generation (2G, 3G, 4G or upcoming 5G networks) and access network agnostic (cellular or WiFi). It can flexibly support a radio access network with minimal development and deployment effort.

[OpenRAN](https://open-ran.org/) is an intelligent Radio Access Network(RAN) integrated on general purpose platforms with open interface between software defined functions. Open RANecosystem enables enormous flexibility and interoperability with a complete openess to multi-vendor deployments.

[Open vSwitch(OVS)](https://www.openvswitch.org/)is an open source production quality, multilayer virtual switch licensed under the open source Apache 2.0 license. It is designed to enable massive network automation through programmatic extension, while still supporting standard management interfaces and protocols (NetFlow, sFlow, IPFIX, RSPAN, CLI, LACP, 802.1ag).

[Edge](https://www.ibm.com/cloud/what-is-edge-computing) is a distributed computing framework that brings enterprise applications closer to data sources such as IoT devices or local edge servers. This proximity to data at its source can deliver strong business benefits, including faster insights, improved response times and better bandwidth availability.

[Multi-access edge computing (MEC)](https://www.etsi.org/technologies/multi-access-edge-computing) is an Industry Specification Group (ISG) within ETSI to create a standardized, open environment which will allow the efficient and seamless integration of applications from vendors, service providers, and third-parties across multi-vendor Multi-access Edge Computing platforms.

[Virtualized network functions(VNFs)](https://www.juniper.net/documentation/en_US/cso4.1/topics/concept/nsd-vnf-overview.html) is a software application used in a Network Functions Virtualization (NFV) implementation that has well defined interfaces, and provides one or more component networking functions in a defined way. For example, a security VNF provides Network Address Translation (NAT) and firewall component functions.

[Cloud-Native Network Functions(CNF)](https://www.cncf.io/announcements/2020/11/18/cloud-native-network-functions-conformance-launched-by-cncf/) is a network function designed and implemented to run inside containers. CNFs inherit all the cloud native architectural and operational principles including Kubernetes(K8s) lifecycle management, agility, resilience, and observability.

[Physical Network Function(PNF)](https://www.mpirical.com/glossary/pnf-physical-network-function) is a physical network node which has not undergone virtualization. Both PNFs and VNFs (Virtualized Network Functions) can be used to form an overall Network Service.

[Network functions virtualization infrastructure(NFVI)](https://docs.vmware.com/en/VMware-vCloud-NFV/2.0/vmware-vcloud-nfv-reference-architecture-20/GUID-FBEA6C6B-54D8-4A37-87B1-D825F9E0DBC7.html) is the foundation of the overall NFV architecture. It provides the physical compute, storage, and networking hardware that hosts the VNFs. Each NFVI block can be thought of as an NFVI node and many nodes can be deployed and controlled geographically.

[Virtualization-based Security (VBS)](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-vbs) is a hardware virtualization feature to create and isolate a secure region of memory from the normal operating system.

[Hypervisor-Enforced Code Integrity (HVCI)](https://docs.microsoft.com/en-us/windows-hardware/drivers/bringup/device-guard-and-credential-guard) is a mechanism whereby a hypervisor, such as Hyper-V, uses hardware virtualization to protect kernel-mode processes against the injection and execution of malicious or unverified code. Code integrity validation is performed in a secure environment that is resistant to attack from malicious software, and page permissions for kernel mode are set and maintained by the hypervisor.

[KVM (for Kernel-based Virtual Machine)](https://www.linux-kvm.org/page/Main_Page) is a full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V). It consists of a loadable kernel module, kvm.ko, that provides the core virtualization infrastructure and a processor specific module, kvm-intel.ko or kvm-amd.ko.

[QEMU](https://www.qemu.org) is a fast processor emulator using a portable dynamic translator. QEMU emulates a full system, including a processor and various peripherals. It can be used to launch a different Operating System without rebooting the PC or to debug system code.

[Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/) enables running virtualized computer systems on top of a physical host. These virtualized systems can be used and managed just as if they were physical computer systems, however they exist in virtualized and isolated environment. Special software called a hypervisor manages access between the virtual systems and the physical hardware resources. Virtualization enables quick deployment of computer systems, a way to quickly restore systems to a previously known good state, and the ability to migrate systems between physical hosts.

[VirtManager](https://github.com/virt-manager/virt-manager) is a graphical tool for managing virtual machines via libvirt. Most usage is with QEMU/KVM virtual machines, but Xen and libvirt LXC containers are well supported. Common operations for any libvirt driver should work.

[oVirt](https://www.ovirt.org) is an open-source distributed virtualization solution, designed to manage your entire enterprise infrastructure. oVirt uses the trusted KVM hypervisor and is built upon several other community projects, including libvirt, Gluster, PatternFly, and Ansible.Founded by Red Hat as a community project on which Red Hat Enterprise Virtualization is based allowing for centralized management of virtual machines, compute, storage and networking resources, from an easy-to-use web-based front-end with platform independent access.

[HyperKit](https://github.com/moby/hyperkit) is a toolkit for embedding hypervisor capabilities in your application. It includes a complete hypervisor, based on [xhyve](https://github.com/mist64/xhyve)/[bhyve](https://bhyve.org/), which is optimized for lightweight virtual machines and container deployment. It is designed to be interfaced with higher-level components such as the [VPNKit](https://github.com/moby/vpnkit) and [DataKit](https://github.com/moby/datakit). HyperKit currently only supports macOS using the [Hypervisor.framework](https://developer.apple.com/library/mac/documentation/DriversKernelHardware/Reference/Hypervisor/index.html) making it a core component of Docker Desktop for Mac.

[Intel® Graphics Virtualization Technology (Intel® GVT)](https://github.com/intel/gvt-linux) is a full GPU virtualization solution with mediated pass-through, starting from 4th generation Intel Core (TM) processors with Intel processor graphics(Broadwell and newer). It can be used to virtualize the GPU for multiple guest virtual machines, effectively providing near-native graphics performance in the virtual machine and still letting your host use the virtualized GPU normally.

[Apple Hypervisor](https://developer.apple.com/documentation/hypervisor) is a frameowrk that builds virtualization solutions on top of a lightweight hypervisor, without third-party kernel extensions. Hypervisor provides C APIs so you can interact with virtualization technologies in user space, without writing kernel extensions (KEXTs). As a result, the apps you create using this framework are suitable for distribution on the [Mac App Store](https://www.appstore.com/).

[Apple Virtualization Framework](https://developer.apple.com/documentation/virtualization) is a framework that provides high-level APIs for creating and managing virtual machines on Apple silicon and Intel-based Mac computers. This framework is used to boot and run a Linux-based operating system in a custom environment that you define. It also supports the [Virtio specification](https://www.redhat.com/en/virtio-networking-series), which defines standard interfaces for many device types, including network, socket, serial port, storage, entropy, and memory-balloon devices.

[Apple Paravirtualized Graphics Framework](https://developer.apple.com/documentation/paravirtualizedgraphics) is a framework that implements hardware-accelerated graphics for macOS running in a virtual machine, hereafter known as the guest. The operating system provides a graphics driver that runs inside the guest, communicating with the framework in the host operating system to take advantage of Metal-accelerated graphics.

[Cloud Hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor) is an open source Virtual Machine Monitor (VMM) that runs on top of [KVM](https://www.kernel.org/doc/Documentation/virtual/kvm/api.txt). The project focuses on exclusively running modern, cloud workloads, on top of a limited set of hardware architectures and platforms. Cloud workloads refers to those that are usually run by customers inside a cloud provider. Cloud Hypervisor is implemented in [Rust](https://www.rust-lang.org/) and is based on the [rust-vmm](https://github.com/rust-vmm) crates.

[VMware vSphere Hypervisor](https://www.vmware.com/products/vsphere-hypervisor.html) is a bare-metal hypervisor that virtualizes servers; allowing you to consolidate your applications while saving time and money managing your IT infrastructure.

[Xen](https://github.com/xen-project/xen) is focused on advancing virtualization in a number of different commercial and open source applications, including server virtualization, Infrastructure as a Services (IaaS), desktop virtualization, security applications, embedded and hardware appliances, and automotive/aviation.

[Ganeti](https://github.com/ganeti/ganeti) is a virtual machine cluster management tool built on top of existing virtualization technologies such as Xen or KVM and other open source software. Once installed, the tool assumes management of the virtual instances (Xen DomU).

[Packer](https://www.packer.io/) is an open source tool for creating identical machine images for multiple platforms from a single source configuration. Packer is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

[Vagrant](https://www.vagrantup.com/) is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past. It provides easy to configure, reproducible, and portable work environments built on top of industry-standard technology and controlled by a single consistent workflow to help maximize the productivity and flexibility of you and your team.

[Parallels Desktop](https://www.parallels.com) is a Desktop Hypervisor that delivers the fastest, easiest and most powerful application for running Windows/Linux on Mac (including the new [Apple M1 chip](https://www.apple.com/newsroom/2020/11/apple-unleashes-m1/)) and ChromeOS.

[VMware Fusion](https://www.vmware.com/products/fusion.html) is a Desktop Hypervisor that deliver desktop and ‘server’ virtual machines, containers and [Kubernetes clusters](https://www.vmware.com/topics/glossary/content/kubernetes-cluster) to developers, and IT professionals on the Mac.

[VMware Workstation](https://www.vmware.com/products/workstation-pro.html) is a hosted hypervisor that runs on x64 versions of Windows and Linux operating systems; it enables users to set up virtual machines on a single physical machine, and use them simultaneously along with the actual machine.

# Emulation Tools
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

[Verdi® Protocol Analyzer](https://www.synopsys.com/verification/debug/verdi-protocol-analyzer.html) is a simulator independent, protocol and memory aware debug environment that enables users to quickly debug with any verification environment and easily share simulation results across teams. It gives users a graphical view of the transfers, transaction, packets and handshaking of a protocol. It highlights relationships across the hierarchy, visually unraveling the complex behavior of highly interleaved traffic. Also, enables engineers to quickly understand protocol activity, identify bottlenecks and debug unexpected behavior. Errors, warnings and messages are annotated to rapidly identify problems in the simulation.

[Synopsys’ Verdi® HW SW Debug](https://www.synopsys.com/verification/debug/verdi-hw-sw-debug.html) is a simulator tool that enables embedded software-driven SoC verification by providing a synchronized multi-window view of the design’s behavior of both hardware and software. It combines an instruction accurate embedded processor, RTL, C and assembly visibility for a comprehensive SoC debug solution.

[Synopsys Euclide](https://www.synopsys.com/verification/ide/euclide.html) is a Integrated Development Environment (IDE) that enables engineers to find bugs earlier and optimize code for design and verification flows by identifying complex design and testbench compliance checks during SystemVerilog and Universal Verification Methodology (UVM) development. Euclide accelerates correct-by-construction code development through context specific autocompletion and content assistance that is tuned for Synopsys VCS® simulation, Verdi® debug, and ZeBu® emulation, helping engineers to improve code quality during the entire project development cycle.

[Simvision](https://www.cadence.com/en_US/home/tools/system-design-and-verification/debug-analysis/simvision-debug.html) is unified graphical debugging environment within Cadence® Xcelium™ Parallel Logic Simulation, Cadence SimVision™ Debug supports signal-level and transaction-based flows across all IEEE-standard design, testbench, and assertion languages. It also supports concurrent visualization of hardware, software, and analog domains. It can be used to debug digital, analog, or mixed-signal designs written in Verilog, SystemVerilog, VHDL, and SystemC® languages or a combination thereof.

[Cadence® Palladium®](https://www.cadence.com/en_US/home/tools/system-design-and-verification/emulation-and-prototyping/palladium.html) is a set of emulation platforms that provides early software development, hardware/software verification and debug, and in circuit emulation.  It provides the highest debug productivity early in the design cycle when the RTL is still changing.

[Veloce Hardware-assisted Verification System](https://eda.sw.siemens.com/en-US/ic/veloce/) is a simulator tool that's used for the rapid verification of highly sophisticated, next-generation integrated circuit (IC) designs. It is the first complete, integrated offering that combines best-in-class virtual platform, hardware emulation, and Field Programmable Gate Array (FPGA) prototyping technologies and paves the way to leverage the latest powerful hardware-assisted verification methodologies.

[Synopsys ZeBu® EP1](https://www.synopsys.com/verification/emulation.html) is the industry’s fastest billion gates emulation system. It delivers 10 MHz emulation performance using Synopsys’ proven direct connect architecture to optimize design communication to accelerate the hardware and software verification for SoC designs of up to 2 billion gates. With ZeBu EP1 users can achieve unmatched performance while supporting all familiar emulation use cases, including early software bring-up, hybrid, hardware/software debug, simulation acceleration, performance validation and in-circuit emulation.

[SystemVerilog DPI (Direct Programming Interface)](https://verificationguide.com/systemverilog/systemverilog-dpi/) is an interface which can be used to interface SystemVerilog with foreign languages. These Foreign languages can be C, C++, SystemC as well as others. DPI allows the user to easily call functions of other language from SystemVerilog and to export SystemVerilog functions, so that they can be called in other languages.

[SystemVerilog Assertions](https://verificationguide.com/systemverilog/systemverilog-assertions/) is primarily used to validate the behavior of a design. An assertion is a check embedded in design or bound to a design unit during the simulation. Where warnings or errors are generated on the failure of a specific condition or sequence of events.

[SystemVerilog Functional Coverage](https://www.chipverify.com/systemverilog/systemverilog-functional-coverage) is a measure of what functionalities/features of the design have been exercised by the tests. This can be useful in constrained random verification (CRV) to know what features have been covered by a set of tests in a regression.

[Verilog-to-Routing (VTR) project](https://docs.verilogtorouting.org/en/latest/vtr/) is a world-wide collaborative effort to provide a open-source framework for conducting FPGA architecture and CAD research and development. The VTR design flow takes as input a Verilog description of a digital circuit, and a description of the target FPGA architecture.

[Verilog Power Estimation](https://docs.verilogtorouting.org/en/latest/vtr/power_estimation/) is performed within the VPR executable; however, additional files must be provided. In addition to the circuit and architecture files, power estimation requires files detailing the signal activities and technology properties.

[Cadence® SpeedBridge® Adapters](https://www.cadence.com/en_US/home/tools/system-design-and-verification/emulation-and-prototyping.html) is a tool that provides efficient driver and application-level testing. It's designed for pre-silicon RTL and integration of ASICs and systems on chip (SoCs), the solution can reproduce post-silicon bugs, as the design runs in the actual target system. The solution verifies emulated designs with the actual ASIC/SoC software/hardware, driver development, and application development, and runs with existing software and software test programs.

[Universal Verification Methodology (UVM)](https://verificationguide.com/uvm/) is a consists of class libraries needed for the development of well constructed, reusable SystemVerilog based Verification environment. In simple words, UVM consists of a set of base classes with methods defined in it, the SystemVerilog verification environment can be developed by extending these base classes. It will refer the UVM base classes as UVM Classes. [Accelerated UVM Testbenches](https://verificationacademy.com/courses/systemverilog-testbench-acceleration).

# Firmware Development
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/126912889-d86e3171-471a-4c05-b6bf-36a70080ab7c.png">
  <br />
</p>

## Firmware Learning Resources

[Firmware](https://en.wikipedia.org/wiki/Firmware) is a software program that comes embedded in a piece of hardware such as a keyboard, hard drive, BIOS, or a video card. It usually provides basic functions of a device and sometimes only provide services to higher-level software.

[Online Embedded Systems Courses | Harvard University](https://online-learning.harvard.edu/subject/embedded-systems-1)

[Internet of Things Graduate Program | Stanford Online](https://online.stanford.edu/programs/internet-things-graduate-program)

[Embedded Systems Certificate | UCSC Silicon Valley Extension](https://www.ucsc-extension.edu/certificates/embedded-systems/)

[Embedded Systems Technology (EET) | ODU Online](https://online.odu.edu/programs/embedded-systems-engineering-technology-eet)

[Learn Embedded Systems with Online Courses and Classes | edX](https://www.edx.org/learn/embedded-systems)

[Top Embedded Systems Courses Online | Udemy](https://www.udemy.com/topic/embedded-systems/)

[Top Embedded C Courses Online | Coursera](https://www.coursera.org/courses?query=embedded%20c)

[Embedded Systems | Udacity Free Courses](https://www.udacity.com/course/embedded-systems--ud169)

[Embedded Linux Online Course - Arm®](https://www.arm.com/resources/education/online-courses/embedded-linux)

[Software Development Online Courses | Coursera](https://www.coursera.org/browse/computer-science/software-development)

[Top Software Engineering Courses | Coursera](https://www.coursera.org/courses?query=software%20engineering&index=prod_all_products_term_optimization&completemode=undefined&page=1)

[Learn Software Development with Online Courses and Lessons | edX](https://www.edx.org/learn/software-development)

## Firmware Tools, Libraries, and Frameworks

[Coreboot](https://doc.coreboot.org/getting_started/index.html) is a replacement for your BIOS / UEFI with a strong focus on boot speed, security and flexibility. It is designed to boot your operating system as fast as possible without any compromise to security, with no back doors.

[TianoCore](https://www.tianocore.org/) is a community project supporting an open source implementation of the Unified Extensible Firmware Interface (UEFI). EDK II is a modern, feature-rich, cross-platform firmware development environment for the UEFI and UEFI Platform Initialization (PI) specifications.

[EDK II](https://github.com/tianocore/tianocore.github.io/wiki/EDK-II) is a modern, feature-rich, cross-platform firmware development environment for the UEFI and PI specifications .

[OpenWrt Project](https://openwrt.org/) is a Linux operating system targeting embedded devices. Instead of trying to create a single, static firmware, OpenWrt provides a fully writable filesystem with package management.

[OpenSK](https://github.com/google/OpenSK) is an open-source implementation for security keys written in Rust that supports both FIDO U2F and [FIDO2](https://fidoalliance.org/fido2/) standards.

[Linux Vendor Firmware Service(LVFS)](https://fwupd.org) is a secure portal which allows hardware vendors to upload firmware updates.

[fwupd](https://github.com/fwupd/fwupd) is a simple daemon to allow session software to update firmware. The goal og project is to make updating firmware on Linux automatic, safe and reliable.

[CHIPSEC](https://chipsec.github.io/) is a framework for analyzing the security of PC platforms including hardware, system firmware (BIOS/UEFI), and platform components. It includes a security test suite, tools for accessing various low level interfaces, and forensic capabilities. It can be run on Windows, Linux, Mac OS X and UEFI shell.

[Secure boot](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-secure-boot) is a security standard developed by members of the PC industry to help make sure that a device boots(Unified Extensible Firmware Interface (UEFI) BIOS) using only software(such as bootloaders, OS, UEFI drivers, and utilities) that is trusted by the Original Equipment Manufacturer (OEM).

[Trusted Platform Module (TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/trusted-platform-module-overview) is a technology module designed to provide hardware-based, security-related functions. A TPM chip is a secure crypto-processor that is designed to carry out cryptographic operations.

[Intel® oneAPI Base Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/base-toolkit.html) is a foundational kit that enables developers of all types to build, test, and deploy performance-driven, data-centric applications across CPUs, GPUs, and FPGAs. For more specialized workloads, use the Base Kit with one or more add-on toolkits.

[Intel® oneAPI HPC Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/hpc-toolkit.html) is toolkit that delivers fast DPC++, C++, Fortran, OpenMP, and MPI applications that scale.

[Intel® oneAPI IoT Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/iot-toolkit.html) is a toolkit for building high-performing, efficient, reliable solutions that run at the network’s edge.

[Intel® oneAPI Rendering Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/rendering-toolkit.html) is a toolit for accelerating High-Fidelity Rendering and Visualization Applications with Powerful Libraries.

[Intel® AI Analytics Toolkit](https://software.intel.com/content/www/us/en/develop/tools/oneapi/ai-analytics-toolkit.html) is a toolkit that helps you achieve end-to-end performance for AI workloads.

[Intel® Distribution of OpenVINO™ Toolkit](https://software.intel.com/content/www/us/en/develop/tools/openvino-toolkit.html) is a toolkit that you help you harness the full potential of AI across multiple Intel® architectures.

[System76 Firmware](https://github.com/pop-os/system76-firmware) is a software package that has a CLI(command-line inferface) tool for installing firmware updates. Also, included is the system76-firmware-daemon package, which has a systemd service that exposes a DBUS API for handling firmware updates.

[Firmware Manager](https://github.com/pop-os/firmware-manager) is a generic framework and GTK UI for firmware updates from [system76-firmware](https://github.com/pop-os/system76-firmware) and [fwupd](https://github.com/fwupd/fwupd), written in Rust.

[Heimdall](https://github.com/Benjamin-Dobell/Heimdall) is a cross-platform open-source tool suite used to flash firmware (aka ROMs) onto Samsung mobile devices.

[Nexmon](https://github.com/seemoo-lab/nexmon) is a C-based firmware patching framework for Broadcom/Cypress WiFi chips that enables you to write your own firmware patches, for example, to enable monitor mode with radiotap headers and frame injection.

[Firmware Analysis Toolkit](https://github.com/attify/firmware-analysis-toolkit) is a toolkit built in order to help security researchers analyze and identify vulnerabilities in IoT and embedded device firmware. This is built in order to use for the ["Offensive IoT Exploitation"](https://www.attify-store.com/collections/training/products/offensive-iot-exploitation) training conducted by [Attify](https://attify.com/).

[Firmware Analysis and Comparison Tool](https://github.com/fkie-cad/FACT_core) is a tool intended to automate most of the firmware analysis process. It unpacks arbitrary firmware files and processes several analyses. Additionally, it can compare several images or single files.

[Mellanox firmware update and query utility](https://www.mellanox.com/support/firmware/mlxup-mft) is a utility that enables scanning the server machine for available Mellanox adapters and indicates whether firmware update is required for each adapter.

[Mellanox FlexBoot](https://www.mellanox.com/products/adapter-software/flexboot) is a multiprotocol remote boot technology that delivers unprecedented flexibility in how IT Managers can provision or repurpose their datacenter servers. FlexBoot enables remote boot over InfiniBand or Ethernet using Boot over InfiniBand, over Ethernet, or Boot over iSCSI (Bo-iSCSI). Combined with Virtual Protocol Interconnect (VPI) technologies available in ConnectX®-3 and onwards adapters, FlexBoot gives IT Managers the flexibility to deploy servers with one adapter card into InfiniBand or Ethernet networks with the ability to boot from LAN or remote storage targets.

[QMK Toolbox](https://github.com/qmk/qmk_toolbox) is a Toolbox companion for [QMK](https://qmk.fm/) Firmware. It provides a collection of flashing tools packaged into one app. It supports auto-detection and auto-flashing of firmware to keyboards.

[QMK(Quantum Mechanical Keyboard) Firmware](https://github.com/qmk/qmk_firmware) is an open-source keyboard firmware for Atmel AVR and [Arm](https://www.arm.com/) USB controllers, and more specifically, the [OLKB product line](https://olkb.com/), the [ErgoDox EZ keyboard](https://ergodox-ez.com/), and the [Clueboard product line](https://clueboard.co/).

[TMK Keyboard Firmware](https://github.com/tmk/tmk_keyboard) is keyboard firmwares for Atmel AVR and [Arm](https://www.arm.com/) Cortex-M.

# Verilog/SystemVerilog Development
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/102273517-4b785480-3ed7-11eb-910a-113821428f17.png">
  <br />

</p>

## Verilog/SystemVerilog Learning Resources

[Verilog](https://verilog.com/) is a Hardware Description Language(HDL) used to design and document electronic systems. Verilog HDL allows designers to design at various levels of abstraction.

[SystemVerilog](https://www.systemverilog.io/) is an extension of Verilog with many of the verification features that allow engineers to verifythe design using complex testbench structures and random stimuli in simulation.

[Verilog Book Shelf](https://verilog.com/v-books.html)

[Verilog HDL Basics training from Intel](https://www.intel.com/content/www/us/en/programmable/support/training/course/ohdl1120.html)

[SystemVerilog for Design and Verification](https://www.cadence.com/en_US/home/training/all-courses/82143.html)

[Verilog HDL Programming Courses on Udemy](https://www.udemy.com/topic/verilog-hdl-programming/)

[Top Verilog Programming Courses on Coursera](https://www.coursera.org/courses?query=verilog)

[Verilog course for Engineers on Technobyte](https://technobyte.org/verilog-course-tutorials/)

[Verilog Tutorials and Courses on hackr.io](https://hackr.io/tutorials/learn-verilog)

[Designing With Verilog Certification from the Xilinx Learning Center](https://xilinxprod-catalog.netexam.com/Certification/35916/designing-with-verilog)

[Learning Verilog for FPGA Development on LinkedIn Learning](https://www.linkedin.com/learning/learning-verilog-for-fpga-development)

[SystemVerilog tutorial on ChipVerify](https://www.chipverify.com/systemverilog/systemverilog-tutorial)

## Verilog/SystemVerilog Tools

[Apio](https://github.com/FPGAwars/apio) is a multiplatform toolbox, with static pre-built packages, project configuration tools and easy command interface to verify, synthesize, simulate and upload your verilog designs.

[IceStorm](https://github.com/YosysHQ/icestorm) is a project that aims at documenting the bitstream format of Lattice iCE40 FPGAs and providing simple tools for analyzing and creating bitstream files.

[Icestudio](https://icestudio.io/) is a visual editor for open FPGA boards. Built on top of the Icestorm project using Apio.

[EDA Playground](https://www.edaplayground.com) is a online code for programming your Verilog projects.

[PlatformIO](https://platformio.org/) is a professional collaborative platform for embedded development with no vendor lock-in. It provides support for multiplatforms and frameworks such as IoT, Arduino, CMSIS, ESP-IDF, FreeRTOS, libOpenCM3, mbed OS, Pulp OS, SPL, STM32Cube, Zephyr RTOS, ARM, AVR, Espressif (ESP8266/ESP32), FPGA, MCS-51 (8051), MSP430, Nordic (nRF51/nRF52), NXP i.MX RT, PIC32, RISC-V.

[PlatformIO for VSCode](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide) is a plugin that provides support for the PlatformIO IDE on VSCode.

[Chisel](https://www.chisel-lang.org/) is a hardware design language that facilitates advanced circuit generation and design reuse for both ASIC and FPGA digital logic designs. Chisel adds hardware construction primitives to the [Scala](https://www.scala-lang.org/) programming language, providing designers with the power of a modern programming language to write complex, parameterizable circuit generators that produce synthesizable Verilog.

[Clash compiler](https://www.clash-lang.org/) is a functional hardware description language that borrows both its syntax and semantics from the functional programming language Haskell. The Clash compiler transforms these high-level descriptions to low-level synthesizable VHDL, Verilog, or SystemVerilog.

[Verilator](https://verilator.org/) is an open-source SystemVerilog simulator and lint system.

[Verilog to Routing(VTR)](https://verilogtorouting.org/) is a collaborative project to provide a open-source framework for conducting FPGA architecture and CAD Research & Development. The VTR design flow takes as input a Verilog description of a digital circuit, and a description of the target FPGA architecture.

[Cascade](https://github.com/vmware/cascade) is a Just-In-Time Compiler for Verilog from VMware Research. Cascade executes code immediately in a software simulator, and performs compilation in the background. When compilation is finished, the code is moved into hardware, and from the user’s perspective it simply gets faster over time.

[OpenTimer](https://github.com/OpenTimer/OpenTimer) is a High-Performance Timing Analysis Tool for VLSI Systems.

# Assembly Development
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/101415607-18154480-389d-11eb-80e8-17a5c57e480f.png">
  <br />
</p>

## Assembly Learning Resources

[Assembly](https://en.wikipedia.org/wiki/Assembly_language) is a low-level programming language. It uses mnemonic codes and labels to represent machine-level code with each instruction corresponding to just one machine operation.

[RISC-V Foundation](https://riscv.org/) is a non-profit corporation controlled by its 500 members(NVIDIA, Google, Samsung, Raspberry Pi, SiFive, Canonical, and Western Digital) to drive forward the adoption and implementation of the free and open RISC-V instruction set architecture (ISA).

[Intel® 64 and IA-32 Architectures Software Developer’s Manual](https://software.intel.com/content/www/us/en/develop/articles/intel-sdm.html)

[Introduction to x64 Assembly from Intel](https://software.intel.com/content/www/us/en/develop/articles/introduction-to-x64-assembly.html)

[x86 Assembly Language Reference Manual for Open Solaris](https://docs.oracle.com/cd/E19120-01/open.solaris/817-5477/index.html)

[AMD64 Architecture Programmer’s Manual Volume 1-5](https://www.amd.com/system/files/TechDocs/40332.pdf)

[AMD GPU ISA documentation](https://gpuopen.com/documentation/amd-isa-documentation/)

[AMD Developer Guides, Manuals, and ISA Documents](https://developer.amd.com/resources/developer-guides-manuals/)

[Assembler language from IBM](https://www.ibm.com/support/knowledgecenter/en/SSLTBW_2.1.0/com.ibm.zos.v2r1.asma400/asmr102112.htm)

[The Assembler language on z/OS from IBM](https://www.ibm.com/support/knowledgecenter/zosbasics/com.ibm.zos.zappldev/zappldev_25.htm)

[MIPS Architecture & Technology from Wave Computing](https://wavecomp.ai/mips-technology/)

[Assemblies in .NET](https://docs.microsoft.com/en-us/dotnet/standard/assembly/)

[Microsoft Macro Assembler reference](https://docs.microsoft.com/en-us/cpp/assembler/masm/microsoft-macro-assembler-reference)

[Compiler Intrinsics and Assembly Language from Microsoft](https://docs.microsoft.com/en-us/cpp/intrinsics/compiler-intrinsics-and-assembly-language)

[x86 and amd64 instruction Reference](https://www.felixcloutier.com/x86/)

[Intro to x86 Assembly Language Programming](https://cs.lmu.edu/~ray/notes/x86assembly/)

[Learn Assembly Programming courses on Udemy](https://www.udemy.com/topic/assembly-language/)

[Assembly Languages and Assemblers courses on Coursera](https://www.coursera.org/lecture/build-a-computer/unit-6-1-assembly-languages-and-assemblers-l4EGm)

[Intro to Assembly Language from MIT](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-004-computation-structures-spring-2017/index.htm)

# C/C++ Development
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/115297894-961e0d80-a111-11eb-81c3-e2bd2ac9a7cd.png">
  <br />
</p>

## C/C++ Learning Resources

[C++](https://www.cplusplus.com/doc/tutorial/) is a cross-platform language that can be used to build high-performance applications developed by Bjarne Stroustrup, as an extension to the C language.

[C](https://www.iso.org/standard/74528.html) is a general-purpose, high-level language that was originally developed by Dennis M. Ritchie to develop the UNIX operating system at Bell Labs. It supports structured programming, lexical variable scope, and recursion, with a static type system. C also provides constructs that map efficiently to typical machine instructions, which makes it one was of the most widely used programming languages today.

[Embedded C](https://en.wikipedia.org/wiki/Embedded_C) is a set of language extensions for the C programming language by the [C Standards Committee](https://isocpp.org/std/the-committee) to address issues that exist between C extensions for different [embedded systems](https://en.wikipedia.org/wiki/Embedded_system). The extensions hep enhance microprocessor features such as fixed-point arithmetic, multiple distinct memory banks, and basic I/O operations. This makes Embedded C the most popular embedded software language in the world.

[C & C++ Developer Tools from JetBrains](https://www.jetbrains.com/cpp/)

[Open source C++ libraries on cppreference.com](https://en.cppreference.com/w/cpp/links/libs)

[C++ Graphics libraries](https://cpp.libhunt.com/libs/graphics)

[C++ Libraries in MATLAB](https://www.mathworks.com/help/matlab/call-cpp-library-functions.html)

[C++ Tools and Libraries Articles](https://www.cplusplus.com/articles/tools/)

[Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)

[Introduction C++ Education course on Google Developers](https://developers.google.com/edu/c++/)

[C++ style guide for Fuchsia](https://fuchsia.dev/fuchsia-src/development/languages/c-cpp/cpp-style)

[C and C++ Coding Style Guide by OpenTitan](https://docs.opentitan.org/doc/rm/c_cpp_coding_style/)

[Chromium C++ Style Guide](https://chromium.googlesource.com/chromium/src/+/master/styleguide/c++/c++.md)

[C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md)

[C++ Style Guide for ROS](http://wiki.ros.org/CppStyleGuide)

[Learn C++](https://www.learncpp.com/)

[Learn C : An Interactive C Tutorial](https://www.learn-c.org/)

[C++ Institute](https://cppinstitute.org/free-c-and-c-courses)

[C++ Online Training Courses on LinkedIn Learning](https://www.linkedin.com/learning/topics/c-plus-plus)

[C++ Tutorials on W3Schools](https://www.w3schools.com/cpp/default.asp)

[Learn C Programming Online Courses on edX](https://www.edx.org/learn/c-programming)

[Learn C++ with Online Courses on edX](https://www.edx.org/learn/c-plus-plus)

[Learn C++ on Codecademy](https://www.codecademy.com/learn/learn-c-plus-plus)

[Coding for Everyone: C and C++ course on Coursera](https://www.coursera.org/specializations/coding-for-everyone)

[C++ For C Programmers on Coursera](https://www.coursera.org/learn/c-plus-plus-a)

[Top C Courses on Coursera](https://www.coursera.org/courses?query=c%20programming)

[C++ Online Courses on Udemy](https://www.udemy.com/topic/c-plus-plus/)

[Top C Courses on Udemy](https://www.udemy.com/topic/c-programming/)

[Basics of Embedded C Programming for Beginners on Udemy](https://www.udemy.com/course/embedded-c-programming-for-embedded-systems/)

[C++ For Programmers Course on Udacity](https://www.udacity.com/course/c-for-programmers--ud210)

[C++ Fundamentals Course on Pluralsight](https://www.pluralsight.com/courses/learn-program-cplusplus)

[Introduction to C++ on MIT Free Online Course Materials](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-096-introduction-to-c-january-iap-2011/)

[Introduction to C++ for Programmers | Harvard ](https://online-learning.harvard.edu/course/introduction-c-programmers)

[Online C Courses | Harvard University](https://online-learning.harvard.edu/subject/c)

## C/C++ Tools, Libraries and Frameworks

[AWS SDK for C++](https://aws.amazon.com/sdk-for-cpp/)

[Azure SDK for C++](https://github.com/Azure/azure-sdk-for-cpp)

[Azure SDK for C](https://github.com/Azure/azure-sdk-for-c)

[C++ Client Libraries for Google Cloud Services](https://github.com/googleapis/google-cloud-cpp)

[Visual Studio](https://visualstudio.microsoft.com/) is an integrated development environment (IDE) from Microsoft; which is a feature-rich application that can be used for many aspects of software development. Visual Studio makes it easy to edit, debug, build, and publish your app. By using Microsoft software development platforms such as Windows API, Windows Forms, Windows Presentation Foundation, and Windows Store.

[Visual Studio Code](https://code.visualstudio.com/) is a code editor redefined and optimized for building and debugging modern web and cloud applications.

[Vcpkg](https://github.com/microsoft/vcpkg) is a C++ Library Manager for Windows, Linux, and MacOS.

[ReSharper C++](https://www.jetbrains.com/resharper-cpp/features/) is a Visual Studio Extension for C++ developers developed by JetBrains.

[AppCode](https://www.jetbrains.com/objc/) is constantly monitoring the quality of your code. It warns you of errors and smells and suggests quick-fixes to resolve them automatically. AppCode provides lots of code inspections for Objective-C, Swift, C/C++, and a number of code inspections for other supported languages. All code inspections are run on the fly.

[CLion](https://www.jetbrains.com/clion/features/) is a cross-platform IDE for C and C++ developers developed by JetBrains.

[Code::Blocks](https://www.codeblocks.org/) is a free C/C++ and Fortran IDE built to meet the most demanding needs of its users. It is designed to be very extensible and fully configurable. Built around a plugin framework, Code::Blocks can be extended with plugins.

[CppSharp](https://github.com/mono/CppSharp) is a tool and set of libraries which facilitates the usage of native C/C++ code with the .NET ecosystem. It consumes C/C++ header and library files and generates the necessary glue code to surface the native API as a managed API. Such an API can be used to consume an existing native library in your managed code or add managed scripting support to a native codebase.

[Conan](https://conan.io/) is an Open Source Package Manager for C++ development and dependency management into the 21st century and on par with the other development ecosystems.

[High Performance Computing (HPC) SDK](https://developer.nvidia.com/hpc) is a comprehensive toolbox for GPU accelerating HPC modeling and simulation applications. It includes the C, C++, and Fortran compilers, libraries, and analysis tools necessary for developing HPC applications on the NVIDIA platform.

[Thrust](https://github.com/NVIDIA/thrust) is a C++ parallel programming library which resembles the C++ Standard Library. Thrust's high-level interface greatly enhances programmer productivity while enabling performance portability between GPUs and multicore CPUs. Interoperability with established technologies such as CUDA, TBB, and OpenMP integrates with existing software.

[Boost](https://www.boost.org/) is an educational opportunity focused on cutting-edge C++. Boost has been a participant in the annual Google Summer of Code since 2007, in which students develop their skills by working on Boost Library development.

[Automake](https://www.gnu.org/software/automake/) is a tool for automatically generating Makefile.in files compliant with the GNU Coding Standards. Automake requires the use of GNU Autoconf.

[Cmake](https://cmake.org/) is an open-source, cross-platform family of tools designed to build, test and package software. CMake is used to control the software compilation process using simple platform and compiler independent configuration files, and generate native makefiles and workspaces that can be used in the compiler environment of your choice.

[GDB](http://www.gnu.org/software/gdb/) is a debugger, that allows you to see what is going on `inside' another program while it executes or what another program was doing at the moment it crashed.

[GCC](https://gcc.gnu.org/) is a compiler Collection that includes front ends for C, C++, Objective-C, Fortran, Ada, Go, and D, as well as libraries for these languages.

[GSL](https://www.gnu.org/software/gsl/) is a numerical library for C and C++ programmers. It is free software under the GNU General Public License. The library provides a wide range of mathematical routines such as random number generators, special functions and least-squares fitting. There are over 1000 functions in total with an extensive test suite.

[OpenGL Extension Wrangler Library (GLEW)](https://www.opengl.org/sdk/libs/GLEW/) is a cross-platform open-source C/C++ extension loading library. GLEW provides efficient run-time mechanisms for determining which OpenGL extensions are supported on the target platform.

[Libtool](https://www.gnu.org/software/libtool/) is a generic library support script that hides the complexity of using shared libraries behind a consistent, portable interface. To use Libtool, add the new generic library building commands to your Makefile, Makefile.in, or Makefile.am.

[Maven](https://maven.apache.org/) is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.

[TAU (Tuning And Analysis Utilities)](http://www.cs.uoregon.edu/research/tau/home.php) is capable of gathering performance information through instrumentation of functions, methods, basic blocks, and statements as well as event-based sampling. All C++ language features are supported including templates and namespaces.

[Clang](https://clang.llvm.org/) is a production quality C, Objective-C, C++ and Objective-C++ compiler when targeting X86-32, X86-64, and ARM (other targets may have caveats, but are usually easy to fix). Clang is used in production to build performance-critical software like Google Chrome or Firefox.

[OpenCV](https://opencv.org/) is a highly optimized library with focus on real-time applications. Cross-Platform C++, Python and Java interfaces support Linux, MacOS, Windows, iOS, and Android.

[Libcu++](https://nvidia.github.io/libcudacxx) is the NVIDIA C++ Standard Library for your entire system. It provides a heterogeneous implementation of the C++ Standard Library that can be used in and between CPU and GPU code.

[ANTLR (ANother Tool for Language Recognition)](https://www.antlr.org/) is a powerful parser generator for reading, processing, executing, or translating structured text or binary files. It's widely used to build languages, tools, and frameworks. From a grammar, ANTLR generates a parser that can build parse trees and also generates a listener interface that makes it easy to respond to the recognition of phrases of interest.

[Oat++](https://oatpp.io/) is a light and powerful C++ web framework for highly scalable and resource-efficient web application. It's zero-dependency and easy-portable.

[JavaCPP](https://github.com/bytedeco/javacpp) is a program that provides efficient access to native C++ inside Java, not unlike the way some C/C++ compilers interact with assembly language.

[Cython](https://cython.org/) is a language that makes writing C extensions for Python as easy as Python itself. Cython is based on Pyrex, but supports more cutting edge functionality and optimizations such as calling C functions and declaring C types on variables and class attributes.

[Spdlog](https://github.com/gabime/spdlog) is a very fast, header-only/compiled, C++ logging library.

[Infer](https://fbinfer.com/) is a static analysis tool for Java, C++, Objective-C, and C. Infer is written in [OCaml](https://ocaml.org/).

# Electric charge, field, and potential
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

     - Charge and electric force (Coulomb's law): Electric charge, field, and potential
     - Electric field: Electric charge, field, and potential
     - Electric potential energy, electric potential, and voltage: Electric charge, field, and potential

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784122-2c0e9166-ff73-44cf-a5b5-62d76aba80c7.png">
  <br />
</p>

 **Electric Potential Energy. Source: [sparkfun](https://learn.sparkfun.com/tutorials/what-is-electricity/electric-potential-energy)**

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784121-8f89a787-1674-4db4-ba46-b2f280706dd9.png">
  <br />
</p>

# Circuits
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

    - Ohm's law and circuits with resistors: Circuits
    - Circuits with capacitors: Circuits

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784127-ad587152-0c0d-4671-b29d-9231889899ff.png">
  <br />
</p>

 **Electric Circuits. Source: [sdsu-physics](http://sdsu-physics.org/physics180/physics180B/Chapters/electric_currents.htm)**

  <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784128-941e1cf9-0cff-4702-b97b-f827d9489a20.png">
  <br />
</p>

 **Symbols of Circuits .Source: [andrewpover.co.uk](https://andrewpover.co.uk/category/physics/)**

# Magnetic forces, magnetic fields, and Faraday's law
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

    - Magnets and Magnetic Force: Magnetic forces, magnetic fields, and Faraday's law
    - Magnetic field created by a current: Magnetic forces, magnetic fields, and Faraday's law
    - Electric motors: Magnetic forces, magnetic fields, and Faraday's law
    - Magnetic flux and Faraday's law

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784132-d4b67030-9e04-41f1-90d2-98b7c6beebe8.png">
  <br />
</p>

 **Magnetic Field. Source: [vecteezy](https://www.vecteezy.com/vector-art/593998-physics-science-about-the-movement-of-magnetic-fields-positive-and-negative)**

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784663-28e8ad0e-aa9d-4dbf-b285-0b2976de2d3e.png">
  <br />
</p>

 **Amphere's Law. Source: [sdsu-physics](https://sdsu-physics.org/physics180/physics196/Topics/magneticFields30.html)**

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127784666-dd53913b-33c9-4ddd-8cf1-b8fa398bf3de.png">
  <br />
</p>

 **Farady's law. Source: [sdsu-physics](http://sdsu-physics.org/physics180/physics196/Topics/faradaysLaw.html)**

# Electromagnetic waves and interference
[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

    - Introduction to electromagnetic waves: Electromagnetic waves and interference
    - Interference of electromagnetic waves

  <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127785050-a98f0812-d723-49b9-9796-ac05bb64804a.png">
  <br />
</p>

 **Electromagnetic Wave. Source: [differencebetween](https://www.differencebetween.com/difference-between-wave-and-particle-nature-of-light/)**

 <p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/127785051-1a86c310-0e09-4f8b-be8e-99770dd0301e.png">
  <br />
</p>

   **EMI Spectrum. Source: [electrical4u](https://www.electrical4u.com/electromagnetic-interference/)**

## Contribute

- [x] If would you like to contribute to this guide simply make a [Pull Request](https://github.com/mikeroyal/SSD-Guide/pulls).


## License

[Back to the Top](https://github.com/mikeroyal/SSD-Guide#table-of-contents)

Distributed under the [Creative Commons Attribution 4.0 International (CC BY 4.0) Public License](https://creativecommons.org/licenses/by/4.0/).
