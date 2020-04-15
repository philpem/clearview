# ClearView

This is a 32-bit-clean (if built with the ROOL C compiler) version of Merlyn Kline's ClearView hypertext reader.

ClearView allows 

# Build instructions

At the time of writing there isn't a native Git client for RISC OS, so this is a little long-winded than it perhaps could be.

  * Check out the code.
    * If using a Raspberry Pi running native RISC OS -- check out onto an SMB or NFS share on a Linux PC. Mount the share on the Raspberry Pi using OmniClient or Sunfish.
    * If using RPCEmu -- check out into your HostFS directory.
  * Start up the C Compiler
    * Run !SetPaths
  * Make the RunImage
    * Shift-click to open !ClearGen.!ClearView
    * Increase the Next slot to about 4MB in Task Manager
    * Double-click the Makefile and let Make build the executable
  * Create a "Production" distribution disk
    * Put a floppy disk in ADFS::0
    * Run !Produce

The Production disk can then be used to make a ClearView floppy (using !ClearGen).
