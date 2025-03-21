## OpenCore-based Prebuilt EFI for specific hardware (see below)

### Hardware
<ul>
 <li>MB: GIGABYTE B550M Aorus ELITE</li>
 <li>CPU: AMD Ryzen 5 5600X</li>
 <li>GPU: XFX AMD Radeon RX 580 8GB</li>
 <li>RAM: 2x8GB Kingston FURY DDR4 3200Mhz</li>
 <li>Startup disk (NVMe SSD): Patriot M.2 P300 512GB Media</li>
</ul>

### Software
**OC Version:** 1.0.2  
**macOS versions:** 14.7.4 Sonoma, 13.5 Ventura, 12.7.6 Monterey  
**AMD Power Gadget:** Everything's working except fan control  

### Problems I've ran into
##### `IOPCIConfigurator::configure kIOPCIEnumerationWaitTime 900s`
Disable Above 4G Decoding and Resizable BAR and include npci=0x300 into boot-args.  
##### `AMDCPUSupport::Start CPUID MWait`
While installing, remove SMCAMDProcessor from your kexts. You can put it back in when you need it.  
Also, you can try repatching with AMD Vanilla patches.  

### Screenshots
<img src="https://i.imgur.com/L9bZlMu.png" style="width: 40%;"/>
<img src="https://i.imgur.com/kYl7OR9.png" style="width: 40%;"/>
<img src="https://i.imgur.com/YonI7Vz.png" style="width: 40%;"/>

### Credits
<a href="https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://discord.com/invite/EfCYAJW&ved=2ahUKEwjN9K_VrYeMAxWbUlUIHbotCDgQFnoECBgQAQ&usg=AOvVaw0ji_l0wt9qIeQFcNhgRGna">AMD OS X Discord</a> - for tech support  
<a href="https://dortania.github.io/">Dortania</a> - for OpenCore and the guides  
<a href="https://reddit.com/r/hackintosh/">r/hackintosh</a> - for moral and tech support
