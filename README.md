# Datagram Installation for Linux

This repository provides a simple guide to install, run, and remove the Datagram CLI tool on Linux systems.

> âœ… **Register first using this referral link:**  
> https://dashboard.datagram.network?ref=580071261

---

## ðŸš€ Installation Instructions

### 1. Copy your API Key

- Go to the [Datagram Dashboard](https://dashboard.datagram.network)
- Navigate to: **Wallet > Licenses**
- Click **Copy Key**

### 2. Run this command in your terminal:

```bash
read -p "Enter your API Key: " API_KEY && \
[ -f /usr/local/bin/datagram-cli ] && sudo rm -f /usr/local/bin/datagram-cli; \
[ -f datagram.log ] && rm -f datagram.log; \
[ -d ~/.datagram ] && rm -rf ~/.datagram; \
wget -q https://github.com/Datagram-Group/datagram-cli-release/releases/latest/download/datagram-cli-x86_64-linux && \
sudo mv datagram-cli-x86_64-linux /usr/local/bin/datagram-cli && \
sudo chmod +x /usr/local/bin/datagram-cli && \
nohup datagram-cli run -- -key "$API_KEY" > datagram.log 2>&1 &
```

### 3. Check the running logs

```bash
tail -f datagram.log
```

---

## âŒ Uninstall / Remove

If you want to stop and remove the installation:

```bash
sudo pkill -f "datagram-cli run" 2>/dev/null; \
[ -f /usr/local/bin/datagram-cli ] && sudo rm -f /usr/local/bin/datagram-cli; \
[ -f datagram.log ] && rm -f datagram.log; \
[ -d ~/.datagram ] && rm -rf ~/.datagram
```

---

## ðŸŽ Claim the **Early Alpha Tester Role**

After successfully installing and running the CLI, go to this form and submit your participation:

ðŸ‘‰ **[Submit the Form](https://docs.google.com/forms/d/e/1FAIpQLSevC3QjAx4xdNysKoRtCSR_5cAUtVBhoNu3XoCrQBIOYVQN8A/viewform)**

When filling out the form, use these social links:

- [Discord Community](https://discord.gg/datagramnetwork)
- [Twitter / X](https://x.com/dgramnetwork)
- [Telegram Group](https://t.me/datagramnetwork)

---

## ðŸŒ Official Website

[http://datagram.network/](http://datagram.network/)

---

## ðŸ–¼ Logo

![Datagram Logo](https://pbs.twimg.com/media/GMrIMhKXwAAY2zI?format=jpg&name=large)
