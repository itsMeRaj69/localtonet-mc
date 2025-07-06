# LocalToNet - Minecraft Port Forwarding Setup

This guide walks you through the steps to install and use LocalToNet *(In our case; In a GitHub Codespaces environment)*.

Follow these steps to easily set up a tunnel to connect your local server (e.g., Minecraft) and invite other players.

## Requirements

- A GitHub account
- Access to GitHub Codespaces 
- Basic knowledge of terminal commands

## Steps to Get Started

1. **Open Terminal**  
   Start by opening a terminal in your GitHub Codespaces environment.

2. **Download LocalToNet**  
   Run the command below to download the LocalToNet Linux binary:
   ```bash
   wget https://localtonet.com/download/localtonet-linux-x64.zip
   ```

3. **Unzip the Downloaded File**  
   After the download is complete, unzip the file:
   ```bash
   unzip localtonet-linux-x64.zip
   ```

4. **Switch to Root User**  
   Gain root privileges by running:
   ```bash
   sudo -s
   ```

5. **Grant Execution Permission**  
   Make the LocalToNet binary executable with:
   ```bash
   chmod 777 ./localtonet
   ```

6. **Setup Complete**  
   Your setup is now complete.

## Connecting to LocalToNet

1. **Sign Up**  
   Open a browser and go to [LocalToNet](https://localtonet.com) to sign up for an account.

2. **Get Access Token**  
   Once signed up, copy your access token from the LocalToNet dashboard.

3. **Authenticate in Codespaces**  
   Back in your Codespaces terminal, run:
   ```bash
   ./localtonet authtoken YOUR_AUTH_TOKEN
   ```
   Replace `YOUR_AUTH_TOKEN` with the token you copied.

4. **Verify Connection**  
   If everything went well, your terminal should show that the machine is connected.

5. **Re-authenticate When Needed**  
   Remember to re-run the command `./localtonet` if you restart Codespaces or close the terminal.

## Setting Up Tunnels

1. **Create a Tunnel**  
   On the LocalToNet website, go to [**My Tunnels** > **TCP - UDP**](https://localtonet.com/tunnel/tcpudp) and set up your tunnel with:
   - **Protocol Type:** UDP - TCP
   - **Server:** Choose one, e.g., SG-Singapore
   - **Port:** 25565 (or any other port you need)

2. **Use the Tunnel**  
   After creating the tunnel, copy the domain and port (e.g., `in1.localto.net:3991`). You can use this to connect your client (e.g., Minecraft) to your server.

3. **Manage Tunnel Usage**  
   Stop the tunnel when you're not using it to save resources.

## FAQ

**Q: Why can't I connect with the IP and port? Why is the connection invalid?**  
**A:** The port changes each time you stop and start the tunnel. So, every time you restart the tunnel, you'll need to copy the new port and use that to connect.

## Done!

That’s it. If you have followed each steps correctly, then you’re all set. Enjoy playing Minecraft with your friends! ✨
