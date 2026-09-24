<div align="center">
  <h1>Omega (UNOFFICIAL)</h1>
  <p>Basicly all and any certificates that you used gets unblacklisted :).</a></p>
  <p>Supports: IOS 16-26.2</p>
  <p>Possible buggy IOS versions:<p>
  <p>- IOS 27.0 (just don't try it's unsupported)<p>
  <p>- IOS 26.2 (it didn't work for me. I prolly just did it wrong)<p>
    <a href="https://github.com/jailbreakdotparty/Omega/stargazers"> <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/jailbreakdotparty/omega?style=flat-square&color=%23FFD300"></a> 
    <a href="https://jailbreak.party/discord"><img alt="Discord" src="https://img.shields.io/discord/1349128546072793218?style=flat-square&logo=discord&logoColor=FFFFFF&color=5865F2"></a> 
    <a href="https://jailbreak.party"><img alt="Static Badge" src="https://img.shields.io/badge/jailbreak.party-blue?style=flat-square&label=%20&color=3868DB"></a>
</div>

> [!WARNING]
> Make a backup before using this tool **JUST IN CASE.** jailbreak.party and StudioTheDev are not responsible for any damages that this may cause to your device, so use at your own risk.

### Usage
**Requirements**
- A computer with Python 3.9+, [pymobiledevice3](https://github.com/doronz88/pymobiledevice3), and `click` installed.
- On Windows, [Apple Devices](https://apps.microsoft.com/detail/9np83lwlpz9k) or [iTunes](https://support.apple.com/en-us/106372) installed.
- On Linux, [usbmuxd](https://github.com/libimobiledevice/usbmuxd) and [libimobiledevice](https://github.com/libimobiledevice/libimobiledevice).
- An iOS device running iOS 16 or higher through IOS 26.2.

**Steps (Updated from experience)**
1. Disable Find My on your device. This is required to restore the partial backup, you can re-enable it after you're done.

2. Connect your device to your computer via USB (Keeped plugged in the whole time).

3. Go on your pc and install [Python 3.12 (recommended)](https://apps.microsoft.com/detail/9ncvdn91xzqp?hl=en-US&gl=US).

4. Open CMD and type `cd /d "C:\Users\You\Desktop\omega-version-gate"` and hit enter.

5. type this `python -m venv .venv`

6. and this `.venv\Scripts\activate` the CMD should look like this `(.venv) C:\Users\You\Desktop\Omega>`

7. after your done run this `python -m pip install --upgrade pip` and should look like this `(.venv) C:\Users\You\Desktop\Omega>python -m pip install --upgrade pip`

8. then install `click` which is this command `python -m pip install -U pymobiledevice3 click`

(Optional Recommended Step): this is to make sure your phone is connected to pymobiledevice `pymobiledevice3 usbmux list` if your phone is listed your good to move onto the next step.

9 (final): to finaly run Omega `python omega_fixed.py` looks like `(.venv) C:\Users\You\Desktop\Omega>python omega_fixed.py` 

--------------------------------- Fixes ---------------------------------
Fix 1: python -m pip install --force-reinstall cffi
Fix 2: python -m pip install --force-reinstall pywin32
Fix 3: python .venv\Scripts\pywin32_postinstall.py -install (this is connected to Fix 2)

note: make sure it's like `(.venv) C:\Users\You\Desktop\Omega>python (Whatever command you run)`

### Info
iOS stores certain databases containing information on which sideloaded apps are revoked and the validity of signing certificates at `/var/db/MobileIdentityData/` and `/var/protected/trustd/`.

Using partial backups, we can restore these files and clear them, or replace them with directories.

This tool replaces the databases with directories of the same name, which causes the system to fail when attempting to write to them, therefore preventing your device from "remembering" any revokes or blacklisted certificates.

### Credits
- [Mineek](https://github.com/mineek) - documented & discovered [this whole concept](https://gist.github.com/mineek/f17df8b95e6fb168a9b9929e2993e900/)
- [Duy Tran](https://github.com/khanhduytran0) - shared persistence (directory overwrite) strategy
- [JJTech](https://github.com/JJTech0130/) - developed [sparserestore](https://github.com/JJTech0130/TrollRestore/tree/main/sparserestore) (backup creation) library
- [LeminLimez](https://github.com/leminlimez) - reference and skipsetup config
- [Skadz](https://github.com/skadz108) - developer

### Unoffical Credits
- [StudioTheDev](https://github.com/StudioTheDev) - A random ahh kid ✌️ (fixer)
