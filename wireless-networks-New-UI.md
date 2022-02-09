# Wireless networks - Updated for the 'new' UI

So you now need to create the wireless networks that the devices will connect to. I tend to have two (plus a guest network). Given that there seems to be much `magic` associated with these settings on the forum, these may not be the most optimal settings but for me, in my location with a mix of 2.4g, 5g, Wifi5 and Wifi6 clients they seem to work. Always welcome to other views that can increase throughput...


| **Setting**                     | **Main Wifi Network** | **IoT Wifi Network**      | **Description**                                                                                                                                                                                                                                                                           |   |
|---------------------------------|-----------------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| Enable                          | TRUE                  | TRUE                      | Simple on/off setting                                                                                                                                                                                                                                                                     |   |
| Name                            | YourMainWifiNetwork   | IoT                       | The name of the wifi network                                                                                                                                                                                                                                                              |   |
| Password                        | SomeComplexPassword   | ADifferentComplexPassword | The password used to connect                                                                                                                                                                                                                                                              |   |
| Network                         | Default / LAN         | IoT                       | Allows the wifi to be associated to a specific network which is what we want                                                                                                                                                                                                              |   |
| Broadcasting AP's               | All                   | All                       | You may want to limit the AP's that broadcast..                                                                                                                                                                                                                                           |   |
| Advanced Configuration          | Manual                | Manual                    | Allows manual configuration of options - generally better than auto as at least you know what is happening to your wifi!                                                                                                                                                                   |   |
| Wifi Band                       | 5Ghz                  | 2.4Ghz                    | I split mine so that all IoT devices (which normally have crappy radios) connect to 2.4Ghz and my main network uses the 5Ghz bands. Its a simple way of managing the RF channels for me, may not work for you..                                                                           |   |
| Wifi Type                       | Standard              | Standard                  | Option to have a 'Guest Hot spot' but I always tend to have my own semi-open wifi network rather than use the landing page and guest hot spot function. YMMV                                                                                                                                |   |
| Band Steering                   | Enabled               | Disabled                  | On by default for 5GHz                                                                                                                                                                                                                                                                    |   |
| Bandwidth Profile                | Default               | Default                   | Sets a bandwidth profile (limit) for this network                                                                                                                                                                                                                                         |   |
| Multicast Management            |                       |                           | As mentioned, I have a re-broadcast setup as the out of the box solution doesn't seem to work well for SONOS devices.                                                                                                                                                                     |   |
| Multicast Enhancement           | Disabled              | Disabled                  | Converts multicast to unicast                                                                                                                                                                                                                                                             |   |
| Multicast and Broadcast Control | Disabled              | Disabled                  | Only allow specific devices tp send broadcast traffic on WiFi network. Things like printers, AirPlay and Chromecast devices should be added to the list of exceptions                                                                                                                     |   |
| Client Device Isolation         | Disabled              | Disabled                  | Prevents wireless clients on the same AP from communicating with each other. This may inhibit the functionality of AirPlay, Chromecast, Sonos devices, Screen mirroring and wireless printers                                                                                             |   |
| Proxy ARP                       | Enabled               | Enabled                   | Reduces airtime usage by allowing APs to "proxy" common broadcast frames as unicast. This can improve latency but may cause connectivity issues in some networks                                                                                                                           |   |
| BSS Transition                  | Enabled               | Enabled                   | Improves client transition between AP's when the have a weak signal. Clients that do not support this feature may experience connectivity issues                                                                                                                                           |   |
| UAPSD                           | Disabled              | Disabled                  | Ensures more efficient power consumption for WiFi, VoIP and similar devices  IoT devices typically won't support this so leave it off                                                                                                                                                      |   |
| Fast Roaming                    | Disabled              | Disabled                  | You will experience connectivity issues with devices that do not support the 802.11r WiFi Standard  I've only got a couple of AP's so don't roam very often. I've seen reported that some Apple devices struggle with this when enabled so based on principle above I leave it turned off |   |
| 802.11 DTIM Period              | Auto                  | Auto                      | Misconfiguring this setting may result in client disconnections. We recommend setting this to "Auto"                                                                                                                                                                                       |   |
| Minimum Data Rate Control       | Auto                  | Auto                      | Clients incapable of meeting the minimum rates will experience network connectivity issues                                                                                                                                                                                                |   |
| Security Protocol               | WPA2                  | WPA3                      | This is the authentication protocol used when clients connect to your WifFi SSID.  Its the safest option (aka takes a bit longer to hack).                                                                                                                                                |   |
| PMF                             | Optional              | Disabled                  | Main wifi is optional to maximize compatibility, IoT really shouldn't need it..given that its pretty much an untrusted network                                                                                                                                                            |   |
| Group Rekey Interval            | Disabled              | Disabled                  | Sets how often connected device groups are assigned a new key.                                                                                                                                                                                                                           |   |
| Hide WIFi Name                  | Disabled              | Disabled                  | I hide my IoT network, not for security but to just stop people from accidentally connecting to it.                                                                                                                                                                                       |   |