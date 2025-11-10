# Setting Up Tribal Trouble - 32-bit Java Required

## Issue
The native graphics libraries (LWJGL) in this project are 32-bit only. To run the game, you need to use 32-bit Java.

## Solution
Install 32-bit Eclipse Temurin Java:

1. Download **32-bit JDK** from: https://adoptium.net/temurin/releases/
2. Choose version **Java 8 or newer, x86 (32-bit)**
3. Install to a directory like `C:\Program Files (x86)\Eclipse Adoptium\jdk-xx-hotspot`
4. Verify installation:
   ```cmd
   "C:\Program Files (x86)\Eclipse Adoptium\jdk-xx-hotspot\bin\java.exe" -version
   ```

5. Set the JAVA_HOME environment variable:
   - Go to: Settings → Environment Variables
   - Create/Edit `JAVA_HOME` = `C:\Program Files (x86)\Eclipse Adoptium\jdk-xx-hotspot`
   - Add to PATH: `%JAVA_HOME%\bin`

6. Restart Command Prompt and run:
   ```cmd
   cd tribaltrouble\tt
   ant run
   ```

## Alternative: Upgrade to 64-bit Libraries
If you want to use 64-bit Java, the LWJGL native libraries would need to be recompiled for 64-bit Windows, which requires building from source.
