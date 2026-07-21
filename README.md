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

## 🔒 Privacy & Disclaimers

### ⚠️ Backend API Disclaimer
- **Purple Installer** is a just a front end client sided website and does **not** host, own, or maintain the backend signing API ([Daisuke Signer](https://daisign.lol/)).
- **User Discretion:** Use this tool at your own risk. Knowing that the backend signer is not managed by this project, it is entirely up to the user to decide if they trust `daisign.lol` with their signing credentials, as there is always an inherent risk with using an online signing tool like this, no matter how trustworthy it is.

### 🔑 Certificate & Credential Privacy
- **100% Local Storage:** Any certificates (`.p12`), provisioning profiles (`.mobileprovision`), and passwords saved via the Certificates tab are stored **strictly on your local device** using your browser's native `localStorage`.
- **No Middleman Logging:** Purple Installer is completely client sided, and does not log or store any certificates on a seperate server.  
- **Direct Transmission:** When signing an app your certificate is sent securely over HTTPS directly from your browser straight to the signing backend API.

## 🤝 This Couldn't Be Done Without...

### ⚙️ Backend & Services
- [Daisuke Signer](https://daisign.lol/) - Signing backend API
- [GitHub REST API](https://docs.github.com/en/rest) - Github release and IPA fetching
- [jsDelivr](https://www.jsdelivr.com/) - Open source CDN hosting for client scripts

### 🧩 Client Libraries
- [node-qrcode](https://github.com/soldair/node-qrcode) - Client side QR code generator

### 📱 Included Applications
- [Feather](https://github.com/claration/Feather) - Feather IPA
- [Ksign](https://github.com/Nyasami/Ksign) - Ksign IPA
- [SideInstaller](https://github.com/FrizzleM/SideInstaller) & [SideStore](https://sidestore.io/) - SideInstaller IPA and the SideStore app itself

### 💡 Project Inspiration
- [Feather Installer](https://github.com/yodaluca23/Feather-Installer) - Project inspiration
