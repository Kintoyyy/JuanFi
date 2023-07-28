# **JuanFi**
- ## Official Website: [juanfi.juansystems.com](https://juanfi.juansystems.com/)



JuanFi is an innovative open-source system designed for seamless coinslot integration with MikroTik Hotspot. It provides a comprehensive solution for managing and monetizing internet access through the integration of a coinslot mechanism. With JuanFi, hotspot owners can effortlessly incorporate a coinslot system into their network infrastructure, enabling them to offer paid internet access in an efficient and user-friendly manner.

## **Donation**

We greatly appreciate donations as they help support the development and maintenance of JuanFi. If you wish to contribute and show your support, you can make a donation using the following methods:

- Gcash account: Ivan Julius Alayan - 09175425572
- PayPal account: [paypal.me/ivanalayan](https://www.paypal.com/paypalme/ivanalayan)

# **Community Group**

Join our vibrant community group to connect with other users and contributors. Share your experiences, exchange ideas, hotspot portals, and stay up to date with the latest developments and enhancements of JuanFi.

- Facebook Group: [JuanFi Community](https://www.facebook.com/groups/1172413279934139)

# **Features**

 ### Hardware Option

- Wireless based
- Lan based

### Coinslot System

- Mikrotik integration
- Pause expiration
- Codeless generation
- Anti Coinslot abuse system
- LCD Display
- Code generation in vendo using LCD without device needed
- Multi vendo system

### Admin System

- Initial setup of the system
- Mikrotik connection setup, SSID setup, coinslot settings
- Promo Rates configuration ( Rates, expiration)
- Dashboard, Sales report
- Custom pin configuration
- coinslot abuse system config

## Requirements

1.) NodeMCU(ESP8266) for wireless/lan or NodemCU(ESP32) for wireless/lan

2.) Coinslot

3.) Mikrotik Router

4.) Access Point

5.) Node MCU baseboard( Optional for wireless)

6.) Power Supply (12v for nodemcu, another 12v for Mikrotik)

7.) W5500 for Lan based

8.) LM2596 or any DC to DC buck that can convert to 5v for (Lan based only since no available baseboard for ESP32)


---
# **Architecture** 


![alt text](docs/JuanFi-Architecture.PNG?raw=true)

---

## ESP32 LAN Based Connection Diagram

![alt text](/docs/esp32-lan-diagram.jpg)

## ESP32 Wireless Based Connection Diagram

![alt text](/docs/esp32-wireless-diagram.jpg)

## ESP8622 Wireless Based Connection Diagram

![alt text](/docs/esp8622-wireles-diagram.jpg)

## ESP8622 LAN Based Connection Diagram

![alt text](/docs/esp8622-lan-diagram.jpg)



# **Installation**

## **ESP32** 

<details>
<summary>ESP32 Flashing Instructions</summary>

---

**esptool.exe** is being use for flashing the esp32 hardware, to flash simply download all the contents

<br>

## **1. Download the esp32 Flashing folder**

- ## [**ESP32 Wirelesss Base folder**](/release/WirelessBase/ESP32/)

- ## [**ESP32 Lan Base folder**](/release/LanBased/ESP32/)

<br>

---


## **2. Double click start_flash.bat**
*Connect the esp32 to the pc*


![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-Lan-FlashFile1.PNG?raw=true)

*Once done, a command propmt screen will appear to let you select available com port for your esp32 device*

![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-Lan-FlashFile2.PNG?raw=true)

<br>

---

## **3. Select Port**

E.G. COM9 and press enter

![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-Lan-FlashFile3.PNG?raw=true)

*you will notice that a connecting message will prompt and it will be ALWAYS connecting if you not do any press button on the flash button*

![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-Lan-FlashFile4.PNG?raw=true)

*Press and hold this button arround 3 - 5 secs until the flash starts*

<br>

---

## **4. Wait for the flash process to finish** 

![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-Lan-FlashFile5.PNG?raw=true)

<br>

---

## **5. Done!**
*and thats it. you can now use your esp32 and begin the Juanfi Setup*
</details>

<br>


## **ESP8622** 

<details>
<summary>ESP8622 Flashing Instructions</summary>

 
<br>

