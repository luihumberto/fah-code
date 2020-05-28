Folding@home Client Changelog
=============================

## v7.6.13
 - Wait to print info blocks to log until after GPUs are detected.

## v7.6.12
 - Don't download GPUs.txt when using ``--send-command``.
 - Fixed GPUs.txt timestamp check.

## v7.6.11
 - Reduce max delay from 6 hours to 1.

## v7.6.10
 - Fix data dir removal confirmation message in Windows.
 - Download GPUs.txt at startup before configuring the slots.

## v7.6.8
 - Remove bug submission dialog, point to GitHub instead
 - Use PUT instead of GET to access web session ID.  Probably more secure.

## v7.6.7
 - Make sure Web control gets opened when requested.

## v7.6.6
 - Fix ``slot-options`` command response header

## v7.6.5
 - Always allow 127.0.0.1 access to web server.
 - Update GPUs.txt even if GPUs are not currently enabled.
 - Instead of altering data dir in Windows, confirm removal.
 - Remove unsupported windows themes on install.

## v7.6.4
 - Make sure Windows data directory ends with ``\FAHClient``.
 - Fix Linux service shutdown.
 - Avoid caching old Web interface.
 - Fix for Windows service install.
 - Fix Windows start menu.

## v7.6.3
 - Organize info blocks

## v7.6.1
 - Mask newer GLIBC calls for better Linux compatibility.
 - Add COVID-19 option.
 - Hardened command server and Web interface security.

## v7.5.2
 - Updated missing GPU slot messages to prompt user to install the driver.
 - Updated copyright.

## v7.5.1
 - OSX installer updates. @kbernhagen

## v7.5.0
 - Fixed client memory leak.
 - Some spelling fixes.

## v7.4.18
 - Fixed user stats link in Web control.
 - Fixed create team link in Web control.
 - Fixes Google+ share link in Web control.
 - Automatically uninstall conflicting files in Windows installer.
 - More thorough termination of F@H apps in Windows installer.
 - Removed option to install for all users in Windows installer.
 - Fixed Windows CPUID problem which causes fail to assign to CPU slots.

## v7.4.17
 - Updated assignment servers.
 - Use same AS for GPU slots.
 - Update URLs to point to foldingathome.org.

## v7.4.16
 - Removed support for reading Gromacs trajectory files.
 - Skip over non-GPU OpenCL devices during detection.
 - Pass both CUDA and OpenCL device indices to GPU cores when available.
 - Fall back to guessing GPU indices when drivers cannot be loaded.
 - Added message to indicate why GPU drivers were not detected.
 - Don't inadvertently remove GPU index options from config.
 - Correctly handle PCI bus/dev IDs > 127.
 - Fixed AMD PCI bus/slot code.
 - Report GPU PCI function in info.
 - Fixed detection of multiple GPUs of the same type. #1161
 - max-packet-size=normal (the default) redefined to mean 25MiB. #1154
 - Report more CPUID feature flags, specifically to detect RDTSCP.

## v7.4.15
 - Fixed further FAHControl connection dropping issue related to UTF-8 encoding.
 - Fixed invalid PyON escape sequences in remote interface.
 - Convert Windows error messages to UTF-8 to avoid parsing problems.
 - Updated GPUs.txt.

## v7.4.14
 - Fixed FAHControl connection dropping issue.

## v7.4.12
 - Fix for AS assigned max CPUs.

## v7.4.11
 - Removed small prime CPU count avoidance code.
 - Let AS specify max CPUs for each WU.
 - Removed libGL.so dependency.

## v7.4.10
 - Attempt to fix hung downloads.  #983
 - Don't default to CPUs counts which are small primes greater 3.

## v7.4.9
 - v7.4.8 bug fix.

## v7.4.8
 - Using GCC 4.8 to avoid libstd++ incompatibility in Linux. #1147
 - Fixes CUDA version parsing and removes CUDA debug information.

## v7.4.7
 - Report zero CPUs to AS for GPU slots.  #1139

## v7.4.6
 - Smarter GPU detection.
 - Report OpenCL devices on command line.
 - Report OpenCL & CUDA devices to AS.

## v7.4.5
 - Fixed 100% CPU lockup on core 0xa4 exploded proteins.
 - Add support for streaming core.

## v7.4.4
 - Fixed failure to update GPUs.txt file.  #1115
 - Don't delete slots on initialization error.  #1117
 - Always allow 127.0.0.1 (localhost) to connect to FAHClient.  #1120
 - Tweaks to Web control.  #1116
 - Don't display points for Anonymous or team 0.

## v7.4.3
 - Allow saving cuda-index=0 and opencl-index=0.  #1106
 - Fixed Failed to remove directory './work/00'.  #1058
 - Fixed GPU Names Are Too Long.  #1061
 - Removed links to Advanced Control and 3D Viewer.  #1110
 - Changed Web Control menu too look more like NaCl client.
 - Updated year.  #1090
 - ATI -> AMD.  #1091
 - Change debian default 'anonymous' -> 'Anonymous'.  #1113
 - Improved GPUs.txt download.
 - Added 'paused', restored function of 'pause-on-start'.  #1100
 - Resolve all AS IP addresses and try each one.  #1094

