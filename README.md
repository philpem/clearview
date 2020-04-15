# ClearView

This is a 32-bit-clean (if built with the ROOL C compiler) version of Merlyn Kline's ClearView hypertext reader.

ClearView is a hypertext reader/compiler which can display wrapped text in a variety of user-selectable fonts. It can also display Sprites, Drawfiles and Ace Films in-line with the text.

## Build instructions

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

## Credits

ClearView was developed by Merlyn Kline.

The EuclidX module was developed by Tony Cheal at Ace Computing. 32-bit conversion was by Martin Wurthner. It is licensed under the same terms as the original module, which was included with !Projector, !Genesis and other applications.