*I had forked a the pyflasher repository [marcelstoer/nodemcu-pyflasher](https://github.com/marcelstoer/nodemcu-pyflasher) and make a custom changes for the custom flasher required for SPIFFS flashing, if your interested here is the repository [ivanalayan15/nodemcu-pyflasher](https://github.com/ivanalayan15/nodemcu-pyflasher)*

<br>

## **1. Download the esp8266 Flashing folder**

- ## [**ESP8622 Wirelesss Base folder**](/release/WirelessBase/ES8622)

- ## [**ESP8622 Lan Base folder**](/release/LanBased/ESP8622/)
  
<br>

---


## **2. Open the NodeMCU-PyFlasher.exe**

*Connect the esp8266 to the pc*

<br>

---

## **3. Flashing the JuanFi-FlashFile1.bin**


- select the file **JuanFi-FlashFile1.bin**
- make sure the offset is **0x000000**
- click **Flash Nodemcu** and wait to complete

![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-FlashFile1.PNG?raw=true)

<br>

---

## **4. Flashing the JuanFi-FlashFile2.bin**


- select the file **JuanFi-FlashFile2.bin**
- make sure the offset is **0x200000**
- click **Flash Nodemcu** and wait to complete


![alt text](https://github.com/ivanalayan15/JuanFi/blob/master/docs/JuanFi-FlashFile2.PNG?raw=true)

<br>

---

## **5. Done!**

### Restart the NodeMCU and begin the setup


</details>

<br>

## **JuanFi Setup**

## **6. Connect to JuanFi Setup**

- ### **For Esp32/Esp8622 Wireless Based** ***"JuanFI Setup"*** will appear

![alt text](/docs/JuanFi-Step01.PNG)

- ### **For Esp32/Esp8622 LanBase** you need to plugin first in your PC/Laptop ethernet

    - Set your device IP address as static **172.217.28.2**

		```
		IP address: 172.217.28.2
		Subnet Mask: 255.255.255.0
		Gateway: 172.217.28.1
		Dns: 172.217.28.1
		```

	- After you set to static you can access the admin in your browser as **[172.217.28.1/login](http://172.217.28.1/login)**

<br>

---

## **7. Login to admin panel**
Default user and password : **admin** / **admin**

![alt text](/docs/JuanFi-Step02.PNG)

## **8. Configure System**
Change the necessary fields to your configuration, system will restart to take effect,
default mikrotik user and password is pisonet / abc123
![alt text](/docs/JuanFi-Step03.PNG?raw=true)

### **Configure Promo rates**
![alt text](/docs/JuanFi-Step04.PNG?raw=true)

<br>

# **Mikrotik Setup**

## **1. Setup mikrotik hotspot according to your configuration**

<br>

## **2.Make the NodeMCU IP address static**
![alt text](/docs/JuanFI-Mikrotik-Step1.PNG?raw=true)

<br>

---

## **3. Add IP Bindings exception on hotspot**
![alt text](/docs/JuanFi-Mikrotik-Step2.PNG?raw=true)

<br>

---

## **4. Modify vendoIpAddress (NodeMcu IPaddress) in the [config.js](/mikrotik-template/assets/js/config.js) file**
 you can do a multivendo setup just follow the comment in javascript for instruction
![alt text](/docs/JuanFi-Mikrotik-Step5.PNG?raw=true)

<br>

---

## **5. Upload [html template](/mikrotik-template/) to mikrotik in Files option of mikrotik**

<br>

---

## **6. Create user for nodemcu access**
 default user for nodemcu is **pisonet** / **abc123** you can change it by your own
![alt text](/docs/JuanFi-Mikrotik-Step3.PNG?raw=true)

<br>

---

## **7. Execute the following script in mikrotik telnet terminal**
replace **10.0.10.253** with your own nodemcu IP address

```bash
/ip hotspot walled-garden ip add action=accept disabled=no dst-address=10.0.10.253
/ip firewall filter add action=accept chain=input place-before=0 comment=NodeMCUIP src-address=10.0.10.253
```

<br>

---

## **8.) Please add this script in the hotspot user profile on login event** (credits to kristoff for adding sales)

Execute on mirkotik terminal

```bash
/system scheduler add interval=1d name="Reset Daily Income" on-event="/system script set source=\"0\" todayincome " policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon start-date=Sep/28/2021 start-time=00:00:00;
/system scheduler add interval=30d name="Reset Monthly Income" on-event="/system script set source=\"0\" monthlyincome " policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon start-date=Sep/28/2021 start-time=00:00:00;
/system script add dont-require-permissions=no name=todayincome owner=admin policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source="0";
/system script add dont-require-permissions=no name= monthlyincome owner=admin policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source="0";
```

Put on the on login script (with telegram support) please change accordinly with your hotspot folder(hex or haplite)

```bash
### enable telegram notification, change from 0 to 1 if you want to enable telegram
:local isTelegram 0;
###replace telegram token
:local iTBotToken "xxxxxxxxxx:xxxxxxxxxxxxx-xxxxxxxxxxxxxxx-xxxxx";
###replace telegram chat id / group id
:local iTGrChatID "xxxxxxxxxxxxxx";
### hotspot folder for HEX put flash/hotspot for haplite put hotspot only
:local HSFilePath "flash/hotspot";
if ([file find name="hotspot"]!="") do={ set HSFilePath "hotspot" }
### enable Random MAC synchronizer
:local isRandomMacSyncFix 0;

### enable JuanFi online monitoring 0 = DoNotSend,  1=send data to api
:local apiSend 0;
### derive from the JuanFi online monitoring, create account in genman.projectdorsu.com
:local URLvendoID 5;

# Get User Data
:local aUsrNote [/ip hotspot user get $user comment];
:local aUsrNote [:toarray $aUsrNote];
:local iUsrTime [:totime ($aUsrNote->0)];
:local iSaleAmt [:tonum ($aUsrNote->1)];
:local iExtCode ($aUsrNote->2);
:local iVdoName ($aUsrNote->3);
:local iTimeMin [/ip hotspot user get $user limit-uptime];
:local iUserReg [/system scheduler find name=$user];

# Check User Data
:if (($iTimeMin>0) and ($iUsrTime>=0) and (($iUserReg="") or ($iExtCode=1))) do={
  /ip hotspot user set $user comment="";
  :local iFileMac;
  :local mac $"mac-address";
  :for i from=0 to=([:len $mac] - 1) do={
    :local chr [:pick $mac $i]
    :if ($chr = ":") do={ :set $chr "" }
    :set iFileMac ($iFileMac . $chr)
  }
# api tracking
  { /do {
  :local URLamount "$iSaleAmt";
  :local URLcomment "ScriptOnLoginFINAL";
  :local URLip [:put [:tostr $address]];
  :local URLusr [$user];
  :local URLmac [$"mac-address"];
  :local URLipmac "$URLusr_$URLip_$URLmac";
  :local URLactive [/ip hotspot active print count-only];
  :if ($apiSend!=0)  do={
  /do {
  :local fixUrl [("https://juanfiapi.projectdorsu.com/serve.js\?s=stats&i=OE-IBX-12345&m=direct&payload=$URLvendoID")];
  :local apiUrl "$fixUrl_$URLamount_$URLipmac_$URLactive_$URLcomment";
  :log debug "API SendInfo: $apiUrl ";
  /tool fetch mode=https http-method=get url=$apiUrl keep-result=no
  :delay 1s;
  } on-error={:log error "API Vendo ERROR: $apiUrl ";} }
  } on-error={:log error "APIvendoRoutineError";} }
# Extend User
  :if (($iUserReg!="") and ($iExtCode=1)) do={
    :local iTimeInt [/system scheduler get $user interval];
    :set iTimeInt ($iTimeInt+$iUsrTime);
    :if ($iTimeMin>$iTimeInt) do={ :set iTimeInt ($iTimeMin+$iUsrTime) };
    /system scheduler set $user interval=$iTimeInt;
  }
# ADD User
  :local iDateBeg [/system clock get date];
  :local iTimeBeg [/system clock get time];
  :if ($iUserReg="") do={
    :local iTimeInt $iUsrTime;
    :if ($iTimeMin>$iUsrTime) do={ :set iTimeInt ($iTimeMin+$iUsrTime) };
    :do { /system scheduler add name="$user" interval=$iTimeInt \
      start-date=$iDateBeg start-time=$iTimeBeg disable=no \
      policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
      on-event=("/ip hotspot user remove [find name=$user];\r\n".\
                "/ip hotspot active remove [find user=$user];\r\n".\
                "/ip hotspot cookie remove [find user=$user];\r\n".\
                "/system scheduler remove [find name=$user];\r\n".\
                ":do {/file remove \"$HSFilePath/data/$iFileMac.txt\"} on-error={};\r\n")
    } on-error={ log error "( $user ) /system scheduler add => ERROR ADD!" };
    :local x 10;:while (($x>0) and ([/system scheduler find name="$user"]="")) do={:set x ($x-1);:delay 1s};
  };
# Save Data File
  :if ([/file find name="$HSFilePath/data"]="") do={
    :do {/tool fetch dst-path=("$HSFilePath/data/.") url="https://127.0.0.1/"} on-error={ };
  }
  :local iValidUntil [/system scheduler get $user next-run];
  :if ([/system scheduler find name=$user]!="") do={
    /file print file="$HSFilePath/data/$iFileMac.txt" where name="dummyfile";
    :local x 10;:while (($x>0) and ([/file find name="$HSFilePath/data/$iFileMac.txt"]="")) do={:set x ($x-1);:delay 1s};
    /file set "$HSFilePath/data/$iFileMac" contents="$user#$iValidUntil";
  }
# Update Today Income
  :local iSaveAmt [:tonum [/system script get todayincome source]];
  :local iDailySales ($iSaleAmt + $iSaveAmt);
  /system script set todayincome source="$iDailySales";
# Update Monthly Income
  :local iSaveAmt [:tonum [/system script get monthlyincome source]];
  :local iMonthSales ( $iSaleAmt + $iSaveAmt );
  /system script set monthlyincome source="$iMonthSales";
# Telegram
  :if ($isTelegram=1) do={
    :local xVendo;
    :for i from=0 to=([:len $iVdoName] - 1) do={
      :local chr [:pick $iVdoName $i]
      :if ($chr = " ") do={ :set $chr "%20" }
      :set xVendo ($xVendo . $chr)
    }
    :local iUActive [/ip hotspot active print count-only];
    :local iMessage ("<<======New Sales======>>%0A".\
                     "Vendo: $xVendo %0A".\
                     "Voucher: $user %0A".\
                     "IP: $address %0A".\
                     "MAC: $mac %0A".\
                     "Amount: $iSaleAmt %0A".\
                     "Extended: $iExtCode %0A".\
                     "Total Time: $iTimeMin %0A %0A".\
                     "Today Sales: $iDailySales %0A".\
                     "Monthly Sales: $iMonthSales %0A".\
                     "Active Users: $iUActive %0A".\
                     "Valid Until: $iValidUntil %0A".\
                     "<<=====================>>");
    /tool fetch url="https://api.telegram.org/bot$iTBotToken/sendmessage\?chat_id=$iTGrChatID&text=$iMessage" keep-result=no;
  }
};
# Random Mac
:if ($isRandomMacSyncFix=1) do={
  :local cmac $"mac-address";
  :foreach AU in=[/ip hotspot active find user="$username"] do={
    :local amac [/ip hotspot active get $AU mac-address];
    :if ($cmac!=$amac) do={  /ip hotspot active remove [/ip hotspot active find mac-address="$amac"]; }
  }
}


```

Put on the on logout script

```bash
:if ($cause="session timeout") do={
  /system scheduler set [find name=$user] interval=5s;
}
```

![alt text](/docs/JuanFi-Mikrotik-Step4.PNG?raw=true)

## **Miscellaneous Scripts**

You can create a scheduler to restart (System - > Scheduler) add your desired schedule and put this script or modify the existing template scripts below in your desired settings

- **38vz2rb6nk** - this is the API KEY you generate in admin panel
- **10.10.10.251** - this is your ESP IP Address

Replace those value with your own setting

### **Restart vendo scheduler**

Sample Script that run at 3am:

```bash
  /system scheduler add interval=1d name="Restart Vendo" on-event="/tool fetch http-method=post http-header-field=\"X-TOKEN: 38vz2rb6nk\" url=\"http://10.10.10.251/admin/api/restartSystem\"" policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon start-date=Sep/28/2021 start-time=03:00:00;
```

### **Night Light schedulers**

Sample Script that turn on nightlight at 6 pm:

```bash
 /system scheduler add interval=1d name="Turn ON Night Light" on-event="/tool fetch http-method=post http-header-field=\"X-TOKEN: 38vz2rb6nk\" url=\"http://10.10.10.251/admin/api/toggerNightLight\?toggle=1\"" policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon start-date=Sep/28/2021 start-time=18:00:00;
```

### **Sample Script that turn off nightlight at 6 am:**

```bash
 /system scheduler add interval=1d name="Turn OFF Night Light" on-event="/tool fetch http-method=post http-header-field=\"X-TOKEN: 38vz2rb6nk\" url=\"http://10.10.10.251/admin/api/toggerNightLight\?toggle=0\"" policy=ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon start-date=Sep/28/2021 start-time=06:00:00;
```


# **Mikrotik Hotspot Portal**

![alt text](/docs/Mikrotik-hotspot.PNG?raw=true)

# **Admin Panel Dashboard**

![alt text](/docs/JuanFi-Step05.PNG?raw=true)

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