## v7.4.2
 - Don't repeat "Frame timer not running' indefinately.  #1105

## v7.4.1
 - Save config.xml on any changes.
 - Fixed QRB calculation, again.  #1044
 - Report progress down to 0.01%.
 - Correct for cores which report incorrect frame/step. #888
 - OSX: workaround for slow communication on 10.9 as service.  #1103
 - Removed trigger-save command, no longer necessary.
 - Only allow one visualization type per WU.
 - Update GPUs.txt when gpu=true, log message on update.

## v7.4.0
 - Disabled stall detection by default.
 - Added options stall-detection-enabled, stall-timeout & stall-percent.

## v7.3.13
 - Fix 'cpus' count.  Use user value if set.  #1074
 - Swapped user and team in bug report.  #1076
 - Hide overflow on slot tabs.  #1061
 - OSX: idle on login window or display sleep.  #944
 - Only autoconfigure Fermi or better NVidia GPUs in Linux.  #1084
 - Fixed error when all slots are removed.  #1088
 - Project links open in new window/tab.  #1079
 - Hide upper right close button on dialogs.  #1078
 - Wait at least 30 minutes & 5% before declaring WU stalled.  #1059
 - Added assign-gpu2.stanford.edu as backup GPU AS.

## v7.3.12
 - Don't open FAHViewer fullscreen from Web Client.  #1067
 - Attempt to fix stall detection.  #1059
 - Catch and suppress "Failed to wait on process ####:No child processes"
 - Idle applies to each slot.  #1060
 - Attempt to fix long GPU name jumble.  #1061
 - Show yellow spinner for finishing in Web Control.  #1065
 - Updated default CPU counts.  #1013
 - Accept IE 11 masquerading as Mozilla 11.  #1073
 - Display full bug URL after report.  #1071
 - Fixed project description layout.  #1068
 - Various Web Control tweaks.  #1062, #1063, #1064, #1070
 - Fixed bug when converting a CPU slot to GPU slot while running.
 - Autoconfigure GPU slot in 64-bit Linux.

## v7.3.11
 - Experimental installer improvements.
 - Slots remember pause status through restart.
 - New Web client design.
 - Separated power/pause/on-idle.
 - Points in Web client.
 - Limit max-unit-errors and max-slot-errors to range (1, 20).  #1020
 - Use SMP:N-1 by default if any GPU slots exists.  #1013
 - Don't try to cleanup if WU is still running.  #1037 #1023
 - Detect stalled WUs and dump.  #1043
 - Fixed QRB calculation.  #1044
 - Don't return failed WUs after their expiration.  #1030
 - Only compute bonus if passkey is set.  #1040
 - Fixed reset of slot boolean options.  #984
 - Only warn on invalid options during startup.
 - Read Core 0x17 JSON visualization files.
 - Autoconfigure CPU slot first.  Changes default order.
 - Better recovery of Web Client on reloads.

## v7.3.10
 - Added 'gui-enable' option to allow disabling the GUI in Windows.
 - Added 'web-enable' option to allow disabling the Web server.
 - Added 'command-enable' option to allow disabling the command server.

## v7.3.9
 - Fixed command-address='' to disable command server.

## v7.3.8
 - Increased the default number of processing threads from 4 to 6.
 - OSX: Moved apps to /Applications/Folding@home/.
 - OSX: Renamed FAHClient.url to Web Control.url.
 - OSX: Added uninstaller package.

## v7.3.7
 - Use timeout for initial ETA estimates so WU doesn't hang at 0%.
 - Show progress to 1/1000ths place.
 - Increase default max-slot-errors to 10.
 - Reset slot error counts when power-level changes.
 - Fixed cause pref update in Web Control. #986

## v7.3.6
 - Submit version with uninstall report.

## v7.3.5
 - pause-on-start pauses slot rather than setting power=off.
 - Optionally send brief details with uninstall report.
 - Updated Linux packages for folding power changes.

## v7.3.3
 - Simplified FB link.
 - Added Twitter and email links to Web Control header.
 - Pointed Google +1 link to http://folding.stanford.edu/
 - (Un)hide passkey on mouse over.
 - Fix logic error in previous fix for #965.
 - Fix Web Control in IE8.
 - Switched Twitter accounts.
 - Don't show RECONFIGURING when slot is turning off.
 - Fix CSS caching problem.
 - Added warning for unsupported browsers.
 - Removed throbber.
 - Added new -gpu-vendor core option for upcoming Zeta core.
 - Install but don't enable screensaver by default.
 - Upgraded Web Control to jQuery 1.9.0 and jQuery-UI 1.10.0.
 - Added option 'open-web-control'.
 - Folding@home shortcut starts FAHClient and opens Web Control in Windows.
 - Fixed: Finish-pause-finish does not finish the WU. #961
 - pause-on-start is now means set folding power to off at startup.
 - Remove old FAHContorl desktop link from v7.2.9.
 - Added uninstall reason reporting.
 - Use away mode notification instead of user input for idle in Windows.
 - Faster remote updates.
 - Added 'idle' option for individual slots.

## v7.3.2
 - Remove desktop link on uninstall.
 - Avoid stylesheet caching.

