EPSON Advanced Printer Driver Ver.4

                                     Copyright (c) 2017 SEIKO EPSON CORPORATION

1. About this software
This package includes the following two software programs to use with an EPSON 
TM/BA/EU series printer and DM-D customer display.

1) Windows Printer Driver
This driver is a Windows Printer Driver for the TM/BA/EU printer and DM-D customer display.
This driver makes it possible to print from a Windows application.

2) StatusAPI
StatusAPI is a program that works in conjunction with the TM/BA/EU printer driver.  
It offers an Application Program Interface for obtaining the printer status 
whether or not the printer is printing.  This API makes integrating printer
status handling functions with applications more simple.

For detailed information, please see each reference manual.

The driver operation has been verified with the following operating systems. 

    Windows 10 Pro English 32/64bit
    Windows 8.1 Pro English 32/64bit
    Windows 8 Pro English 32/64bit
    Windows 7 Ultimate SP1 English 32/64bit
    Windows Vista Ultimate SP2 English 32/64bit
    Windows XP Professional SP3 English 32bit
    Windows Server 2016 English 64bit
    Windows Server 2012 R2 English 64bit
    Windows Server 2012 English 64bit
    Windows Server 2008 R2 Enterprise SP1 English 64bit
    Windows Server 2008 Standard/Datacenter SP2 English 32bit
    Windows Server 2008 Standard SP2 English 64bit
    Windows Server 2003 R2 Enterprise SP2 English 32bit
    Windows Server 2003 R2 Standard SP2 English 64bit
    Windows XP Embedded 32bit SP2
    Windows Embedded Standerd 2009 32bit
    Windows Embedded POSReady 2009 32bit
    Windows Embedded for Point of Service 32bit
    Windows Embedded POSReady 7

This driver is not supported by Windows 95/98/NT/2000 and Windows XP 64bit.

EPSON IM series PC or IBM compatible PC

Supported Printers
  EPSON TM-T88V
  EPSON TM-T88IV
  EPSON TM-T88III
  EPSON TM-U220A/B/D
  EPSON TM-H2000
  EPSON TM-H6000III
  EPSON TM-H6000II
  EPSON TM-H6000IV
  EPSON TM-J7600/7500
  EPSON TM-T70
  EPSON TM-T90
  EPSON TM-L90
  EPSON TM-L90 Peeler
  EPSON TM-U295
  EPSON TM-H5000II
  EPSON TM-H5200
  EPSON TM-L60II
  EPSON TM-U230
  EPSON TM-U375
  EPSON TM-U675
  EPSON TM-U590
  EPSON TM-U950
  EPSON TM-J7100/7000
  EPSON TM-P60
  EPSON TM-P60 Peeler
  EPSON TM-U120
  EPSON TM-C100
  EPSON TM-T58
  EPSON TM-T70
  EPSON TM-T20
  EPSON TM-U325
  EPSON TM-T86FII
  EPSON TM-L500A Ticket
  EPSON TM-P60II
  EPSON TM-P60II Peeler

  EPSON DM-D110/120/210
  EPSON DM-D500

  EPSON BA-T500
  EPSON BA-T500II
  EPSON EU-T300
  EPSON EU-T400
  EPSON EU-T500

  EPSON TM-T88IV ReStick

The printer driver operates regardless of the printer firmware version.

2. Supplied Files
   APD_456dEWM.zip   : Printer Driver,StatusAPI installer with manuals

Refer to the installation manual APD4_Install_E_RevU.pdf.

3. Remarks
- For detailed information, please read each manual that is created by the 
  installation APDMANE_U.exe.

-When an error message is displayed during installation, the following procedure may enable to recover from the error.
  1) Specify the uninstall option, and execute the installer "APD_456dE.exe /uninstall".
  2) Remove the error factor.
  3) Execute the installer "APD_456dE.exe".

-Characters may not be printed correctly when using Easy Print of Windows Server 2008.
 For detailed information of this problem arising from the operating system,
 see the following web page provided by Microsoft Corporation.
  http://support.microsoft.com/kb/946411/

-In the Easy Print environment of Windows Server 2008, you cannot print the printer device font directly.
 However, you can print the device font converted from the True Type font by using "Font Substitution" of APD.
 For more information, see "Character Printing (Device Font)" in Printer Manual.

-To set properties of the printer driver redirected on the server using Terminal Service or Remote Desktop
 on the printer driver on a client, go to [Advanced] Tab, and press the [Printing Defaults] button.

