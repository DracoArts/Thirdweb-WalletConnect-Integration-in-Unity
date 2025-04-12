
# Welcome to DracoArts

![Logo](https://dracoarts-logo.s3.eu-north-1.amazonaws.com/DracoArts.png)




#  Thirdweb WalletConnect Integration in Unity
WalletConnect is an open-source protocol that enables secure communication between decentralized applications (dApps) and mobile wallets. It allows users to connect their MetaMask, Trust Wallet, Coinbase Wallet, and other Web3 wallets to apps via QR codes or deep links without exposing private keys.
# Why Use Thirdweb’s Unity SDK?
Thirdweb simplifies Web3 integration in Unity by providing:

- Pre-built WalletConnect support (no manual Web3.js setup)

- Cross-platform compatibility (Android, iOS, PC, WebGL)

- Easy wallet authentication & transactions

- Smart contract interaction (NFTs, tokens, marketplaces)
# Key Features of Thirdweb + WalletConnect in Unity
## 1.Seamless Wallet Connection

- Users scan a QR code or open a deep link to connect their wallet.

- No need for seed phrase input (secure & user-friendly).

## 2.Multi-Chain Support

- Works with Ethereum, Polygon, Solana, Avalanche, etc.

- Switch networks dynamically (e.g., from Ethereum to Polygon).

## 3. Transaction & Signing Support

- Players can send crypto, mint NFTs, or sign messages securely.

- Cross-Platform Compatibility

- Works on mobile (Android/iOS), desktop, and WebGL builds.
# How It Works 
- Player clicks "Connect Wallet" in the Unity game.

- A QR code appears (on desktop) or wallet app opens (on mobile).

- Player approves the connection in their wallet (e.g., MetaMask).

- Game detects the connected wallet and displays the address.

 - Player can now perform Web3 actions (buy NFTs, earn tokens, etc.).

 # Use Cases for Unity Games

- ✔ NFT-Based Games – Players connect wallets to own in-game assets.

- ✔ Play-to-Earn (P2E) – Securely distribute crypto rewards.

- ✔ Token-Gated Content – Unlock features for NFT holders.

- ✔ DAO & Governance – Let players vote using their wallets.

# Install Thirdweb Unity SDK
### Option A: Via Unity Package Manager (UPM)
- Open Unity and go to Window > Package Manager.

- Click the + button and select Add package from git URL.

- Paste the Thirdweb Unity SDK Git URL:

Copy

     https://github.com/thirdweb-dev/unity.git
Click Add.

### Option B: Via .unitypackage
- 
Download the latest .unitypackage from Thirdweb’s 

[GitHub Releases](https://github.com/thirdweb-dev/unity/releases")

- In Unity, go to Assets > Import Package > Custom Package.

- Select the downloaded .unitypackage and import all files.
## Usage/Examples
    using UnityEngine;
    using Thirdweb;

    public class WalletConnectManager : MonoBehaviour
    {
    private ThirdwebSDK walletConnectsdk;

    void Start()
    {
           walletConnectsdk = new ThirdwebSDK("sepolia"); // Use your desired chain (e.g., "ethereum", "polygon", etc.)
    }

    // Connect Wallet via WalletConnect
    public async void ConnectWallet()
    {
        try
        {
            string address = await walletConnectsdk.wallet.Connect(
                new WalletConnection()
                {
                    provider = WalletProvider.WalletConnect,
                    chainId = 11155111 // sepolia testnet
                }
            );
            Debug.Log("Connected wallet: " + address);
        }
        catch (System.Exception e)
        {
            Debug.LogError("Wallet connection failed: " + e.Message);
        }
    }

    // Disconnect Wallet
    public void DisconnectWallet()
    {
        sdk.wallet.Disconnect();
        Debug.Log("Wallet disconnected");
    }
}
## Image

## Thirdweb Wallet Connect
![](https://github.com/AzharKhemta/Gif-File-images/blob/main/ThirdWeb%20Wallet%20connect.gif?raw=true)



## Authors

- [@MirHamzaHasan](https://github.com/MirHamzaHasan)
- [@WebSite](https://mirhamzahasan.com)


## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/mir-hamza-hasan/posts/?feedView=all/)
## Documentation

[Thirdweb Unity Documentation](https://portal.thirdweb.com/unity/v5)




## Tech Stack
**Client:** Unity,C#

**Plugin:** Thirdweb Unity SDK



