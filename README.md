# Windows 11 & 10 Activation Errors and Fixes

A complete reference of Windows activation error codes: what each one means and how to fix it, step by step. It covers Windows 11 and Windows 10 Home, Pro, Education and Enterprise.

Maintained by [Noxkeys](https://noxkeys.com/), an online store for genuine software licences. Corrections are welcome.

---

## Table of contents

- [Quick fixes to try first](#quick-fixes-to-try-first)
- [How to find your error code](#how-to-find-your-error-code)
- [Product key and licence errors](#product-key-and-licence-errors)
- [Edition mismatch errors](#edition-mismatch-errors)
- [Key used on too many devices](#key-used-on-too-many-devices)
- [Hardware change errors](#hardware-change-errors)
- [Network and server errors](#network-and-server-errors)
- [KMS and volume licence errors](#kms-and-volume-licence-errors)
- [System and update errors](#system-and-update-errors)
- [Step-by-step fixes](#step-by-step-fixes)
- [When you need a new product key](#when-you-need-a-new-product-key)
- [FAQ](#faq)
- [Related guides](#related-guides)
- [References](#references)

---

## Quick fixes to try first

Many activation errors are fixed by one of these four steps:

1. **Run the Activation troubleshooter:** *Settings → System → Activation → Troubleshoot*
2. **Check the date and time:** *Settings → Time & language → Date & time → Sync now*
3. **Check your internet connection** and temporarily disable any VPN or third-party firewall
4. **Restart the PC** and try activating again

If none of these work, find your error code below.

---

## How to find your error code

Go to **Settings → System → Activation**. The error code appears under *Activation state*.

You can also check from **Command Prompt (Admin)**:

```bat
:: Show activation status and licence channel (Retail / OEM / Volume)
slmgr /dli

:: Show whether activation is permanent
slmgr /xpr
```

---

## Product key and licence errors

| Error code   | What it means                                          | Fix                                                                         |
| ------------ | ------------------------------------------------------ | --------------------------------------------------------------------------- |
| `0x803F7001` | No valid licence was found on this PC                  | Enter a genuine product key. See [Change product key](#2-change-the-product-key) |
| `0x800704CF` | No valid licence found, or the network can't be reached | Enter a genuine key. After a hardware change, run the Activation troubleshooter |
| `0xC004F213` | No product key was found on the device                 | Enter a genuine product key or sign in with the Microsoft account linked to your licence |
| `0xC004C003` | The product key is invalid or blocked                  | The key was likely used elsewhere. Contact the seller or use a genuine key  |
| `0xC004C060` | The product key is no longer valid                     | Replace it with a genuine key from an authorised seller                     |
| `0xC004F050` | The product key entered is invalid                     | Re-check for typos, or enter a genuine key                                  |
| `0xC004F034` | Invalid key, or a key for a different Windows version  | Use a key that matches your Windows version and edition                     |

---

## Edition mismatch errors

These happen when the key is for a different edition than the one installed, for example a **Pro** key on **Home**.

| Error code   | What it means                                          | Fix                                                                         |
| ------------ | ------------------------------------------------------ | --------------------------------------------------------------------------- |
| `0xC004F212` | The key isn't compatible with the installed edition    | Install the matching edition, or use a key for the edition you have         |
| `0xC004F210` | The key or digital licence doesn't match the edition   | Enter a matching key, or reinstall the edition your licence is for          |
| `0xC004E016` | The key is for a different version or edition          | Enter a key that matches your installed version and edition                 |
| `0xC004F00F` | An Enterprise key was entered on Home or Pro           | Enter a Home or Pro key that matches your edition                           |

**Tip:** to move from Home to Pro, see [Upgrade Home to Pro](#5-upgrade-windows-11-home-to-pro).

---

## Key used on too many devices

| Error code   | What it means                                          | Fix                                                                         |
| ------------ | ------------------------------------------------------ | --------------------------------------------------------------------------- |
| `0xC004C008` | The key has already been used on another PC            | Each PC needs its own key. Buy a separate key for this device              |
| `0xC004C770` | The key has been used on more devices than allowed     | Buy a separate key for this device                                          |
| `0x803FA071` | The key has been used on more devices than allowed     | Buy a separate key for this device                                          |
| `0xC004C020` | A volume licence exceeded its activation limit         | Contact your organisation's IT department, or use a different key          |

---

## Hardware change errors

| Error code   | What it means                                                    | Fix                                                                       |
| ------------ | ---------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `0xC004F211` | Major hardware changed (usually the motherboard), so the licence wasn't found | Run the Activation troubleshooter and choose *"I changed hardware on this device recently"* |

This only works if your digital licence was **linked to a Microsoft account before** the hardware change. See [Reactivate after a hardware change](#3-reactivate-after-a-hardware-change).

---

## Network and server errors

| Error code                               | What it means                                         | Fix                                                                 |
| ---------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------------------- |
| `0xC004FC03`                             | No internet connection, or a firewall is blocking activation | Check the connection and firewall, or [activate by phone](#4-activate-by-phone) |
| `0x8007267C`                             | No internet, or the activation server is unavailable  | Check your connection and firewall, then try again                 |
| `0x80072F8F`                             | Wrong date/time, or can't reach the activation service | Fix the date and time, check the internet connection, then restart |
| `0xC004E028`                             | An activation request is already in progress          | Wait for the first request to finish                               |
| `0xD0000272` `0xC0000272` `0xC004C012` `0xC004C013` `0xC004C014` | The activation server is temporarily unavailable | No action needed. Windows activates automatically when it's back |
| `0x87E10BC6`                             | A problem with the licensing server                   | Wait a few minutes, then run the Activation troubleshooter again   |

---

## KMS and volume licence errors

These appear when the PC has a **KMS client key** (common after using generic or volume keys) but no company KMS server is available.

| Error code   | What it means                                         | Fix                                                                     |
| ------------ | ----------------------------------------------------- | ----------------------------------------------------------------------- |
| `0xC004F074` | No KMS server could be contacted                      | On a home PC, replace the KMS key with a genuine retail key            |
| `0x8007232B` | The KMS host could not be found (DNS name doesn't exist) | On a home PC, replace the KMS key with a genuine retail key         |
| `0xC004F038` | The KMS server doesn't have enough clients to activate | On a company network, contact IT. On a home PC, use a retail key      |
| `0x8007007B` | Activation failed, often due to a volume key with no KMS host | Replace the key with a genuine retail key                        |
| "Your Windows licence will expire soon" | A volume licence is installed and managed by an organisation | Contact your IT administrator, or install a retail key on a personal PC |

> **Using a generic or KMS key at home?** Those keys only install Windows. They can't activate it. See the companion reference [Windows 11 & 10 Product Keys](https://github.com/noxkeys/windows-11-10-product-keys).

---

## System and update errors

| Error code   | What it means                                          | Fix                                                                     |
| ------------ | ------------------------------------------------------ | ----------------------------------------------------------------------- |
| `0xC004E003` | Third-party software changed system files activation needs | Restore Windows to an earlier restore point                          |
| `0x80004005` | A general, unspecified activation failure              | Run the Activation troubleshooter. If it still fails, [repair system files](#6-repair-system-files) |
| `0x80070652` | Missing or corrupted update components                 | Run the Windows Update troubleshooter and check your connection        |

---

## Step-by-step fixes

### 1. Run the Activation troubleshooter

1. Open **Settings → System → Activation**
2. Click **Troubleshoot** (it appears only when Windows isn't activated)
3. Follow the prompts. After a hardware change, choose *"I changed hardware on this device recently"*

### 2. Change the product key

**Using Settings:** go to *Settings → System → Activation → Change product key* and enter your 25-character key.

**Using Command Prompt (Admin):**

```bat
:: Remove the old key
slmgr /upk
slmgr /cpky

:: Install the new key
slmgr /ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX

:: Activate online
slmgr /ato
```

### 3. Reactivate after a hardware change

1. Sign in to Windows with the **Microsoft account** your digital licence is linked to
2. Go to **Settings → System → Activation → Troubleshoot**
3. Select **"I changed hardware on this device recently"**
4. Choose this device from the list and click **Activate**

If your licence was never linked to a Microsoft account, you'll need a new product key.

### 4. Activate by phone

Use this when online activation fails because of network problems:

```bat
slui 4
```

Select your country and follow the automated phone instructions. Phone activation isn't available for Windows Pro Education or Pro for Workstations.

### 5. Upgrade Windows 11 Home to Pro

1. Go to **Settings → System → Activation → Change product key**
2. Enter your genuine **Windows 11 Pro** key
3. Windows upgrades to Pro and restarts. Your files and apps are kept

### 6. Repair system files

Run these in **Command Prompt (Admin)**, one after the other:

```bat
DISM /Online /Cleanup-Image /RestoreHealth
sfc /scannow
```

Restart and try activating again.

### 7. Fix the date and time

```bat
w32tm /resync
```

Or go to *Settings → Time & language → Date & time*, turn on **Set time automatically** and click **Sync now**.

---

## When you need a new product key

Some errors can't be fixed without a new key:

- The key was blocked or is no longer valid (`0xC004C003`, `0xC004C060`)
- The key was already used on another PC (`0xC004C008`, `0xC004C770`, `0x803FA071`)
- A generic or KMS key is installed on a home PC (`0xC004F074`, `0x8007232B`)
- The motherboard was replaced and the licence wasn't linked to a Microsoft account (`0xC004F211`)
- You need a different edition, for example Pro instead of Home (`0xC004F212`, `0xC004F210`)

Genuine **Windows 11 Pro** and **Windows 11 Home** keys with instant email delivery are available at **[noxkeys.com](https://noxkeys.com/)**.

---

## FAQ

**What happens if I don't activate Windows?**
Windows keeps working, but you'll see an "Activate Windows" watermark, personalisation settings are locked, and you'll get regular reminders.

**Can I reuse my Windows 10 key for Windows 11?**
Yes. A genuine Windows 10 key activates Windows 11 of the same edition.

**Why did Windows deactivate after I replaced my motherboard?**
Windows ties the licence to your hardware. Replacing the motherboard counts as a new PC. If your licence is linked to a Microsoft account, use the Activation troubleshooter to reactivate.

**Why does my key say it's been used too many times?**
Retail and OEM keys activate one PC at a time. If you bought a key that was already used, contact the seller for a replacement.

**How do I check whether my licence is Retail, OEM or Volume?**
Run `slmgr /dli` in Command Prompt. The description shows the licence channel.

**Is it safe to use activation tools or scripts from the internet?**
No. Unofficial activators often contain malware and violate Microsoft's licence terms. A genuine key is the safe and legal option.

---

## Related guides

More free references maintained by [Noxkeys](https://noxkeys.com/):

- [Windows 11 & 10 Product Keys](https://github.com/noxkeys/windows-11-10-product-keys): generic and KMS client keys for every Windows edition
- [Microsoft Office 2024, 2021 & 2019 Product Keys](https://github.com/noxkeys/microsoft-office-2024-2021-2019-product-keys): Office KMS keys, ospp.vbs commands and version comparison
- [Windows Server 2025, 2022 & 2019 Product Keys](https://github.com/noxkeys/windows-server-2025-2022-2019-product-keys): Server KMS keys, Standard vs Datacenter and Evaluation conversion
- [How to Upgrade Windows 11 Home to Pro](https://github.com/noxkeys/upgrade-windows-11-home-to-pro): step-by-step upgrade without reinstalling
- [Microsoft Office Activation Errors and Fixes](https://github.com/noxkeys/microsoft-office-activation-errors): fix "Unlicensed Product" and Office error codes

---

## References

- [Microsoft Support – Get help with Windows activation errors](https://support.microsoft.com/en-us/windows/get-help-with-windows-activation-errors-09d8fb64-6768-4815-0c30-159fa7d89d85)
- [Microsoft Support – Activate Windows](https://support.microsoft.com/en-us/windows/activate-windows-c39005d4-95ee-b91e-b399-2820fda32227)
- [Windows 11 & 10 Product Keys](https://github.com/noxkeys/windows-11-10-product-keys) – generic and KMS keys for Windows
- [Microsoft Office 2024, 2021 & 2019 Product Keys](https://github.com/noxkeys/microsoft-office-2024-2021-2019-product-keys) – KMS keys and activation fixes for Office
- [Windows Server 2025, 2022 & 2019 Product Keys](https://github.com/noxkeys/windows-server-2025-2022-2019-product-keys) – KMS keys for Windows Server
- [Noxkeys – Genuine Windows licences](https://noxkeys.com/)

---

⭐ **If this helped, star the repo** so others can find it. Last updated: October 2026.
