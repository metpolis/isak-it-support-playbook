<h1>PXE Boot Guide (New PC Setup)</h1>

<p>This guide explains how I perform PXE boot when setting up a new PC. It is based on experience with Lenovo laptops and desktops in a corporate environment.</p>

<hr>

<h2>📌 Important context</h2>

<p>PXE boot has been tested on Lenovo laptops and desktops, and in all cases the same ethernet port has been used. A stable wired network connection is required for the process to work correctly.</p>

<hr>

<h2>⚙️ BIOS setup (Required before PXE boot)</h2>

<p>Before starting PXE boot, the BIOS must be configured correctly. The following settings should be verified:</p>

<p>- Wake on LAN: AC only</p>
<p>- Allow boot from network devices: Enabled</p>
<p>- MAC address: Set to internal (use secondary only if using dock pass-through)</p>

<p>After confirming these settings, exit and save the BIOS configuration.</p>

<hr>

<h2>🚀 PXE boot process</h2>

<p>Once the system is powered on, press F12 to enter the boot manager.</p>

<p>From the boot menu, select PXE boot. In this environment, PXE over IPv4 has been used consistently.</p>

<p>When initializing the boot image, ensure that the PC is powered on and connected via ethernet. A stable network connection is required for the image to load successfully.</p>

<p>After the PXE boot process completes, the machine should proceed into the deployment or setup phase and be ready for further configuration.</p>

<hr>

<h2>⚠️ Mistakes I have encountered</h2>

<p>During PXE booting, I have encountered a few common issues that are important to be aware of.</p>

<p>One of the most frequent mistakes was using the wrong ethernet port, which resulted in no PXE connection being established. This prevented the boot process from starting and required troubleshooting before identifying the issue.</p>

<p>Another issue occurred when the secondary MAC address was not properly set when using a dock pass-through. In these cases, the device was not correctly recognized during PXE boot because the network interface used by the dock differed from the internal network adapter.</p>

<p>Additionally, PXE boot was once unavailable due to maintenance on the MECM server. In this situation, the issue was not related to the client device but to the backend infrastructure required for deployment, which temporarily prevented PXE functionality.</p>

<p>These situations highlight the importance of verifying both physical connections and infrastructure availability before starting the PXE boot process.</p>

<hr>

<h2>✅ Summary</h2>

<p>PXE boot is a reliable method for deploying new machines when BIOS settings, network connectivity, and infrastructure availability are correctly configured. Attention to detail is critical, as small misconfigurations can prevent the process from working as expected.</p>
