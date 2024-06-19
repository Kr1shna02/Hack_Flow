## Footprinting 
  + Whois lookup
  + Explitdb
  + FCC ID search - https://www.fcc.gov/oet/ea/fccid
  + IOTSeeker tool to scan for iot devices with default passwords - https://github.com/rapid7/IoTSeeker
  + Shodan
    + Search for port : 1883 which is commonly usesd of MQTT iot communication protocal.

      ![1](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/cde7fb0a-e23f-42f4-8f72-30eeb14318cc)
      
    + Now we get the IP address of all the devices with 1883 port and we can get the detailed info.

      ![2](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/99ca6ecd-4ab4-481f-8e40-5f2e005beae5)

    + Use advanced Shodan queries to search - https://www.shodan.io/search/examples
    + OT Information gathering
      + SearchDiggity -  https://bishopfox.com 
    ### OT control system

       ![1](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/87df6853-f298-4872-98c4-ddf3e309036f)

## Vulnerability scanning
 
  + Analyzing IoT Traffic using IoT Inspector - https://www.iot-inspector.com
  + Vulnerability Scanning using Retina IoT (RIoT) Scanner - https://www.beyondtrust.com
  + Wireshark
  + OT Vulnerability scanning using nessus

## Attacks
  
  + Rolling-code attack using RFCrack
  + Hacking Zigbee Devices with Attify Zigbee Framework - https://www.attify.com
  + HackRF One - https://greatscottgadgets.com
    + Hardware and software based tool
    + Attacks- Replay, sniffing , jamming signals.
  + Side-Channel Attack using ChipWhisperer - https://newae.com
  + IoTVAS Fireware analysis tool - https://firmalyzer.com
  + ICS Exploitation Framework (ISF) - https://github.com/dark-lbp/isf
