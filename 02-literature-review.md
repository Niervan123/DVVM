a review of at least five relevant papers or existing vulnerable-by-design testbeds

# Literature Review

## Existing testbeds
**1. OWASP IoTGoat**
A deliberately insecure, OpenWrt-based firmware built for learning IoT hacking.
*Relevance:* closest existing "vulnerable by design" IoT project. It targets Linux-based devices, while DVVM targets a microcontroller kiosk.
https://owasp.org/www-project-internet-of-things/

**2. DVID (Damn Vulnerable IoT Device), Vulcainreo**
An open-source hardware board (ATmega328p + OLED) where each challenge is a different firmware, such as hardcoded password and UART/Bluetooth tasks.
*Relevance:* shows hands-on hardware hacking works for teaching. DVID is a standalone board, with no Wi-Fi vending scenario or reward.
DVID: https://github.com/Vulcainreo/DVID
DVID walkthrough: https://swisskyrepo.github.io/DVID


**3. OWASP Firmware Security Testing Methodology**
A stage-by-stage method for assessing firmware.
*Relevance:* guides how I will find, exploit and document DVVM's vulnerabilities.

## Research papers
**4. Costin et al., "A Large-Scale Analysis of the Security of Embedded Firmwares", USENIX Security 2014**
Analysed 32,000 firmware images and found 38 unknown vulnerabilities across 693 images.
*Relevance:* shows hardcoded credentials and similar flaws are common in real firmware (OWASP I1).

**5. Chen et al., "Towards Automated Dynamic Analysis for Linux-based Embedded Firmware" (FIRMADYNE), NDSS 2016**
Emulates Linux firmware to test it at scale, on 23,035 images from 42 vendors.
*Relevance:* shows how embedded firmware flaws are found. It covers Linux devices only, which DVVM's microcontroller is not.

**6. Antonakakis et al., "Understanding the Mirai Botnet", USENIX Security 2017**
Seven-month study of a botnet that grew to about 600,000 devices by guessing default logins.
*Relevance:* real-world cost of weak and default credentials (I1).

1. OWASP IoTGoat: https://github.com/OWASP/IoTGoat
2. DVID: https://github.com/Vulcainreo/DVID
3. OWASP Firmware Security Testing Methodology: https://github.com/scriptingxss/owasp-fstm
4. Costin et al. 2014: https://www.usenix.org/conference/usenixsecurity14/technical-sessions/presentation/costin
5. FIRMADYNE paper 2016: https://www.dcddcc.com/docs/2016_paper_firmadyne.pdf
6. Mirai paper 2017: https://www.usenix.org/system/files/conference/usenixsecurity17/sec17-antonakakis.pdf

## Gap
These sources either analyse real devices, target Linux-based firmware, or provide a standalone board. I did not find a Wi-Fi-connected, microcontroller-based vending kiosk testbed where exploiting a flaw triggers a physical reward. DVVM fills that gap and is meant to make hacking fun to learn.