-HELP is unavailable when using a printer driver redirected through the server using Terminal Service or Remote Desktop.

-When using Terminal Service and Remote Desktop, interactive communication becomes unavailable between the PC and the printer,
 prohibiting displaying the printer status and obtaining printer information using the Status API.

-The port redirection function is unavailable for a client when using Terminal Service or Remote Desktop.

-At times, the status of the shared printer may not be displayed correctly or the Status API may not be opened.
 These problems arise from the security policy settings of the operating system.
 Although changing the settings of the operating system is possible by the following steps, it lowers the security policy.
 (1) Go to [Start] - [Administrative tool] - [Local Security Policy].
 (2) [Security Option] - [Network Access (Set "Limit anonymous sccesses to the named pipe and shared printer" to "Invalid".)]
 However, you do not have to change the settings when a client PC is connected to the domain environment and
 when the same user name as a user name that is logged on a client is existing."

-In Printer Driver, some Languages in the Language Option, can not be displayed in the tool tips messages.
  For these languages, tool tips are displayed in English.

-In Printer Driver, some of the characters may turn into garbage characters when using the search function in Help.

-If you are using Electric Journal, the following file(s) in the Temp folder will be deleted each time the Electric Journal Viewer is launched.
  PRNXXX.tmp

-10,000 electric journal files can be saved in one folder.

-Please use the same version of EPSON Advanced Printer Driver for each host when a network printer is shared among two or more hosts.

-About how to use .Net module on Windows7/8.
  In case of Visual Basic .NET (Windows7/8).
    Example of Visual Basic .NET environment.
    1 Execute Microsoft Visual Basic and and run project window.
    2 Right click for [Reference settings] on Solution explorer and select [add reference].
    3 "Add reference" window is shown and click [Reference] tab.
    4 Select "C:\Programfiles\Epson\Advanced Printer Tool\StatusAPI" in  [File location] and open.
      -In case of 64bitOS, specify "C:\Program Files(x86)\Epson\Advanced Printer Tool\StatusAPI".
    5 Input "EpsonStatusAPI.dll" in [file] menu and click [OK] to select.
    6 Select [ Reference setting ] - [EpsonStatusAPI] in solution explorer.
      And set "False" on [specific version] property.
    7 Add following description in the source code using Imports statement.
      Imports com.epson.pos.driver
    8 Visual Basic .NET is now ready. You can develop application development using Status API.
  In case of Visual C# (Windows7/8).
    Following is example of Visual C# development.
    1 Execute Microsoft Visual C# and run project window.
    2 Right click for [Reference settings] on Solution explorer and select [add reference].
    3 "Add reference" window is shown and click [Reference] tab.
    4 Select "C:\Programfiles\Epson\Advanced Printer Tool\StatusAPI" in [File location] and open.
      -In case of 64bitOS, specify "C:\Program Files(x86)\Epson\Advanced Printer Tool\StatusAPI".
    5 Input "EpsonStatusAPI.dll" in [file] menu and click [OK] to select.
    6 Select [ Reference setting ] - [EpsonStatusAPI] in solution explorer.
      And set "False" on [specific version] property.
    7 Add following description in the source code using "using" keyward.
      using com.epson.pos.driver
    8 Visual Basic .NET is now ready. You can develop application development using Status API.