## v7.3.1
 - Attempt to solve excess disk IO problem.
 - Wait up to 5 minutes for user idle, but prevent sleep if waiting.

## v7.3.0
 - Don't keep computer from sleeping when on battery.
 - Removed "Validate Name" button from Web interface.
 - Name change "Web Client" -> "Web Control".
 - Added FAHWebControl to menu in Linux.
 - Avoid caching of main Javascript code.
 - Updated copyright dates.
 - Only one instance of Web Control. http://caniuse.com/#search=webstorage
 - Default level "medium" for machines wo/ a battery.
 - Don't both cut the number of CPUs and throttle by default.
 - Display version in Web page title.
 - By default only allow Web access from localhost regardless of 'allow'.
 - Log HTTP access errors as warnings.
 - WU not downloading at 100%, i.e. before current WU upload. #970

## v7.2.14
 - Change systray icons based on activity or failure.
 - Use system idle information as well as screensaver for idle modes.
 - Keep system from sleeping while folding. (Windows and OSX only)
 - Text changes to Web interface per suggestions in forum.
 - Added "Validate Name" button in Web interface Identity tab.
 - Signed installer. (Windows) #343
 - Changed "Restarting" to "Reconfiguring".
 - Stopped using cookies for session ID due to iframe/cookie issue w/ Safari.
 - More robust loading & timeout message for Web client.

## v7.2.13
 - Merge SMP and Uni slot types into one CPU type. #586, #693
 - Implemented new folding power levels.  #396
 - Only, but always, restart cores if # CPUs or % usage has changed.
 - Eliminated waiting between successive, intentional core restarts.
 - Hide HTTP messages at log level 3 in Windows too.
 - Changed ambiguous date format in log.  #947
 - Added Systray GUI in Windows.  #217, #565, #487, #321
 - Allow moving config and logs across file systems.  #965
 - Auto restart cores after relavant configuration changes. #261

## v7.2.12
 - Don't display fractions of credit points to reduce queue_info updates.
 - Added Web interface on port 7396.
 - Removed 'screensaver' option.
 - Added 'power' option.
 - Linked Web server 'allow' and 'deny' to 'command-allow' and '-deny'.
 - Removed quotes from GPU slot description.
 - Auto configure a SMP or Uniprocessor even if a GPU slot is configured.

## v7.2.11
 - Install with screensaver by default.
 - After 5 minutes w/ no config attempts automatically set configured=true.

## v7.2.10
 - Dropped 'unpause-while-connected <slot>' remote command.
 - Added 'screensaver' remote command.
 - Made slot-info and protein trajectory available even when paused.
 - Added slot pause reason information.
 - Add screesaver option to windows installer.
 - Choose appropriate startup command after windows installer finishes.
 - Added 'send-command' command line option.
 - Added 'send-(un)pause' and 'send-finish' command line options.
 - Shutdown any running clients on windows install.
 - Default 'pause-on-battery' to true. #743
 - Fixed: Limit ERROR: Exception: Have already seen this work unit. #496
 - Added 'configured' command which reports of the client was configured.
 - If not configured, don't start folding.
 - Added 'fold-anon' configuration option, fold even if not configured.
 - After 5 minutes if no connections automatically enable 'fold-anon'.
 - Removed client configuration options from windows installer.
 - Default gpu=true on Windows only.
 - Default smp=false if ATI GPU detected.
 - Windows: Remember custom data directory during upgrade. #838

## v7.2.9
 - Added 'unpause-while-connected <slot>' remote command.

## v7.2.8
 - Start FAHControl optionally after installer finish. #471

## v7.2.7
 - Use new dependency based init.d scripts if available in Linux.
 - Disable init.d rather than use /etc/defaults/fahclient to stop autostart.
 - Fixed a crash when loading bad protein data.

## v7.2.4
 - Link libssl libcrypto and libexpat statically in .deb.  #893
 - Warn on init.d start when /etc/default/fahclient has ENABLE=false.
 - Remove /etc/default/fahclient on --purge.
 - Added 'force-start' option to init.d script.

## v7.2.1
 - Added Installed-Size control field to .deb.  #853
 - Try to stop and uninstall service before install.  #922
 - Download GPUs.txt if there GPU slots or no slots and gpu=true. #920
 - Stop trying to load .tpr and .xtc files which have failed twice.  #917
 - Don't load .tpr until core has a chance to write.
 - Don't try to load .tpr/.xtc for core 0x11. #919 #916
 - Don't load .tpr/.xtc while core is loading.  #919

## v7.2.0
 - Replace invalid characters in user name by '_'.  #903
 - Fixed repeated 'gpu-index' error on GPU slot delete.  #874
 - Fixed misuse of PCI subvendor IDs.  #881
 - Changed error:OK to error:NO_ERROR in log to avoid confusion.  #892
 - "Viewer" menu items to "View" for consistency.  #899
 - Fixed text.  #891
 - If there is no systray, window close will exit FAHControl.  #900
 - Display 'Unknown' for 0 estimated PPD.  #901
 - Automatically update GPUs.txt.
 - Log warning if core returns an error code.  #887
 - Remap FERMI GPU type to NVIDIA with FERMI species in GPUs.txt.
 - Request IPv4 addresses until we support IPv6.

