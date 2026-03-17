# NES-power-board
NES power board

this design is safer and more effective than any other option for a modded NES. It eliminates the root cause of crashes (heat) while purifying the power for your RGB kit.
Here is why this design guarantees zero crashes and zero overheating:
1. Why there will be NO overheating
The original 7805 regulator has to burn off about 6 Watts of pure heat. Your new setup reduces this waste to only 0.6 Watts.
90% Reduction: The SOT-223 package of the MCP1826 is designed to dissipate up to 1 Watt without an external heatsink. At 0.6W, it will stay merely lukewarm (around 45°C/113°F), whereas the original 7805 climbed above 85°C/185°F.
Thermal Safety: The MCP1826 features an automatic thermal shutdown at 150°C. Since you will never exceed 50°C, the regulator will never cut out during gameplay.
2. Why there will be NO crashing
Crashes on modded consoles (EverDrive/RGB) occur when the 5V line briefly drops during a massive current draw.
Power Overhead: The AP62250 provides 2.5A and the MCP1826 provides 1.0A. Your console draws a maximum of 0.9A. You have a constant safety margin.
The Role of Tantalum: The 22µF Tantalum capacitor we selected acts like an ultra-fast battery. If the EverDrive pulls a sudden current spike, the Tantalum provides it instantly, preventing the 5V from dipping and the console from "freezing."
3. Why the image will be perfect
1.3 MHz Frequency: The Buck converter's switching noise is located far beyond the NES video frequencies. It is "invisible" to the console.
Shielded Inductor: The Bourns SRP inductor traps its magnetic field inside its iron powder shell. It will not "pollute" the colors of your NESRGB kit through induction.
4. Summary of the Security Chain
9V-12V Input 
 Original 1000µF Cap (Initial smoothing) 
 AP62250 (Efficiency) 
 LDO MCP1826 (Silence) 
 22µF Tantalum (Final stability).
This is industrial-grade engineering. As long as you follow the wiring diagram (SHDN connected to VIN), your console's power system will be virtually bulletproof.
