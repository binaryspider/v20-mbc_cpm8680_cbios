# v20-mbc_cpm8680_cbios

CP/M-86/80 CBIOS

This CBIOS allows the V20-MBC fitted with the V20 CPU to seamlessly execute either 8086 or 8080 programs.

The CBIOS patches the CCP at initialisation to execute programs as follows:

 1. If program specified is a .CMD file, load and execute it as normal
 2. If the SAVE command was entered and an 8080 bank is still allocated, create the specified save file
 3. If program specified is a .COM file, allocate an 8080 memory bank, load program, prime CPM-80 environment and execute program