## v7.1.52
 - Account for ',' as decimal point in some locales.  #849

## v7.1.51
 - Allow parsing GPUs.txt with Windows CRLF line endings.
 - Allow setting GPU type and species from GPUs.txt.

## v7.1.50
 - Don't return WU results if they are less than 512 bytes.

## v7.1.49
 - Improved Windows install error message.
 - Fixed next-unit-percentage.  #842
 - Attempt to fix negative/wrong PPD numbers.  #843
 - Track project runtime estimates per slot.  #828

## v7.1.48
 - Added code to the Windows installer to stop the service.
 - Fixed Windows default theme.

## v7.1.47
 - Fix Error popup: gpu-index has no default.  #802
 - Added PPD calculation.  #408
 - Ignore ETA calculations that are triggered during folding core startup.
 - Fix OSX data directory permissions.
 - Don't use estimated progress to decide when to download new WUs.

## v7.1.46
 - Integrated caxalot's OSX install script changes.
 - Run as user nobody in /Library/Application Support/FAHClient on OSX.
 - Fixed windows installer copyright.  #832
 - Retry windows install if client running.
 - Attempt to fix builds for OSX < 10.6.  #572

## v7.1.45
 - Improved WU error handling, retry and recovery.
 - Added 'Z' to times to indicate UTC for ISO 8601 time format.
 - Update viewer eta and progress information more often.
 - Second attempt at FAHCoreWrapper '-lifeline' usage
 - Removed Windows installer check for previous install.  #825, #726
 - Fixed debian configuration questions.  #749
 - Don't allow progress estimate to go over 100%.  #395
 - Don't build OSX app for client.  Instead install to /usr/bin.
 - Use corrrect user home directory in OSX.  #826

## v7.1.44
 - Cause FAHCoreWrapper to automatically exit if client dies.  #794
 - Improved ETA/TPF/PPD estimation. #395
 - Update GPU index allocation after slot delete or modify.  #788
 - Add Debian dependency on libssl.so.0.9.8.  #791
 - GPU white list updates. #778

## v7.1.43
 - Only update active project descriptions.
 - Retry failed project description updates at most every 5 minutes.
 - Work around Windows socket blocking write problem.  #762
 - Updated copyright dates.

## v7.1.42
 - Networking code overhaul.

## v7.1.41
 - Added Tesla M2075 GPU.  #766
 - Ignore SIGPIPE in FAHCoreWrapper.
 - Fixed OSX lanuchd usage. #638
 - Fixed socket timeout/heartbeat issues.  #762, #764, #765, #775
 - Print slot number with nearly all WU messages.  #769
 - Print core number with core emitted log messages.
 - Changed log tag order to WU##:FS##:0x##
 - Fixed core wrapper interrupt/kill handling.

## v7.1.40
 - Fixed some debian package problems.
 - Get actual core PID from core wrapper and wait for it when stopping core.
 - Fixed finishing a paused slot problem. #755
 - Fixed GPU allocation problem.  #767

## v7.1.39
 - Obscure passkey even when saved as a slot option. #742
 - Added FAHCoreWrapper which handles soft core shutdown.  #563
 - Removed code which kills cores which are known to not shutdown softly.
 - Add 'Upload' & 'Download' to percent in log.  #532
 - Convert 'Unit ##' and 'Slot ##' to 'WU##' and 'FS##' in log.  #686
 - Resolved many of the lintian warnings & errors on the .deb package. #745
 - Keep queue entries sorted by ID in FAHControl.
 - Added log filtering to FAHControl. #157
 - Preload much more of the log.
 - Print date to log periodically.  #122
 - Slightly increased OSX DMG window size. #583
 - Restored --info functionality in FAHViewer.
 - Custom donor and team stats links. #673
 - Fixed bug in project information downloading.
 - Removed build machine names from packages.
 - Added more log information for core crashes return codes in Windows. #753
 - Fixed a multi-vendor GPU indexing bug.  #756
 - Use blocking socket writes in an attempt to fix #682.
 - Split deb, RPM and OSX packages.
 - Removed dependencies on GL libraries. #751
 - Don't enable GPU by default in .deb config.  #749
 - Integrated most of smoking2000's .deb package improvements.
 - Unpause WU on finish. #755
 - GPU white list updates.  #752

## v7.1.38
 - Fixed network connection dropping.

## v7.1.37
 - Added missing wraplabel.py file to FAHControl.
 - Changed socket error message verbosity.
 - Fail WU on UNSTABLE_MACHINE immediately & return for partial credit. #615

## v7.1.36
 - Fixed a potential socket connection bug.  Maybe related to #734.
 - Added several NVidia cards to GPUs.txt. #737.
 - Improved Linux on battery detection. #738.
 - Print WU error state on WU status line.
 - Emit correct exception on FAH transaction failure.  #615.
 - Fixed debian package install core permissions problem.  #732.
 - Removed core byte order warning.  #602.
 - Added GPL link to FAHControl about. #736.
 - Ask user, team, passkey and mode during .deb package install. #739.

