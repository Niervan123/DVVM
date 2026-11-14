DVVM
damn vulnerable vending machine 

# DVVM: Damn Vulnerable Vending Machine

## Problem
Few students get to hack real hardware. hands on labs are linux based networking , owasp , dvwa, so it stays something we cant "see" 
,and campus has little hacking culture.

## Idea
A vending machine that rewards you with a snack when you hack it. DVVM is a mock kiosk on an ESP32 with 4-5 deliberate vulnerabilities, 
so breaking in is the fun part.

## Vulnerabilities (OWASP IoT Top 10)

1. Hardcoded admin password          (I1):      the admin password is written inside the firmware, so anyone who extracts it or guesses it gets full control.
2. Unauthenticated dispense endpoint (I2):      the machine dispenses when you simply visit its dispense URL, with no login or payment check.
3. Cleartext, replayable commands    (I7):      commands travel unencrypted over Wi-Fi, so you can sniff one and replay it for free snacks.
4. Exposed UART debug console        (I10):     plug a cable into the debug pins and you get a shell on the device.
5. Unsigned firmware update (I4),stretch goal:  the machine accepts any firmware you upload, including a hacked one.

The “I” stands for IoT, and the number is the category’s position in the list (I1 is first, I10 is tenth). They don’t rank how serious something is, they’re just labels.

Here are the ones you use:

I1 = Weak, Guessable, or Hardcoded Passwords
I2 = Insecure Network Services
I4 = Lack of Secure Update Mechanism
I7 = Insecure Data Transfer and Storage
I10 = Lack of Physical Hardening

## Outcome
Working kiosk, exploit write-ups, fixed version, demo video. Due 20 Dec 2026.

## Out of scope
Real payments and campus rollout. The QR portal, college login and HackerRank link are future work.
