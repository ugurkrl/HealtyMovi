# eMMC Health Reader
This simple program can read "vendor proprietary" health reports.
Requires native mmc interface (eg : /dev/mmcblkx ; NOT /dev/sdx)
Compilation : gcc smart.c -o smart

# Supported & Tested Devices : 

| Vendor | Family | eMMC Version | IC Model |
| - | - | - | - |
| SAMSUNG* | MoviNAND® 4.3 | 4.3 | KLM4G1EEHM-B101 |
| SAMSUNG* | MoviNAND® 4.3 | 4.3 | KLM8G4DEHE |
| SAMSUNG* | MoviNAND® 4.41 | 4.41 | KLM8G2FE3B |
| SAMSUNG* | MoviNAND® 4.41 | 4.41 | KLM8G2YE4C |
| SAMSUNG* | MoviNAND® 4.41 | 4.41 | KMSJS000KA |
| SAMSUNG* | MoviNAND® 4.5 | 4.5 | KMVTU000LM |
| SanDisk | iNAND® 7232 | 5.1 | SDINADF4-XXG |
| Western Digital | iNAND® EM111 | 5.1 | SDINADF4-XXG |


# Not Working Devices : 

| Vendor | Family | eMMC Version | IC Model |
| - | - | - | - |
| SAMSUNG* | MoviNAND® 4.5 | 4.5 | KLMAG2GEAC-B001 |
| SAMSUNG* | MoviNAND® 5.0 | 5.0 | KLMAG2GEAC-B031** |


1* : Do Not Run Code If OS Runs From SAMSUNG eMMC . Sometimes eMMC can't exit from report mode. System will hang.  
2* : Same model eMMC but 5.0 Version. Supports EXT_CSD Life report but still no MoviNAND S.M.A.R.T Report