## v7.1.35
 - Added 'Enchanter' theme. #731
 - Renamed 'Wimp' to 'Windows-Default'. #731
 - Unminimize FAHControl window on unhide. #567
 - Better core download failure message. #161
 - Cleaned up project descriptions using html2text.py.
 - Store project data in client DB.
 - Use system default font size.  #733
 - Added project info to viewer. #575.
 - Added clickable buttons to viewer.
 - Fixed FAHViewer crash introduced in v7.1.34.
 - Fixed mouse wheel scrolling in FAHControl. #463.
 - Fixed color difference for text boxes. #698.
 - Changed FAHControl window name. #711.

## v7.1.34
 - Fixed CPU consumption in client connections. #702
 - Really fixed "Wrong architecture" bug on 32-bit Ubunut. #599
 - Only warn on config errors. #722
 - Log error and continue of command server fails to initialize.
 - Fixed Slot configuration text.  #717
 - Use -1 or 0 for CPUs default to be consistent with GPU options.  #717
 - Disabled no longer supported AMD X1300 - 1900 GPUs.
 - Added "OpenGL Render" to info in FAHViewer.  (For blacklisting)
 - Added 'override-blacklist' option to FAHViewer. (Nothing black listed yet)
 - 'OK' -> 'Save' in FAHViewer preferences window. #724
 - Fixed NVIDIA_DEV.1244.01 = "NVIDIA GeForce GTX 550 Ti" detection.
 - Added the 'Wimp' theme and win32 theme engines. #723
 - Made 'Wimp' theme the default in Windows. #713
 - Added heartbeat to viewer<->client connection to timeouts dead connections.
 - Stop trying FAILED, FAULTY and DUMP reports if WS connection was made. #728
 - Check WS server versions for unreasonable values.  #728.

## v7.1.33
 - Set default 'gpu-usage' to 100%, until GPU cores implement better throttle.
 - Fixed client connection rate limiting.
 - Fixed error reporting for bad slot configuration. #582.
 - Attempt to fix EUE reporting for WSv4.  #615.
 - Fixed "Wrong architecture" bug on 32-bit Ubunut. #599.
 - Dropped "64-bit" Windows release.  Use 32-bit on all systems.

## v7.1.32
 - Added 'gpu-usage' option with default of 80%.
 - Added percent GPU usage slider in FAHControl.
 - Added 'opencl-index' and 'cuda-index' options to FAHControl.
 - 'gpu-id' -> 'gpu-index' in FAHControl.

## v7.1.31
 - Another attempt to fix OSX PCI scan crash.

## v7.1.30
 - Attempt to fix OSX PCI scan crash.

## v7.1.29
 - Print UNSUPPORTED in front of unsupported GPUs in info.
 - Removed unsupported gpu-vendor-id and gpu-device-id options.
 - Allow auto-configuring both GPU and SMP. #629
 - Configure GPU & SMP by default in Windows.
 - Repaired OS description printing in info.
 - Use OS bits to determine 32 vs 64 rather than build bits. #703
 - Enabled GPU detection in OSX.
 - Removed 'gpu-id' and added 'cuda-index' and 'opencl-index' options.
 - GTX465 -> Fermi. #661
 - Automatically install themes in Windows installer.

## v7.1.28
 - Hopefully finally fixed the OSX on battery detection code.
 - More GPU whitelist changes.

## v7.1.27
 - Check shared info modification time in an attempt to fix #688.
 - More GPU whitelisting.
 - Fixed Windows PCI/GPU detection, broke in v7.1.26. #701.
 - Use WS UTC WU assign time in client wo/ computing offset #697, #681.
 - If running WU is dumped shutdown the core. #700.

## v7.1.26
 - Correctly report client version to WS with WU return.
 - Failed upload attempt could cause WU to dump before it was expired. #679.
 - Added AMD Radeon HD 6600 Series to GPU white-list.
 - Fix failure to restart FAHControl in OSX when 'start minimized'.  #649.
 - Fixed a socket bug that could cause the loss of the end of a message.
 - Build OSX client in 32-bit mode with Intel compiler.
 - Reduced socket send buffer size to 32KiB to try to solve #682.
 - Attempt to fix PCI detect crash in Windows. #695.
 - Whitelisted more GPUs.

## v7.1.25
 - Hide 'Quit on window close' option in OSX.
 - Fixed some problems with WU assign time and time offset calculations.
 - Detect and ignore invalid assign time from older WS.
 - Log computed WS time offset.
 - Removed warning from Slot configuration about changing threads mid-run.
 - Catch and log error accessing battery info in /sys on Linux
 - Fix grayed out name and IP in client add after viewing local client. #640.
 - Remove 'RS480 PCI-X Root Port' from GPU whitelist. #635
 - Added a few new Radeon HD 6xxx cards.
 - Added Nvidia GTX 590 device ID 0x1088 to whitelist.
 - Increase Radeon HD 5xxxx and 6xxxx GPU type level by one. #653.
 - Don't fail WS connections if all data was recieved even on net error.
 - Print IP Address with 'Uploading' message.
 - Fixes for OSX minimize and quit bugs. #649 & #659.
 - Limit max CPUs per slot to system count. #652.
 - Attempt to fix #654.
 - Release system resources when querying OSX battery status.  #650.
 - Don't send 'auth' command from FAHControl if empty. #658.
 - Fixed 'slot-add' NULL pointer exception. #666.
 - Fixed 'log-updates start' error. #671.
 - Fixed FAHClient script parsing bug. #676.
 - Show 'Remote Access' tab in advanced mode. #648.
 - Don't allow minimizing to sys-tray if it is not there.  #670.
 - Also print core return code numbers in hex. #677.
 - Print times in ISO 8601 format. #664.
 - Expire WUs in sending status.

