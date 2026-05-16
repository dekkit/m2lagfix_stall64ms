# m2lagfix
lag fix for the model2 emulator


**Update 16/05/2026**

Updated to reduce the Stall detection wait time from 128ms down to 64ms.  This was reduce the freeze/glitches when transferring my daytona setup over to PCs with a faster cpu.

**Issue:**  Network game would randomly freeze for 2 seconds.  Even when using m2lagfix on one or both machines, i was still getting intermittent glitches/ freezes of around  .5 seconds (usually 1 -2 per race).
**Resolution:**  Reducing the Stall detection routine, has resolved the intermittent freezes on my setup.  Network gameplay is now smooth, however it does not resolve the flickering purple cars



Changes:
 - 16/05/2026 - Replaced line 224 "If GetTickCount - STALL_Tick >= 128 Then" with "If GetTickCount - STALL_Tick >= 64 Then" .


Note: 
- Installed VB 6 professional (from archive.org) and compiled within a Window XP 32-bit Vmware instance.
-  m2lagfix_stall64ms.exe will trigger a virus alert on Windows 10's Defender (possibly later versions windows as well) .  This appears to be common problem when using old versions of Visual basic to compile code (google for more details).
- My m2 emulator setup is not connected to the internet so the risk for me low.
- I have assumed the compiled code to be a false positive, however have included all source code in case you would like to compile for yourself (please share a version if you can compile without this issue)
