# LocalToNet Setup in GitHub Codespaces

This guide provides step-by-step instructions to install and use LocalToNet in a GitHub Codespaces VSCode environment. Follow these steps to easily set up a tunnel to connect your local server (e.g., Minecraft) with the outside world.

## Requirements

- A GitHub account
- Access to GitHub Codespaces
- Basic knowledge of terminal commands

## Installation Steps

1. **Open Terminal**  
   Launch a terminal in your GitHub Codespaces environment.

2. **Download LocalToNet**  
   Run the following command to download the LocalToNet Linux binary:
   ```bash
   wget https://localtonet.com/download/localtonet-linux-x64.zip
   ```

3. **Unzip the Downloaded File**  
   Once the file is downloaded, unzip it using:
   ```bash
   unzip localtonet-linux-x64.zip
   ```

4. **Switch to Root User**  
   Gain root privileges by executing:
   ```bash
   sudo -s
   ```

5. **Grant Execution Permission**  
   Make the LocalToNet binary executable:
   ```bash
   chmod 777 ./localtonet
   ```

6. **Setup Complete**  
   The setup is now complete!

## Connecting to LocalToNet

1. **Sign Up on LocalToNet**  
   Open a browser, navigate to [LocalToNet](https://localtonet.com), and sign up for an account.

2. **Copy Access Token**  
   After signing up, copy your access token from the LocalToNet dashboard.

3. **Authenticate in Codespaces**  
   Back in your GitHub Codespaces terminal, run the following command to authenticate:
   ```bash
   ./localtonet authtoken YOUR_AUTH_TOKEN
   ```
   Replace `YOUR_AUTH_TOKEN` with the token you copied earlier.

4. **Check Connection**  
   If successful, the terminal should indicate that your machine is connected.

5. **Re-authenticate if Needed**  
   Each time you restart Codespaces or close the terminal, re-run the above command to re-authenticate.

## Creating and Managing Tunnels

1. **Create a Tunnel**  
   In the LocalToNet website, navigate to **My Tunnels** and choose the **TCP - UDP** option. Configure your tunnel with the following settings:
   - **Protocol Type:** UDP - TCP
   - **Server:** SG-Singapore (or any other server)
   - **Port:** 25565 (or your desired port)

2. **Copy Tunnel Domain**  
   After creating the tunnel, copy the domain and port (e.g., `in1.localto.net:3991`) to connect your client (e.g., Minecraft) to your server.

3. **Manage Tunnel**  
   Remember to stop the tunnel when not in use to avoid unnecessary resource usage.

## Conclusion

You're all set! Follow these steps accordingly to create and manage tunnels easily in your GitHub Codespaces. Enjoy!