## v7.1.24
 - Don't download a new WU if max-units is reached. #607
 - Added GeForce GTX 460 SE to the white-list.
 - Fixed 'core-priority' in FAHControl.
 - Fixed options save.
 - Don't allow changing 'local' client name or IP.
 - Don't try to autostart the local client once online.
 - Fix permissions problem in RPM. #627
 - Hide 'Status' tab in novice mode.
 - Added project info.  In novice mode only by default.

## v7.1.23
 - Fixed bug caused by ignoring WU return code after a quick pause/unpause.
 - Set default verbosity to 3.
 - Explictly white-list Fermi GPUs & downgrade if CUDA driver is insufficient.
 - Added new GTX 470, 485 and 590 to GPU white-list.
 - Moved FAHControl single app port within 0-65535 range.  #604.
 - Filtered out 'Theater' from GPU list.
 - White-listed Nvidia Quadro G8x cards.
 - Move all ATI R700s GPUs to species 3 and R800s to species 4.
 - Don't allow passwordless access even if password is not set.
 - Don't automatically allow IPs in command-allow-no-pass.
 - Don't call battery status code if not necessary.
 - Release resources related to battery query in OSX. #593
 - Allow changing the number of CPU threads mid run but warn. #292
 - Fixed client new and client connection options saving. #617
 - Lock database on startup to stop multiple runs of FAHClient in same dir.
 - Pass '-service' option to core when running as a Win32 service. #592
 - Fix permissions for All Users Windows install. #595.

## v7.1.22
 - Added proxy support with authentication types: none, basic & digest.
 - Added proxy configuration tab to FAHControl.

## v7.1.21
 - Another attempt at fixing the package permissions problems.

## v7.1.20
 - Fixed DMG permissions.
 - Show 'Error' when CUDA detection fails.
 - Suppress FAHClient startup text by default for package installers.
 - Warn that cores can take up to 1 min to shutdown when uninstalling.

## v7.1.19
 - Order clients by name. #510
 - Fixed permissions on debain package installs.
 - Improved handling when a subprocess fails to start.
 - Add window titles to FAHControl dialogs.
 - Remove ATI 1xxx cards from GPU whitelist.

## v7.1.18
 - More GPU whitelisting.  All ATI HD series.  Only HD 5/6000 on Core 0x16.
 - Use OS logical CPU count instead of CPUID counts.
 - Hide/restore any open dialogs with main FAHControl window.
 - Don't allow opening more than one dialog via the sys-tray menu.
 - Restore main window on preferences or about from sys-tray menu.
 - Change configure dialog OK button to Save.
 - Fixed AS hammering, #511.
 - Fixed 'Waiting On' message problems.
 - Use heartbeat to timeout FAHControl connections.
 - Fixed damage to active client's config when adding new client. #536.
 - Catch property save error on FAHControl close in Windows 2008.
 - Disallow saving both config and address/port changes in FAHControl.
 - Fixed CUDA driver version reporting. #571.
 - Fix file and directory permissions in .deb and .rpm packages.
 - Added volume icon for OSX DMG package.
 - Hopefully fixed sidebar issue in DMG.  #516.
 - Fixed local FAHClient shutdown with 'Stop' button on Windows.
 - Removed extra linefeeds from copied log.  #428.
 - Merged FAHViewer <-> FAHClient and FAHControl <-> FAHClient interfaces.
 - More idle time optimizations for FAHViewer, FAHControl and FAHClient.

## v7.1.17
 - Really whitelisted some more GPUs.

## v7.1.16
 - Use core count not thread count for SMP autoconfiguration.
 - Clear FAHViewer info when disconnected.
 - Whitelisted some more GPUs.
 - Removed ATI Mobility GPUs from whitelist.
 - Fixed cpu core/thread/logical detection.

## v7.1.15
 - Print 'CUDA not detected' in info.
 - Attempt to fix broken CUDA detection.

## v7.1.14
 - Ignore CUDA library exceptions.

## v7.1.13
 - Fixed problem with editing client in FAHControl when not connected.
 - Fixed next-unit-percentage rounding error.
 - Removed threading and polling in FAHControl.
 - Created developer interface for FAHClient.
 - Dropped follow log control.
 - Fixed bug in connecting FAHViewer when no slot is selected in FAHControl.
 - Added heartbeat between FAHControl and FAHClient.
 - Added local client command in FAHControl preferences.
 - Let FAHClient crash rather than catch unknown exceptions at top level.
 - Added button to manually start and stop local client from FAHControl.
 - Display error dialog if client authorization fails.
 - Fixed slot popup menu actions bug.

