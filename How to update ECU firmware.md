# 🔧 How to Update **BossECU / Honduino** Firmware

> This guide explains how to safely update your ECU firmware using **rusefi_updater.exe**.

---

## ⚙️ Step-by-step Instructions

### 1️⃣ Disconnect from the vehicle
Unplug the ECU from your car before starting the update process.

---

### 2️⃣ Download and extract the firmware bundle
Download the latest firmware package for your ECU model and **extract it** to a convenient location on your computer.

---

### 3️⃣ Open the updater app
Launch **`rusefi_updater.exe`** (included inside the firmware bundle).

---

### 4️⃣ Dismiss the startup error
When the updater opens, it might show an error pop-up — just click **“OK”**.  
This is expected and normal.

---

### 5️⃣ Put the ECU into DFU (firmware update) mode

On the ECU board, you’ll find **two buttons** labeled **BOOT** and **RESET**.

Follow these steps carefully:

1. **Press and hold** the **BOOT** button.  
2. While holding **BOOT**, **press the RESET** button once.  
3. **Release BOOT**.  

Your ECU is now in **DFU mode**.

---

### 6️⃣ Check for DFU connection

In the updater app, the grey button should change to:

> 🟩 **Update Firmware via DFU**

If the button **does not appear**, it means your computer doesn’t have the DFU drivers installed.

<details>
<summary>📦 How to install DFU drivers</summary>

1. Inside the firmware bundle, open the **`drivers`** folder.  
2. Run the driver installer and follow the instructions.  
3. **Restart your computer.**  
4. Put the ECU into DFU mode again (repeat Step 5).  
5. Reopen the updater app — the DFU update button should now appear.
</details>

---

### 7️⃣ Flash the firmware

Click **“Update Firmware via DFU”** and wait.  
Once the update completes successfully, the updater window will turn **green** ✅.

---

### 8️⃣ Load a new base map or update your TunerStudio project

After the firmware update, you can either:

- Load a **base map** compatible with the new firmware, **or**  
- Update your existing **TunerStudio** project with the new `.ini` file.

---

## 🔄 Updating the TunerStudio Project `.ini` File

1. In **TunerStudio**, go to:  
   **File → Vehicle Projects → Project Properties**

2. Under **Firmware**, click:  
   **Other / Browse**

3. Select the new **`.ini`** file located inside the firmware bundle.

4. An error pop-up might appear — click to **view the errors**.

5. Fill in any **missing base settings** manually.

---

### ✅ Done!
Your ECU firmware and project are now updated and ready to use 🎉

---

**Tip:** Keep your firmware bundle backed up for reference, and always verify the correct firmware version before flashing.
