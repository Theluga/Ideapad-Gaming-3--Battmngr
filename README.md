# ig3mngr
![made for ideapad Gaming 3](https://img.shields.io/badge/made%20for-ideapad-blue) ![license](https://img.shields.io/github/license/0xless/ig3mngr) 

Battery manager to handle system performance modes and charge modes through acpi_calls (for Ideapad Gaming 3 15ACH6). 


## Motivation

On Windows native software to support battery and performance operations exist, on GNU/Linux, it's possible to handle system performance modes and battery charge modes making `acpi_calls` [manually](https://wiki.archlinux.org/title/Lenovo_IdeaPad_Gaming_3#Power_management). This script makes it easy to manage such operations.

## Getting started

### Prerequisites

In order to use ig3mngr the `acpi-call` module needs to be installed.

### Installation

To install `ig3mngr` you only need to download the script, put it in a directory of your choice and then add it to your PATH.

## Usage

```
 Usage: ig3mngr [OPTION] MODE
 Options:
	-h, --help		usage help
	-s, --set		set battery mode
	-sc, --set-charge	set charge mode
 Battery modes:
	0	Intelligent Cooling
	1	Extreme Performance
	2	Battery Saving	
	
 Charge modes:
	r1	Rapid Charge On
	r0	Rapid Charge Off
	b1	Battery Conservation On
	b0	Battery Conservation Off		

 Examples:
 	ig3mngr -s 1
	ig3mngr -sc b1
	ig3mngr -s 0 -sc r0 

```
## Contributing
`ig3mngr` seem to be working fine on the supported device, but only because ACPI calls values are publicly known.

If you know any way of discovering ACPI calls values for specific laptop models, please open an issue detailing your process.
This could help supporting many more potentially compatible laptops.

## Note
Note: turning Rapid Charge will disable Battery Conservation and vice-versa.

Issuing the command `ig3mngr -sc r1` will turn on Rapid Charge mode but disable Battery Conservation mode.

## License

This project is licensed under the GPL-3.0 License.

