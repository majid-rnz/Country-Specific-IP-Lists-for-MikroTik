# Country-Specific-IP-Lists-for-MikroTik
A collection of IP address lists categorized by country for MikroTik firewalls to streamline network configuration and management.

This repository provides categorized IP address lists for various countries, specifically formatted for MikroTik firewall configurations. These lists can be directly imported into MikroTik devices to enhance network management, implement country-specific rules, or block/allow traffic based on geographic locations.

The available country lists include:

Afghanistan (AF-IP)
Armenia (Armenia-IP)
Bahrain (Bahrain-IP)
Iraq (Iraq-IP)
Iran (IR-IP)
Oman (Oman-IP)
Qatar (Qatar-IP)
Turkmenistan (TM-IP)
United Arab Emirates (UAE-IP)
Each list is meticulously prepared and regularly updated to ensure accuracy. Users can easily integrate these lists into their MikroTik configurations with minimal effort.

## How to Use These IP Lists in MikroTik

### 1. Download Files from GitHub
Select the file corresponding to your desired country from this repository and download it. The files are preformatted as MikroTik scripts.

### 2. Upload the File to MikroTik
Open **Winbox** and navigate to the **Files** menu. Upload the downloaded file to your MikroTik device.

### 3. Run the Script
Go to the **Terminal** and execute the following command to apply the script:
```bash
/import file-name=<YourFileName.rsc>
```
Replace `<YourFileName.rsc>` with the name of the uploaded file.

### 4. Verify the Address Lists
After running the script, check the imported address lists using the following command:

```bash
/ip firewall address-list
```

### 5. Use the Lists in Firewall Rules
You can utilize the imported address lists in your firewall rules. For example:

```bash
/ip firewall filter
add chain=forward src-address-list=Armenia action=drop comment="Block traffic from Armenia"
```
This rule blocks traffic originating from the "Armenia" address list.

By following these steps, you can easily implement country-specific IP management on your MikroTik device.


