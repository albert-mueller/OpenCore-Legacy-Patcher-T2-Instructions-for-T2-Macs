# OpenCore-Legacy-Patcher-T2-Instructions-for-T2-Macs
** To be able to boot OpenCore, you'll need to disable Secure Boot and System Integrity Protection on T2 Macs. Why disable? Because, T2 Macs don't trust OpenCore, and Secure Boot blocks OpenCore. And SIP being disabled is absolutely required to boot the installation media too. If T2 Macs were trusting any boot manager, they could trust a malicious boot manager, which is a high security risk.

These instructions are for T2 Macs only. These instructions don't apply to non-T2 Macs.
1. Once you reach Reboot to apply:
<img width="372" height="482" alt="image" src="https://github.com/user-attachments/assets/6eda34be-65a4-454d-b904-9c3217db5d66" />
2. Click on Reboot

3. Click on Neu starten / Restart
<img width="563" height="286" alt="image" src="https://github.com/user-attachments/assets/696ac25f-5ae9-4cfb-bbdb-1e226b0fd15a" />
4. Once the screen becomes black, prepare your fingers to hold command-R
5. Once you hear the chime, immediately hold command-R until you see a progress bar
<img width="2100" height="1576" alt="IMG_0213" src="https://github.com/user-attachments/assets/34f34e38-e8e2-4578-82b2-199485eaae2a" />
6. Now that you've successfully booted into your native OS's macOS Recovery, go to Dienstprogramme / Utilities
<img width="2100" height="1576" alt="IMG_0215" src="https://github.com/user-attachments/assets/e3cb7b3c-b4eb-438b-91f4-21484ad02a0e" />
7. Go to Startsicherheitsprogramm / Startup Security Utilitiy
<img width="2100" height="1576" alt="IMG_0216" src="https://github.com/user-attachments/assets/5036d4c5-8ca1-4008-a2c6-8dbb387c94b7" />
8. Authentifizierung erfoderlich / Authentication required - Click on macOS-Passwort eingeben / Enter macOS password
<img width="2100" height="1576" alt="IMG_0217" src="https://github.com/user-attachments/assets/d5d02623-4ee6-42e7-9a07-84528ebdbde8" />
9. Set Secure Boot to Ohne Sicherheit / No Security and Allowed boot media (Erlaubte Boot-Medien) to Starten von externen oder Wechselmedien erlauben / Allow startup from external bootable media
<img width="2100" height="1576" alt="IMG_0218" src="https://github.com/user-attachments/assets/4c88f484-e345-412d-8315-65c43eb0e45b" />
10. Close this window
<img width="2100" height="1576" alt="IMG_0218" src="https://github.com/user-attachments/assets/7609949e-608d-4a00-80f9-ff13cfc3500a" />
11. Go to Dienstprogramme / Utilities > Terminal
<img width="2100" height="1576" alt="IMG_0218" src="https://github.com/user-attachments/assets/3016daca-f94d-41df-9380-04411a10320a" />
12. Type csrutil disable && csrutil authenticated-root disable && csruitil authenticated-boot disable
<img width="5712" height="4284" alt="IMG_0239" src="https://github.com/user-attachments/assets/82ff1341-ea15-478b-ba9a-008cf7b9094b" />

13. Click on Apple Logo > Restart

14. Hold option key

15. Choose EFI boot
<img width="2100" height="1576" alt="IMG_0221" src="https://github.com/user-attachments/assets/1ad19aed-6b1e-4174-87c5-13db0dc02f40" />
16. Select Install macOS Tahoe or the version of your choice
<img width="2100" height="1576" alt="IMG_0222" src="https://github.com/user-attachments/assets/dded1c8d-f7c4-4d5d-947f-4025535ff5d3" />

If you see a kernel panic or stall at the Apple logo, you should definately report what kernel panic appears or the stall here: https://github.com/albert-mueller/OpenCore-Legacy-Patcher-T2/issues 


