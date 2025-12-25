# Fortnite Server Assets (PS4 Builds)

This repository documents the process of extracting **server assets** from supported **Fortnite PS4 builds**.

Server assets are required for:
- POI Manager
- Proper navigation mesh (NavMesh) functionality
- BotNames
- Maps like Creative hub
- And more

## Supported Versions

⚠️ **Important**

- **PS4 builds from OT 6.5 through 12.61 (Maybe 13.00) include server assets**
- **Builds newer than 12.61 do NOT contain server assets**

This method will not work on versions outside the supported range.

## Prerequisites
- Basic understanding of game asset extraction

### Required Tools
- **PS4PKGViewer**
- **PS4-PKG-Tools**
- **FModel**
-  **u4pak**

## Extraction Guide

### Step 1: Download Fortnite PS4 PKGs

Visit:

https://orbispatches.com/CUSA07022

Use `CTRL + F` to locate the Fortnite version you need  
Example: `12.41`

Download **all PKG files** for that version:
- Typically **9–12 PKG files**
- **Do NOT download delta PKGs**

### Step 2: Merge PKG Files

1. Open **PS4PKGViewer**
2. Merge all downloaded PKGs into a **single PKG file**

> This process may take several minutes.

### Step 3: Extract the Merged PKG

1. Open **PS4-PKG-Tools**
2. Extract the merged PKG file to a directory of your choice
   
Note: if it asks for a password to decrypt use these:

**Fortnite PKG EUR Passcode key:** `4uD7qyfx9TRfRLP7kQTWjxWdh8zb85eY`

**Fortnite PKG US Passcode key:** `ZcR3MhZHd1jeAiX20yR-jmnPEqo-9Pog`

### Step 4: Locate Server Assets and extract them

1. Open **FModel**
2. Add the [AES](https://github.com/dippyshere/fortnite-aes-archive) keys and load the Paks using FModel
3. Browse the content to locate the **server assets**
4. Extract them
5. Use u4pak to pak them (Make a sig file by getting a random sig dile from your builds paks and rename it the same name as your pak)

**For example:**

NavMesh is located at: `FortniteGame/Content/Maps/Apollo_Nav_Gameplay`

Bounds are located at: `FortniteGame/Content/Maps/NavMeshBounds`

POI Manager is located at: `FortniteGame/Content/Athena/Apollo/Maps (Every File)`

BotNames are located at: `FortniteGame/Content/Athena/AI/Phoebe/Names (Every File)`

## Notes

- Server assets are exclusive to supported PS4 builds (Maybe other console builds)
- This repository is intended for **educational and research purposes only**

## Disclaimer

This project is not affiliated with, endorsed by, or associated with Epic Games.  
Fortnite and Unreal Engine are trademarks of Epic Games, Inc.

Use this information responsibly and in accordance with applicable laws.
