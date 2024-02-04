# Skyhawkson-KiCAD-Libraries

This is a library of KiCAD 6/7/+ components and supporting documentation that I use in my personal projects. I'm making it publically available in the hopes that the contents within prove a useful starting point for others in the hobby/high-power rocketry community, especially the folks of the BPS.Space Discord.

**NOTE**: This library is intended to be a library of *physical components* not just mix-and-match symbols and footprints as in stock KiCAD. It loosely mimics an Altium-esque library philosophy, intended to prevent invalid symbol/footprint combinations from ever reaching the ordering phase. As such, all items have a Digikey part number, to assist in BoM creation and ordering. You are welcome to fork and modify to suit your individual needs/vendor of choice as you like.

All items included here are subject to change/my own hubris. While I strive to make them as correctly as possible, use your own best judgement and please flag an issue ticket if something doesn't seem right. You are welcome and encouraged to use symbols/footprints/models independently in your own libraries as a way to accelerate your own designs.

## Symbols

<img width="1447" alt="KiCad_Symbols_Screenshot" src="https://github.com/Skyhawkson/Skyhawkson-KiCAD-Libraries/assets/32376505/d291c78f-a201-45f6-bb3a-d0342b447156">

Symbols in this library represent a single physical part, and therefore contain more information than the name of the device. They include a manufacturer prefix, and data per the YJSP Component Naming Preferences PDF in /Reference Documents. Adding a symbol to your schematic should automatically include the matching footprint and DKPN, and therefore be immediately importable to a PCB and indexable in a BoM. I encourage the use of the [Interactive HTML BOM](https://github.com/openscopeproject/InteractiveHtmlBom) plugin for ordering and placing parts.

## Footprints

<img width="1600" alt="KiCad_Footprints_Screenshot" src="https://github.com/Skyhawkson/Skyhawkson-KiCAD-Libraries/assets/32376505/647d86c1-5b2f-4701-a476-2e891a6a2edf">

Footprints in this library are intended to follow the manufacturer's recommendation as closely as possible, or my best judgement based on experience/IPC standards if a manufacturer footprint isn't available. Please raise an issue if you experience problems with manufacturing; this is a living library and I update it to fix bugs as I build additional boards. 

Footprints marked 'GENERIC_' are for such common 'jellybean' parts that making a new footprint for them all is infeasable and unnecessary, such as 0805/0603/0402 passives.

## Models

Models included in the /Models folder are based on the following sources:
- Manufacturer Supplied Models
- Models modified from [SnapEDA](https://www.snapeda.com/about/terms/)
- Models hand-made by myself in Solidworks

All models are .STEP AP214 with appearances enabled.

## Supporting Documentation

Included in the /Reference Documents folder are a few pieces of information included to help new designers select parts, manage a library, and create or modify components to suit their needs. They are not the be-all, end-all of electronic design, but a starting point for new folks in the hobby/high-power rocketry space. Some highlights include:

### YJSP Derating Guide
Created as part of the early stages of a space-shot avionics program, this document adds quick derating standards for designers looking to make more robust boards. This document is more comprehensive than NASA's [PD-ED-1201], but significantly less verbose than [EEE-INST-002] (300+ pages!). Take it with a grain of salt and always use your best judgement as a designer, but I hope it proves a useful quick entry into derating parts.


### YJSP Component Naming Conventions
A companion to the derating guide, this document describes what our team felt were the most important characteristics of a variety of parts, to be included with every component library entry.

### Component Manufacturer Prefixes
Describes prefixes used on parts to shorten certain manufacturer names.

### Calculating Hole Size and Plating (from [pcb-3d.com])
The easiest answer I've ever found to 'what size should I make my pads'. Reproduced here in case that website ever goes dark.


[PD-ED-1201]: https://extapps.ksc.nasa.gov/Reliability/Documents/Preferred_Practices/1201.pdf
[EEE-INST-002]: https://nepp.nasa.gov/docuploads/FFB52B88-36AE-4378-A05B2C084B5EE2CC/EEE-INST-002_add1.pdf
[pcb-3d.com]: https://www.pcb-3d.com/wordpress/tutorials/how-to-calculate-pth-hole-and-pad-diameter-sizes-according-to-ipc-7251-ipc-2222-and-ipc-2221-standards/