## v7.1.12
 - Fixed --info printing for FERMI GPUs.
 - Fixed Non-fermi CUDA reporting.
 - Added new core exit codes for GPU cores.
 - Include CPU threads in SMP default core count.
 - Updated CPU count info display.
 - Default next-unit-percentage to 99%.
 - Added color for 'Finishing' state in FAHControl.
 - Fixed bug in highlighting WU for selected 'Finishing' slot.
 - Added warning in FAHControl about changing SMP CPU count mid run.
 - Round the next-unit-percentage calculation to the nearest integer.
 - Fixed arrow key movement in slot and queue list views in FAHControl.
 - Updated FAHViewer icon and use in FAHControl.
 - Fixed problem with selecting slots in FAHControl.  #359
 - Fixed potential problems with CPU count code on single core machines.
 - Quit FAHControl on Window X in OSX.
 - Remove 'Hide' toolbar button in OSX.
 - Fixed crash in OSX on Apple keys.
 - Added OSX dock menu items.

## v7.1.11
 - Fixed FAHViewer fullscreen problems in Windows.
 - Show absolute path to log file in client fail popup.
 - Fixed CPU counting for multiple physical processors.
 - Fixed missing estimated credit field in FAHControl.
 - Fixed bug with removing client from FAHControl.
 - Fixed crash in FAHViewer when switching from Demo to Live data.
 - Don't load Demo protein when connecting.
 - Set environment variable to communicate gpu-id to GPU cores.
 - Added list of known GPUs PCI vendor + device IDs including subvendors.
 - Added support for loading a custom 'GPUs.txt' file in the run directory.
 - Added 'gpu-index' for cases where GPU indexing does not match core's.

## v7.1.10
 - Fix Windows missing icons.
 - Use different icon for FAHViewer.
 - Go back to static linking of libexpat.
 - Popup error message if local client exits in FAHControl.
 - Fixed bug in auto-detecting multiple GPUs.
 - Removed 'gpus' option.
 - Fixed bug which disabled adding slots via FAHControl.
 - Changes to the GPU detection code.
 - Changes to sample-config.xml.
 - Minor textual tweaks.

## v7.1.9
 - Quit popup not viewer on <ESC> or 'q' in FAHViewer popup.
 - Another attempt at fixed i7 CPU core counts.
 - Dump WU entries if the slot is remove and they were not yet downloaded.
 - Fixed arrow key help text in FAHViewer.
 - Clear old values from add option dialog on add option.
 - Clear out added options from client dialog on 'Cancel'.
 - Never migrate Units to deleted slots.
 - Don't report deleted slots to FAHControl.
 - Use mono-spaced font in FAHControl log view.
 - Fixed max-packet-size reporting to AS.
 - Enabled unit processing during up/download.
 - Drop WS if it does not give an assignment.
 - Support running client as a daemon for Linux service install.
 - Moved clientgui.db to FAHControl.db.
 - Look for FAHControl.db in $HOME/.FAHClient in non-Windows.
 - Don't start FAHControl minimized by default.
 - Run FAHClient in $HOME/.FAHClient when started by FAHControl on non-Win.
 - Create proper Debian package with FAHClient service install.
 - Added OSX on battery support.  Thanks to calxalot for the code!
 - Fixed Windows sys-tray tool tip cut off problem.
 - Don't write window size and pane locations to disk as often.
 - If multiple WUs are ready to start, start the one furthest along.
 - Fixed client to core version reporting.
 - Uncapitalized status names in FAHControl.
 - Changed 'Core' to 'FahCore' in logs and FAHControl.
 - Some optimizations to FAHClient's main loop.
 - Look for FAHClient and FAHViewer in same dir as FAHControl.
 - Close FAHViewer with FAHControl if started by FAHControl.
 - Create proper DMG for OSX.
 - Added ellipses after dialog menu items in OSX.
 - Removed extra '(Un)Hide Window' menu item in OSX.
 - Go back to (un)hiding FAHControl when sys-tray icon is clicked.
 - Display 'FAHControl' in 'top' in Linux instead of 'python'.
 - Preload some of the log in the FAHControl window when tailing.
 - Some FAHControl optimizations.
 - Store client data in '~/Library/Application Support/FAHClient' on OSX.
 - Popup error when FAHClient or FAHViewer fails to run in FAHControl.
 - Attempt to fix FAHControl quad click problem.
 - Fixed FAHViewer box drawing problem on OSX and Windows.
 - Added gpu-vendor-id and gpu-device-id configuration options.
 - Fixed potential crash in GPU detection code.
 - Improve fallback to uniprocessor slot.

## v7.1.8
 - Second attempt to fix i7 CPU core detection.
 - Changed NA to Unknown in FAHControl.
 - Added TPF calculation.
 - Removed verbosity from Windows installer to discourage changing it.
 - Handle XML special characters '"&<> in donor name in Windows installer.
 - Added next-unit-percentage option.
 - Changed 'Client Mode' to 'Preferred Mode' in Windows installer.
 - If Folding@home-x86\client.cfg exists load as defaults for Win installer.
 - Removed WU history.
 - Added more low-level GPU information to WS and AS packets.
 - Added default data to FAHViewer.
 - Added rotation and snapshot linear interpolation to FAHViewer.
 - Fixed bug in writing config.xml with 0 slots.
 - Display WU info on click even when slots are finishing.
 - Fixed sys-tray menu / toolbar tooltip inconsistencies.
 - Added viewer to sys-tray menu.

