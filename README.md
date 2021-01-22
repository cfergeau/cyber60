
# cyber60

A DIY-friendly 60% using nRF52840 and ZMK: the cyber.

## Status:
CAUSION, project is being tested and only an early rough ZMK-implementation is done (not in main repo, check my fork). Bugs in Rev A1, use rev A2 for MX or rev A1 for SMK/Alps if you want to give it a go. ALPS and SMK-version is done, but untested. Revision B is currently being prototyped.

## Specs cyber60:
- Module: Holyiot YJ-18010
- Standard Tray Mount support
- Non constant drain battery measurement
- Lipo charger for single cell 3.7V li-po/li-ion batteries
- RGB-led under Capslock for multi function indicator (not on SMK-version)
- Possible to build with just a soldering iron (no underside pads etc)
- Three versions running the same FW-implementation. One MX, one ALPS, one SMK.
- Underglow for cozy glow
- Buzzer for indicator or sweet tunes

## Todo:
- Verify current consumption
- Verify charge current
- Make basic ZMK config for Rev B
- Implement buzzer, RGB capslock-led and underglow in ZMK
- Update Alps and SMK-PCB's to Rev B and make releases on github

# MX-version
## Layout support cyber60 MX-version:
![alt text](./readme-images/layout_support_cyber60-mx_Rev_A2.jpg "Layout support")

## Altium view of - cyber60 MX-version:
![alt text](./readme-images/cyber60-mx_Rev_B1.jpg "PCB View - Rev B")

## MX Revisions:
- A1 - initial revision/prototype
- A2 (prerelease) - flipped PMOS-transistor, error in design. Added pulldown on enable to battery voltage measurement circuit, so it does not have to be disabled in code, only enabled. Minor silkscreen changes.
- B1 (prerelease) - Adding underglow, buzzer and rotary support. Simplifying voltage measurement circuit (tiny bit more leak current). Changing matrix to duplex.

# ALPS-version
## Layout support cyber60 ALPS-version:
![alt text](./readme-images/layout_support_cyber60-alps_Rev_A1.jpg "Layout support")

## Altium view of - cyber60 ALPS-version:
![alt text](./readme-images/cyber60-alps_Rev_A1.jpg "PCB View - Rev A")

## ALPS Revisions:
- A1 - initial revision/prototype, builds on MX rev A2

# SMK-version
## Layout support cyber60 SMK-version:
![alt text](./readme-images/layout_support_cyber60-smk_Rev_A1.jpg "Layout support")

## Altium view of - cyber60 SMK-version:
![alt text](./readme-images/cyber60-smk_Rev_A1.jpg "PCB View - Rev A")

## SMK Revisions:
- A1 - initial revision/prototype, builds on ALPS rev A1

## Note:
- Voltage measurement and power consumption for revision A1/A2 is not fully verified
- RGB-led is not implemented in ZMK yet
- Buzzer support is not implemented in ZMK yet
- B-revision is still not tested and implemented.
