<div align="center">
  <br>
  <a href="https://purpleinstaller.c0n.xyz/">
    <img width="180" alt="Purple Installer Logo" src="https://github.com/user-attachments/assets/284e96c8-fcc4-4f48-9efa-66a931b6a420">
  </a>
  <br>
  <h1><a href="https://purpleinstaller.c0n.xyz/">Purple Installer</a></h1>

  A web-based tool that allows you to seamlessly sign and install or update [Feather](https://github.com/claration/Feather), [Ksign](https://github.com/Nyasami/Ksign), and [SideInstaller](https://github.com/FrizzleM/SideInstaller) using an iOS signing certificate (`.p12`) and (`.mobileprovision`)

  Inspired by yodaluca23's [Feather Installer](https://github.com/yodaluca23/Feather-Installer)
</div>

---

## ✨ Features

- Choose from either Feather, Ksign, or SideInstaller
- Choose from a list of recent releases (latest stable release is selected by default)
- Save certificates to the website local storage and easily use them multiple times
- Direct OTA (`itms-services://`) installation in the tap of a button
- Copy OTA link to your clipboard
- Generate QR code of OTA link
- Download signed IPA file

## ⚙️ How It Works

- Select your preferred app and version
- Upload your certificate pair and password or select a locally saved certificate
- The direct IPA URL is fetched from the app's GitHub releases
- The IPA URL (using the ipaUrls feature) along with your certificate are sent to the [Daisuke Signer API](https://daisign.lol/)
- The app is signed on the Daisuke backend, and a direct install URL to the plist and a download URL to the signed IPA are returned
- If you choose to generate a QR code, then [node-qrcode](https://github.com/soldair/node-qrcode) generates one to the direct install URL