## v7.1.7
 - Don't log 0% up/download.
 - Fixed ETA, Progress, etc. update in Work Unit view of FAHControl.
 - Update WU status when slots is in FINISHING as well as RUNNING state.
 - Fixed CUDA GPU type support check.
 - dump-after-deadline is default true and fixed WU expire checking.
 - Removed most of the logos from FAHViewer.
 - Added CUDA dlls.
 - Do send results if slot is paused.
 - Added help and about boxes to viewer.
 - Fixed up/download percentage in log.
 - Fixed 'fahclient-log.txt' creation problem on Windows.
 - Attempted to fix i7 CPU core detection.
 - Fixed bug in Unit log file following.

## v7.1.6
 - dump-after-deadline is default false for now.

## v7.1.5
 - Display version in FAHControl About.
 - Added "lifeline" support.
 - Fixed process ID detection in Linux.
 - Added support for starting local FAHClient from FAHControl.
 - Don't try to send results if Slot is paused.
 - Save credit information returned by v6.1.3+ WS.
 - Keep WU data in DB as a credit record.
 - Keep Windows debug symbols with .tar.bz2 archive.
 - Store timeout, k-factor and credit from v6.1.3+ WS.
 - Send DUMP reports to v6.1.3+ WS.
 - Estimate ETA, PPD and Credit.
 - Fixed crash after WU completion.
 - Created FAHViewer
 - Detect previous config in Windows installer and offer to keep.
 - Save Windows Installer values when back/forward buttons are clicked.
 - Added CUDA detection code and report coprocessor version accordingly.
 - Fixed FAHControl browser links in Windows.
 - Disallow @?*|<>'" characters in paths in Windows installer.
 - Fixed reporting 64-bit CPU type to AS.
 - Removed language about password defaulting to passkey in FAHControl.
 - Changed up/download pacifier to not hold a log lock.
 - GUI up/download lockout fixed.
 - Use the term "Folding slot" instead of "Computation slot".
 - Rearranged auto-start options in installer and added (Recommended, etc.)
 - Always raise FAHControl window when sys-tray icon is clicked.
 - Validate entries in Windows installer.
 - Added help text for configuration in Windows installer.
 - Detect previous install in installer and offer to run uninstaller.
 - Added Folding Forum link in About box.
 - Offer an Express install mode in Windows installer.
 - Use better Windows icon from v6.
 - Put program directory in PATH in Windows installer.
 - Removed 'Startup' tab from FAHControl.
 - 'autostart' to 'pause-on-start' with opposite meaning and defaulted false.
 - Don't remove old config.xml in Windows installer if install is aborted.
 - Removed FAHControl's 'autostart' option, must reinstall to change.
 - Save FAHControl window dimensions and pane positions.
 - Display ETA, PPD and Credits in FAHControl
 - Added ETA, Credit and PRCG to Novice view
 - Update Work Unit details immediately when queue list entry is clicked.
 - Display completed WUs as well as active ones.
 - Enable log following by default in FAHControl. (Active when selected)
 - Rearranged FAHControl toolbar.
 - Clicking slot activates running WU in FAHControl.
 - Added viewer to slot pop-up menu in FAHControl.
 - Added viewer config to FAHControl preferences pane.
 - Added viewer button to FAHControl toolbar.
 - Align Address in Clients to the left.
 - Fixed tabbing between fields in FAHControl.
 - Dump WUs after they have expired if 'dump-after-deadline' is true.

## v7.1.4
 - Fixed core path problem.
 - Dump or migrate units when slot is deleted.
 - Dump unit if WS does not understand fail report.
 - Fixed SMP unit creation problem.

## v7.1.3
 - Don't exit before killing and saving kill status of stubborn cores.
 - Fixed bug that allows more than one Unit to start in a slot.
 - Don't download core when slot is paused.
 - Store cores in same directory structure as on server.
 - Differentiate cores by URL not type.
 - Regularly check if WUs match their slot's config and migrate or dump.
 - Migrate or dump a unit if it's slot cannot be found at startup.
 - Default to ignore logff signal in Windows service.
 - Set Connection->Password with Remote Access->Password in FAHControl.

## v7.1.2
 - Don't dump WU on PLEASE_WAIT.
 - Fixed slot FINISHING and STOPPING status bug.
 - Improve FAHControl's responsiveness.
 - Remember which cores don't shutdown cleanly also on CTRL-C exit.
 - Clear any WU backoff waits on unpause.
 - Second attempt to fix FAHControl lockout during results upload.
 - Print to log when pausing, unpausing and finishing.

## v7.1.1
 - Don't reset slot highlighter on queue info update in FAHControl.
 - Fixed core unpackaging bug.
 - Fixed Windows file open bug.
 - Raise FAHControl window when run a second time.
 - Always raise window when icon is clicked and FAHControl is not on top.
 - Fixed --dump loop.

## v7.1.0
 - Made incompatible changes to the client DB.
 - Download a new WU when the previous one is 95% complete.
 - Require each slot to have a unique numerical ID.
 - Lock units to one s
