# DragonOS_Focal
DragonOS is the straight line between you and Software Defined Radio!
*Good to know
- Will not install from DVD, burn ISO to USB w/ Etcher etc.. 
- Before installing most GPU and WiFi drivers
   - sudo apt install dkms 
- Some USRP FPGAs have been removed to save space, but can be downloaded w/ internet using sudo uhd_images_downloader 
   - sudo uhd_images_downloader
- New ground up build on Lubuntu 22.04
- Crocodile Hunter and GsmEvil2 require python virtual environments.
   - included in /usr/src/crododilehunter/src
   - included in /usr/src/gsmevil2
   - open DragonOS_README in each directory for instructions on how to activate
- SoapySDRServer is not enabled by default, either use SoapySDRServer cli or enable.
- Run volk_profile from a terminal after install to increase GNU Radio performance
- Disable Soapy w/ SDR++ module manager before using native hackRF plugin  
- On some systems xlinrad64 seg faults (make sure you're running it with sudo). You can try to rebuild it in the directory w/ 
sudo ./configure && sudo make xlinrad64

DragonOS_FocalX_R32 (January 8 2024)
*Collection of PPA updates into a new ISO +

Updates
SatDump
HackTV
HackTV GUI
SigDigger
Spike 3.9.0
srsRAN_4G 23.04

Added
QCSuper (added back actually)

Please note that I've disabled codecserver.service by default.
If you want to use openwebrx, run the following in a terminal beforehand,
sudo systemctl enable codecserver.service
sudo systemctl start code server.service

--------------------------------------------
DragonOS_FocalX_R31 (August 24 2023)
*Collection of updates into a new ISO

Updates
22.40.3 w/ 6.2 Kernel
LimeSuite
GR-Lora_SDR
GR-LimeSDR
Iridium Toolkit w/ Airframes IO tweak
RTLSDR drivers (supporting v4 dongle)
WhisperCPP
Scat
SDRTrunk v0.6.0 beta1
Spike 3.8.11
SDR++
SatDump
SDRAngel 7.15.3
Kismet 2023-07-R1
QradioLink
SDR4space + Examples 
SigDigger

Added
PortaPack Mayhem firmware v 1.7.4 located in /usr/src/firmware/mayhem 
GR-SigMF

-------------------------------------------------------------------
DragonOS_FocalX_R30.2 (May 2 2023)
*Additional installer fixes and collection of updates into a new ISO

Updates
Manual update of WhisperCPP
5.19.0-41 Kernel

Added
LTESniffer

------------------------------------------------------------------
DragonOS_FocalX_R30.1 (April 20 2023)
*Fixed the installer for legacy installs

------------------------------------------------------------------
DragonOS_FocalX_R30 (April 16 2023)
*Collection of updates into a new ISO

Updates
Apt package updates to include 5.19 kernel
FocalX PPA updates (https://github.com/alphafox02/focalx_ppa)
Manual update of SigDigger using /usr/src/blsd
Manual update of SDRTrunk v0.6.0 Alpha 5 /usr/src/
LibUHD modification for additional ANTSDR hardware

Fixed
Logrotate error

-------------------------------------------------------------------
DragonOS_FocalX_R29.1 (February 25 2023)
*Mainly meant to fix the installer, other packages can be manually 
updated/added

Fixed
Installer 

Updated
SDRangel w/ heat map v7.10
SDR++ 1.1.0-942
SatDump
SDRTrunk v0.6.0-alpha3 w/ SDRPlay

Added 
RF-Tools
Kismet MetaGPSD (replaces KisStatic2Mobile)

---------------------------------------
DragonOS_FocalX_R29 (February 19 2023)

Fixed
Mariadb will now run on live boot
OsmocomBB, CalypsoBTS, and AutoCalypsoBTS 
SoapyRTLSDR
  
Added 
Modmobmap (run installer in /usr/src/Modmobmap if android tools are needed)
BladeRF 122Msps Support (/usr)
Osmo-GMR (utils still need updated for GR 3.10)
E200 SDR support to UHD (/usr)
GR-Smart_Meters
GR-Fhss-utils
GR-Sandia-utils
GR-Timing-Utils
GR-PDU
OpenBTS 
TempestSDR
Ice9-bluetooth-sniffer (call from terminal w/ ice9-bluetooth)

Updated
GR-GSM to Multi ARFCN branch
Spike Signal Hound 3.8.9
GR-BladeRF w/ 122Msps Support 
SDR4Space 20230126
Hackrf-2023.01.1 (firmware is in /usr/src/firmware)
Kernel 5.15.0.58
Dsd-fme
Kismet
Hak5-wifi-coconut
SDRTrunk v0.5.0 Final
SatDump w/ Immarsat + BladeRF 122Msps 
SDRAngel 7.9.0
SDR++ 1.1.0-903
M17-Tools
Mirage
SigDigger
BoatBod OP25 (3.10 branch)
HackTV-GUI 2023-01-15
GR-Mixalot
Fldigi-4.1.23
WhisperCPP (remember to sudo make clean && sudo make for optimization after install)
SigDigger

Removed 
dkms (reinstall as needed, however, be aware it'll install gcc12 to)


---------------------------------------
DragonOS_FocalX_R28 (December 23 2022)

Added
Dragon Spectrum Awareness Manager
LimeGPS (usr/src/LimeGPS)
DSD-FME
qFlipper 1.2.2+
qFlipper-cli 1.2.2+
SDR4Space Whispercpp script
Whispercpp w/ tiny model
Pyrtlsdr
WXtoIMg 2.11.2 w/ updated weather.txt
CSDR
CalibrateSDR 
MiniModem 0.24
Redsea 0.21 https://github.com/windytan/redsea
Astro-virgo https://virgo.readthedocs.io/en/latest/
Multi-sdr-gps-sim
Gps-sdr-sim
PlutoGNSS 
Welle.io 2.2
RTLSDR-Airband 4.0.2
TRXCON (/usr/src/Osmocom-BB/Bin)
ProbeQuest
JSquelch
GeoServer
Osmo-fl2k
    fl2k_signal_generator
    fl2k_spif
    Noise-generator
    Fl2k-tool
    Ampliphase-fl2k
Spectrum_painter
M17-tools (replaced m17-cxx-demod)
GR-AISTX w/ AIS toolkit
GR-AIS_Simulator w/ AIS-Simulator
RTL-SDR-Scanner-CPP (auto-sdr binary)


Updated
Kernel 5.15.0-56
Spike 3.8.8 (Signal Hound) 
SDR++
SDRTrunk 0.5.0-beta6
SDRAngel 7.8.5
NOAA-APT 1.4.0
SatDump 1.4.0
SigDigger
QradioLink
DF-Aggregator
JAERO 1.0.4.14
Tetra-Kit


Fixed
Grgsm_tx
Osmo-NITB-Scripts w/ UHD (start Osmo-trx-uhd separately)
Gr-LimeSDR
SDRPP LimeSDR plugin built against newer LimeSuite, look in /usr/src/firmware for backup


------------------------------------------
DragonOS_FocalX_R27.1 (November 14 2022)

*If you do not want to reinstall, install the files here 
https://drive.google.com/drive/u/1/folders/1C3bdv-vuzfEBAO_jtDkHI5K_tIpBI9SI
and unzip apt.zip in the /etc/ directory (only if you're missing it and copy 
grgsm_decode to /usr/local/bin/


Added
Sometimes missing /etc/apt directory after install
grgsm_decode 

Updated
Dumphfdl 1.4.0


-----------------------------------------
DragonOS_FocalX_R27 (November 12 2022)
 
Installed:

ACARS Decoder
Aircrack-NG
Airspy ADSB
Apache2
Asterisk
AutoCalypsoBTS
Blue-hydra
BlueWho
BoatBod OP25
BTLE (hackRF + bladeRF)
Bully 1.4
CalypsoBTS
CBandHunter (/usr/src/gr-JAERO)
Cesium 1.95
Chirp
CleverJam
DF Aggregator
dumpHFDL
dumpVDL2
ESPTool
FALCON LTE Tool
Flrig 1.4.7
Gnome-Firmware 41.0.1
GNU Radio 3.10.4
Gpredict
GQRX 2.15.9
GQRX Scanner
GR-AOA
GR-BB60 (Signal Hound)
GR-bladeRF
GR-Dect2
GR-DJI_DroneID
GR-DSD
GR-Foo
GR-Fosphor (benchmark tool gr-fosphor/lib/fosphor)
GR-Funcube
GR-GSM
GR-IEEE802-11
GR-IEEE802-15-4
GR-Inspector
GR-Iridium
GR-JAERO
GR-Lora_SDR
GR-Mixalot
GR-NRSC5
GR-NTSC-RC
GR-Osmosdr/IQBal
GR-Paint
GR-RDS
GR-RFTap
GR-Satellites
GR-SDRPlay3
GR-SM (Signal Hound)
GR-VSG60 (Signal Hound)
GridTracker v1.22.1016
GSMEvil2
hackRF 2022.09.1 libraries w/ shortcut to 2022.09.1 firmware
hackRF-Spectrum-Analyzer
HackTV w/ GUI
Ham2Mon (usr/src)
Hashcat 6.2.5.7
Hcxdumptool
Hcxtools
IMSI Catcher Script
Inotify-Tools 3.22.6
Inspectrum
Iridium-ToolKit
Iridium-ToolKit-Airframesio
JAERO 1.1-de-11 (feeder ability)
Js8call
JTDX
Kalibrate-hackRF v0.4.1 (kal-hackrf)
Kalibrate-RTL v0.4.1 (kal)
Kismet
Kismet Rest API
Kismon
kisStatic2Mobile
Larry Tetra Kit
Libbtbb
libhackRF 2022
Libre Office Writer/Calc
LimeSuite/Firmware 2022 w/ Lime v2 support
Linrad 05.01 w/ SDRPlay support (xlinrad in /usr/src/linrad)
LinSSID
LTE Cell Scanner (hackRF + rtlsdr)
LuaRadio 0.10.0
M17-cxx-demo (/usr/src)
M17-Gnuradio
Macchanger 1.7
Meshtastic 1.3.40
Modem-Manager-GUI 0.20.3
Multimon-NG 1.1.9
Netcat
Nmap
NOAA APT 1.3.1
NRSC5
NRSC5-GUI
Octave
Octave-Signal
OpenWebRX 1.2.1 (M17/DMR)
Osmo-NITB
Osmo-NITB-Scripts
Osmo-NITB-Scripts (CalypsoBTS)
PAT 0.12.1
Photon Map
Pixiewps 1.4.2
PulseView
Pyadi_iio
Qalculate
QCSuper
QRadioLink
Qspectrumanalyzer
QSSTV 9.5.8
Qstdcdec (QT GUI Inmarsat-C Parser)
Radio_tool 0.2.1
Reaver 1.6.5
ReconToCrack
Retrogram-PlutoSDR
Retrogram-RTLSDR
Retrogram-SoapySDR
RFCat
RFHack
RSPTCP Server (SDRPlay)
RT_433 v21.12-159
RX_Tools
SatDump w/ SDR++ source
SCAT
SDR++ 1.1.0-821 w/ Inmarsat-C and USRP plug-in
SDR4Space
SDRAngel 7.8.2-1
SDRReceiver 1.0
SDRTrunk v0.5.0 beta 5
SigDigger (October 11)
Signal Server 3.21
Signal Server GUI
Sigrok 0.2-5
SoapyAirspy (AST developed Fork)
SoapyAirspyHF
SoapyBladeRF
SoapyHackRF
SoapyLime
SoapyMiri
SoapyOsmosdr
SoapyPlutoSDR
SoapyRedpitaya
SoapyRemote
SoapyRfspace
SoapyRtlsdr
SoapySDRPlayV3
SoapyUHD
SoapyVOLKConverters
Sox 14.4.2
Sparrow-WiFi
Spike (Signal Hound) 3.8.3
SpyServer
srsGUI
srsRAN 22.4.1
Stdcdec (Command line Inmarsat-C Parser)
StillSuit
STRF
Tetra-Kit-Player in /usr/src (needs configured/npm installed)
Tshark
Ubertooth
WFView 1.52
Wifi Coconut
Wifite 2.6.0
WireGuard Tools 1.0.2
WireShark 3.6.2
Wpapcap2john
Yate rc3
