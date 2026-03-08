# Redmi Note 7 Pro (Violet) Flashing Guide
## ⚠️WARNING⚠️
> Flashing can brick your phone and erase all data. Proceed only if you understand the risks.
## Requirments

### 📱Physical Items📱
-Your Phone
- Usb A to Usb C
- Battery Charged at 50% or More
- PC or Laptop
  > (With Windows 10 or Greater; Linux may work with WINE, ADB and Fastboot)

### 🔓Unlocking Bootloader🔓
- Sim Card with Network Connectivity
- A MI Account (equal or older than 30 Days)
- PC or Laptop
  - [MI Flasher](https://xiaomiflashtool.com/wp-content/uploads/MiFlash20220507.zip)

### 🛠️Flashing Recovery🛠️
- PC or Laptop
  - [TWRP](https://dl.twrp.me/violet/twrp-3.7.0_9-0-violet.img)
 
### 📦Flashing the Custom Rom📦
- Your desired Custom ROM (Rename To ROM.zip)
  > Following are some Popular ROMs

| Name | Android Version |
|-----|-----|
|  [Pixel Experience](https://get.pixelexperience.org/violet) | 13, 12 |
| [LineageOS](https://download.lineageos.org/devices/violet/builds) | 16 |
| [CrDroid](https://crdroid.net/downloads#violet) | 10, 11, 12, 13, 14 |
| [EvolutionX](https://evolution-x.org/devices/violet) | 13 |

- Download MindTheGapps for your Android Version (Rename to GApps.zip)
  > Optional If you want Google Services

| Android Version |
| ----------------|
| [Android 11](https://github.com/MindTheGapps/11.0.0-arm64) |
| [Android 13](https://github.com/MindTheGapps/13.0.0-arm64) |
| [Android 14](https://github.com/MindTheGapps/14.0.0-arm64) |
| [Android 15](https://github.com/MindTheGapps/15.0.0-arm64) |
| [Android 16](https://github.com/MindTheGapps/16.0.0-arm64) |



## Setup

- **Step 0:** Start by inserting a SIM card with network connectivity into the device.

- **Step 1:** Sign in to your **Mi Account** on the device.  
  Go to **Settings → Mi Account** and log in with your account.  
  If you do not have one, create it first.
    > NOTE: you will have to wait 30 more days if you make a new account.

- **Step 2:** Go to **Settings → About Phone** and tap **MIUI Version** 10 times to enable *Developer Options*.

- **Step 3:** Go to **Settings → Additional Settings → Developer Options**.

- **Step 4:** Enable **OEM Unlocking**.

- **Step 5:** Enable **USB Debugging**.

- **Step 6:** Scroll down and open **Mi Unlock Status**.

- **Step 7:** Tap **Add account and device** and make sure the phone is connected to **mobile data**.

- **Step 8:** Wait for the confirmation message saying the account was successfully added.
    > Depending on you region and account; you might have to wait for 168 Hours(7 Days) or 360 Hours(15 Days)

## 🔓Unlocking Bootloader🔓

- **Step 1:** Power off the device.

- **Step 2:** Boot into **Fastboot mode** by holding **Volume Down + Power**.

![Fastboot Mode Screen](SS/xiaomi-stuck-on-fastboot-1_cropped_processed_by_imagy.png)

- **Step 3:** Connect the device to your PC using a USB cable.

- **Step 4:** Open the **Mi Unlock Tool** on your computer and log in with the same Mi account.

- **Step 5:** Follow the instructions in the tool to unlock the bootloader.

## 🛠️Flashing TWRP Recovery🛠️

**Step 1:** Download the TWRP recovery image for **violet** and place it inside your **ADB / Fastboot folder**.

**Step 2:** Rename the downloaded file to:
`twrp.img`

**Step 3:** Boot the phone into **Fastboot Mode**.
Hold **Volume Down + Power** until the Fastboot screen appears.

**Step 4:** Connect the phone to your PC using a USB cable.

**Step 5:** Open a **Command Prompt** inside the ADB / Fastboot folder.

**Step 6:** Check if the device is detected:
`fastboot devices`

**Step 7:** Flash TWRP

**Step 8:** Immediately boot into TWRP (important to prevent MIUI from restoring stock recovery)

**Step 9:** Once inside TWRP, swipe to allow modifications.

**Step 10:** (Recommended) Go to **Backup** and create a full backup of your current system.

Your device is now ready to flash a **Custom ROM**.

## 📦Flashing the Custom ROM📦

**Step 0:** Choose a ROM you want to Flash.
  > This time we will use Lineage OS

**Step 1:** Boot the phone into TWRP recovery. You can use the CMD from Windows:
`adb reboot recovery`

**Step 2:** Transfer Files to Device.

- `adb push <ROM.zip> /sdcard/`
- `adb push <GApps.zip> /sdcard/   (if needed)`

**Step 3:** Wipe Dalvik / Cache / Data:
In *TWRP*: `Wipe` → `Advanced Wipe` → `Dalvik / ART Cache, Cache, Data`, then swipe to wipe.

**Step 4:** *Install ROM ZIP:*
- Tap Install, select the ROM ZIP from your phone storage, swipe to flash.

**Step 5:** *Flash GApps (if needed):*
- Tap Install again and select the GApps ZIP. Swipe to flash.

**Step 6:** *Reboot System:*
- Tap Reboot → System. The first boot may take several minutes.

**Step 7:** Follow instructions according to your ROM.

# Congratulations!