4.Modification from the old version
  Ver4.56d
     -The following problem has been solved:
         -When "Print all documents as image image" is enabled and printing a character string 
          including "\\" "\x" in barcode or two-dimensional symbol font, dose not printed correctly.

  Ver4.56c
     -Added support model
        TM-U950 USB model
     -The following problem has been solved:
         -There is a possibility of No print that use network printer from multi PC.

  Ver4.56
     -If using shared printer, take over the installation state of StatusViewer.
     -Improved print speed of TM-U220.
     -The following problem has been solved:
         -Printing white page when layout infomation set by layout settings tool.
         -By ethernet, there is a possibility of no print.
         -By ethernet, there is a possibility of stopping the print when used with Status API.
         -There is a possibility of stopping the print after BiCloseMonPrinter.
         -If BiOpenMonPrinter is faster than spooler open port, then does not print.
         -The TM-C100 driver does not get no ink status that windows immediately after start-up.
         -The TM-U950 driver continue printing without paper.
         -The speed of the BiOpenMonPrinter function of StatusAPI is slow.
         -A utility of TM-C100 may not work.
         -Printer status may come to remain "initializing".
         -AutoSize feature of StatusAPI does not work.

  Ver4.55d
     -The following problem has been solved:
         -There is a possibility of No print of TM-C100 on 64bit OS.
         -In share printer environment there is a possibility of delay print of TM-C100.
         -There is a possibility of that suddenly StatusViewer cannot get ink status of TM-C100.
         -When OS recovered from unexpected shutdown, there is a possibility of no printing.

  Ver4.55b
     -The following problem has been solved:
         -There is a possibility of No print of TM-C100 on 64bit OS.
         -The data are resent to a printer again in BiDirectIO/BiDirectIOEx of StatusAPI.

  Ver4.55a
     -The following problem has been solved:
         -There is the possibility of occurring not available printer issue. (Only APD4.55)

  Ver4.55
     -Add new functions for TM-L90 Label Driver.(Need connect to TM-L90 4**.)
         -Support "Full Page Label" on TM-L90 Label Driver.
         -Support GS1 barcode, MicroQR and DataMatrix.
         -Support gray scale print.
         -Support option buzzer.
         -No support the printing for 2 color receipt.
         -It can become to print the characters which are built-in printer by FontA/FontB
         -It can obtain "Number of line feeds" by StatusAPI ÅiBiGetCounterÅABiResetCounterÅj
     -Fix the problem of dividing the barcode when included the specific code(e.g."-") in input data.
     -Change the initial values of printer monitoring time and timeout at using Ethernet I/F.
         Status Polling Interval           3000(ms)
         Status Polling Timeout            2000(ms)
         Power Status Polling Interval     1000(ms)
         Power Status Polling Timeout      1000(ms)
         Power Status Polling Retry Count     3(times)
         Wireless Offline Count               1(time)
         Wireless Power Off Count             3(times)
         Wired Offline Count                  1(time)
         Wired Power Off Count                1(time)
     -The following problem has been solved:
         -There is a possibility of stopping the print by sending job to the printer from multiple PCs at the same time via Ethernet I/F.
         -There is a possiblity of to occur the garbage print by occurring lucking data in printing.
         -There is a possibility of to occur the while-loop(no end process) from BiCloseMonPrinter().
         -No print if contained "%" on document name.
         -It takes about 5 sec until online status after power-on the printer(TM-T20 and TM-T88V).
         -There is a possiblity of No end issue of Status Veiwer for TM-C100.
         -There is a possibility of No print by image mode on 64bit OS.

  Ver4.54a
     -Added support model
        TM-P60II Peeler

  Ver4.54
     -Added support model
        TM-P60II
     -Supports the following OS
          Microsoft Windows 8 32/64bit
          Microsoft Windows Server 2012 64bit
     -Revised the contents of EpsStmApi.h for StatusAPI.
     -Added support for .NET Framework 4.0.
     -The following problem has been solved:
         -During continued printing, the following kinds of prints are delayed.
         -Error recovery is not performed properly even when BiResetPrinterÅiÅj/BiForceResetPrinterÅiÅjis executed.

  Ver4.53
     -Add 80 x 60dpi resolution on TM-U295
     -Add 160 x 72dpi resolution on TM-U220
     -Supports to print FontA and FontB on BA-T500II
     -Supports to adjust cut posiotion for Black mark receipts on TM-L90 layput setting menu.
     -Silent install package is possible to install to any Windows OS version.
     -Can specify install folder for .Net module.
     -Add TMUSB Ver6.10a in the same package.

  Ver4.52c
     -The following problem has been solved:
        -It takes time until TM-T70/TM-T86FII becomes ready to print.

  Ver4.52b
     -The following problem has been solved:
        -A garbage characters are printed. (TM-T70,TM-T86FII(ESC/POS1.02))

  Ver4.52
     -Added support model
        TM-L500A Ticket
     -The following problem has been solved:
        -When the barcode of Code39 or Code93 print using DrawText function, the barcode is divided into two.

  Ver4.51
     -Added support model
        BA-T500II(Supports 58/60mm Roll Paper.)

  Ver4.50
     -Added support model
        TM-T86FII
     -Changed port setting window.
     -Newly added printer IP address setting to the port setting window.
     -Changed log setting window.
     -Supports the following OS
          Microsoft Windows Embedded POSReady 7

  Ver4.15b
      -The following problem has been solved:
         -The temporary files generated at the time of printing are left.

  Ver4.15
      -The TM-H6000IV now has the EPSON TM-H6000IV-40C EndorseE4 Å\ an additional driver that is compatible with 
       the TM-T6000III Endorse driver.
      -The installer has been changed so as to install only the necessary modules.
      -For dot impact series printers, the print resolution has been improved to print correctly when using Java or IE8.
         TM-H2000/TM-H6000II/TM-H6000III/TM-H6000IV/TM-H5000II/TM-H5200/TM-U675/TM-U950
      -The following problems have been solved:
         -The printer is unable to print if its power is turned off and then turned on in serial connection.
         -When printing continuously in the peeling issue mode with the TM-L90 peeler model, if the printer power is turned off and then turned back on 
          while the printer is waiting for label peeling, the printer is unable to print the next label.

  Ver4.13
      -Added support model
        TM-H2000
        TM-H6000IV
     -When "Print all text as graphic images" is enabled, you can set the printing speed lower for the pages that include barcode or 2D symbol.
        TM-T88V,TM-H2000,TM-H6000IV
     -The following functions have been added to the Status API function.
         BiForceResetPrinter
         BiGetExtendStatus
         BiStampImprint
         BiSCNClumpPaper
         BiSCNGetClumpStatus
         BiSCNClumpPaper
         BiSCNGetClumpStatus
     -The following problems have been solved:
        -APD installation will be failed if the specified ports are existed.
        -If printing in the image mode or multiple tone, 10mm more blanc will be found in the bottom.
        -Files are deleted and not be printed when executing the printing operation.
        -Printerkew status will be "User Intervention Required" and the printing cannot be performed.
        -The printing is performed while the printer is turned off. But the printing will not be performed even when turning on the printer.
        -The printer may not work even when reconnecting it after it is disconnected while the printing operation with Ether connection.
        -The check insertion time will be not abled even if setting it by the StatusAPI function.
        -The call back function will not be responded even when turning OFF/ON the printer after the BiMICRReadCheck is executed by the Status API function.
        -The memory area to be secured by MICR reading is NOT correct.
        -When connecting the printer with the parallel I/F by 64bitPS, a new hardware wizard dialog box will be appeared.

  Ver4.12
      -Added support model
        TM-U325
      -In APD installation, TM-T88V Utility and TM-T20 Utility will not be installed as the default.
      -The default value for the choices of the installing printer will be blanc.
      -In case of the installation of TM-U375, only Parallel and Serial port can be selectable.
      -When the electrical journal file could not be stored to the disc, it (jpeg) will be stored to the folder,
       which includes the default setting.

      -The following problem has been solved:
         -When installing the driver with BA-T500II turned ON, two ESDPRTxxx ports were created.
         -The value of [SCNDetail] and [MICRDetail], which were set in ".NET Wrapper" of "StatusAPI" was wrong.
         -A crash happened if repeating the "Debug" of the "Status API" by "VB6".
         -If repeating the print operation with the Ether connection, the print jobs were stored to the spooler and
          the print operation may stop.
         -If repeating the print operation with the Ether connection, Epson PH.exe might be force quitted.
         -In case of using the common printer or user authorized printer, the electrical journal file cannot be created.
         -In case of printing multiple copies, the set command of when printing started could not be stored to the electrical
          journal file of the 2nd copy or after.
         -Even if selecting the file to be indicated in the electrical journal viewer with the "PageUp" or "PageDown" keys,
          the preview was not updated.
         -Whenever the electrical journal file was selected in the electrical journal viewer, more memory was used.

  Ver4.11
      -TM-T20 support serial port.
      -Disregarded message display when creating electronic journal.(TM-T20,TM-T88V)
      -The following problem has been solved:
         -Lag in StatusAPIÇÃBiCloseMonPrinter.
         -Can not change monitor interval for Ether port.
         -Displays "Can not print" even if status detected by TM-C100 Status Veiwer is still "Ink low".
         -When printing multiple copies, electronic journal creates an uprintable file.(TM-T20,TM-T88V)

  Ver4.10
      -Printer Driver Supports 24 languages for Language Option and Help (except for TM-C100).
      -Printer Driver Logo Printing supports JPEG, GIF, and PNG  file formats.
      -Enabled the selection of "Fine" printing for TM-C100 on monochrome ink.
      -The following problem has been solved:
         -Sometimes unable to print when StatusAPI is being used.(Ver4.08)

  Ver4.09a
      -The compress/extract module was replaced to a one without encryption function.
      -The following problem has been solved:
         -If you enable sharing printer, it takes about 20 minutes when you start the pc.
          Or it takes about 10 minutes until you can use printer.

  Ver4.09
      -Queuing time until printing start after the instruction is reduced.
      -Alias is specifiable for Printer font.
      -New parallel port driver is used on 32-bit OS.
      -Wireless-Offline count setting is added to the Ethernet setting dialog.
      -The following problem has been solved:
         -Even though executing Silent install, User defined size that is set using the Layout tab in the Printing settings 
          cannot be copied.

  Ver4.08
      -Supports the following OS
         Microsoft Windows 7 32bit English
         Microsoft Windows 7 64bit English
         Microsoft Windows Server 2008 R2 64bit English
      -Added support model
        EPSON TM-T88IV ReStick
      -Added the function to specify the horizontal print position for logo printing of the printer driver.
         -Added support model
            EPSON TM-H5000II ReceiptE4
            EPSON TM-H5200 ReceiptE4
            EPSON TM-H6000II ReceiptE4
            EPSON TM-J7000/7100 ReceiptE4
            EPSON TM-J7500/7600 ReceiptE4
            EPSON TM-T88III ReceiptE4
            EPSON TM-L90Peeler ReceiptE4
            EPSON TM-P60 ReceiptE4
            EPSON TM-P60Peeler ReceiptE4
            EPSON TM-U675 ReceiptE4
            EPSON BA-T500 ReceiptE4
            EPSON EU-T300 ReceiptE4
            EPSON EU-T400 ReceiptE4
            EPSON EU-T500 ReceiptE4
      -Set the Sandbox function to "Isolated" (OS: Windows7/Microsoft Windows Server 2008 R2 or later).
         -When installing using an installer, set the Sandbox function to "Isolated".
         -When installing with Point & Print, set the Sandbox function to "Isolated".
         -When installing with Plug & Play, set the Sandbox function to "Isolated".
         For the "Isolated" setting:
           This setting allows you to operate a printer driver on a process separating from Spooler process.
           By setting each printer driver to "Isolated",
           all the printer drivers will not stop even if one of them stops because of some error occurrence.
      -In Paper layout setting tool of TM-L90, support 5-inch or more label length.
       The maximum length: "279.4mm (11inch)".
      -Eliminated "Wireless Offline Count"from the Ethernet port setting dialog.
      -The following problems have been solved:
         -TM-C100 silent package is not created.
         -When repeatedly rebooting a PC with two or more printers connected and their power ON,
          the port settings are automatically changed on the PC side. 
         -When an application using the StatusAPI is crushed in command transmission,
          the printer may not normally operate until the power is OFF and then ON.
         -No command is transmitted even if setting to "Send command" with TM-L60II Label.
         -After installing APD on WindowsXP SP2, a system error occurs when rebooting the OS.
         -After printing using EPSON Flash logo tool, ASB of the Status API will not be noticed.
         -There is no response when clicking a printer icon after stopping the Print Spooler while printing and
          then re-executing it.
         -Printer offline caused by the buffer full in printing is noticed to the status (status of PrinterInfo
          structure of the OS) displayed on the printer. 

  Ver4.07
      -Supports the following OS
          Microsoft Windows Embedded Standerd 2009 32bit
          Microsoft Windows Embedded POSReady 2009 32bit
          Microsoft Windows Vista 32bit SP2 English
          Microsoft Windows Vista 64bit SP2 English 
          Microsoft Windows Server 2003 R2 64bit SP2 English
          Microsoft Windows Server 2008 64bit SP2 English 
      -Added support model
        TM-U120II
      -The following problem has been resolved:
         -When the Protected Mode of the IE7 security settings is enabled (the lowest right),
          the StatusAPI displays an error dialogue.
         -Right after the print completion status is obtained, an error that executes
          BiDirectIO/BiDirectIOEx is returned
         -Even if an IP address is specified with the zp option during the silent installation,
          the setting is not reflected.
         -When two or more printers are silently installed, they are not installed with
          the correct port setting.
         -When BiSCNSetCutSize is specified and scanning is executed, the obtained image is deleted
         -Even when BiESCNClearImage is executed, stored image files are not deleted.
         -Layout setting with the paper layout set tool for the TM-L90 with the Ethernet connection
          causes an error and fails.
         -When using the TM-U375, TM-U295, TM-U950, or TM-L60II with the parallel connection,
          an incorrect status is repeatedly displayed.

  Ver4.06a
      -The following device font properties of each printer have been changed.
         FontAxx
         FontBxx
         Barcodex
         2D-Codex
         Control
         ConrolA
         etc
      -An improvement to eliminate the need for rebooting the PC on the upgrade installation has been made.
      -The following problem has been resolved:
          -While making printer settings for the TM-J7000/7100 and TM-J7500/7600, ÅgDenseÅh set for
           ÅgCharacters per line" does not become effective.

   Ver4.06
      -Added support model
        TM-T58
      -Added the function to specify the horizontal print position for logo printing of the printer driver.
      -Changed to continue uninstallation when an error occurs during uninstallation.
      -Changed to copy the bitmap file, which is specified for watermark/logo printing of the printer driver,
       to the destination PC when the silent installation is executed.
      -Corrected the following defects.
         -The Status of the PRINTER_INFO structure is not updated for the EU-T300/EU-T400 printer.
         -FontAxx[255] and FontBxx[255], that are not available with the TM-U295, are supported.
         -Installation fails when the file path where the print log file cannot be output is specified.
         -After the upgrade installation from the APD Ver3, "EpsStmApi.dll" remains even when 
          the APD Ver.4 is uninstalled.
         -Correct a misdescription in the silent installation creation screen.
         -The tab in the print data does not become active even when it is specified.

   Ver4.05
      -GS1 bar code printing function has been added to the TM-P60 Peeler printer driver.
       The print results stay the same as those for RSS bar codes.
      -Problems with the USB device driver have been fixed.
      -The following problems have been fixed:
         -If the silent installation function is used to install the TM-L90 printer driver,
          the Paper Size set by the paper layout setting tool is not installed.
         -If the silent installation function is used to install the TM-L90 printer driver,
          the User Defined Paper Size is not installed.
         -If the silent installation function is used to install the TM-L90 printer driver,
          the Start button for the paper layout setting tool is not displayed.
         -When printing using a Slip driver, if the Slip driver is uninstalled 
          while the printer is waiting for the slip to be removed, an error occurs.

   Ver4.04
      -A function that specifies the brightness of the print results during graphic printing has been added.
      -The TM-H6000III slip printer has been equipped with a printer driver that performs
       revolving printing of the printerÅfs built-in fonts.
      -The TM-C100 printer driver has been equipped with a new function that retries printing
       of the page when printing has failed. 
      -The following problems have been fixed:
          -When execution of printing and the calling of StatusAPI from the application coincide,
           the CPU utilization may remain high.
          -With a printer using the UB-E02 board, Cover Open status is not issued in some cases
           even if the printer cover is opened at the beginning of printing.

   Ver4.03
      -The TM-C100 printer driver has been equipped with the following additional features:
        Specifying the print starting position
        Specifying the number of pages to cut 
        Linking the paper type and properties
        Support for Windows2003Server
      -The TM-C100 printer has been modified so that no improper properties can be set. 
      -The time required from when the printing starts on the application until when the printer actually
       starts printing has been reduced.
      -The installer has been modified to allow port settings with silent installation.
      -The memory usage used to keep increasing when printing was repeated with WindowsXP SP2,
       but this problem has been eliminated.
      -The TM-P60 printer can now be connected to the serial interface.

   Ver4.02
      -Added support model
        TM-C100, BA-T500, EU-T300, EU-T400, EU-T500
      -In Windows Vista, the problem that users other than the user who 
       performed the installation cannot print is corrected.

   Ver4.01
      -Added support OS
        Windows Vista SP1(32bit) is corresponded. 
      -Added support model
        TM-H5000II, TM-H5200, TM-H6000II, TM-J7000, TM-J7100, TM-J7500,
        TM-J7600, TM-L60II, TM-L90, TM-L90Peeler, TM-P60, TM-P60Peeler,
        TM-T70, TM-T88III, TM-T90, TM-U120, TM-U230, TM-U295, TM-U375, 
        TM-U590, TM-U675, TM-U950, DM-D110, DM-D120, DM-D210, DM-D500
      -Devmode API is added. 
      -Sample program is added.
      -TM Flash Logo Setup utility is added.
      -The paper layout set tool (utility only for the TM-L90) is added. 
      -The convenience of the bar-code and 2D-Code is improved. 
      -The convenience of the installer is improved.  
      -The printer did extra paper feed when the last data of the page is device 
       font at Paper Conservation is "None" setting.( For all receipt printer/label printer). 
       We corresponded this phenomenon.

   Ver4.00
      -New release. 
