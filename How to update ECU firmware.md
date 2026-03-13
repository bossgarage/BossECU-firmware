# 🔧 How to Update BossECU / Honduino ECU

## ⚠️ Before You Start

Make sure the ECU is **not connected to the vehicle** during the firmware update process.

---

## ⚙️ Step-by-step Instructions

### 1️⃣ Disconnect the ECU from the vehicle

Unplug the ECU from the car before starting the update process.

---

### 2️⃣ Save your current tune

Open your project and **save the current `.msq` file** to your **desktop**.
This will serve as a backup of your current tune.

---

### 3️⃣ Download the latest firmware

Download the latest firmware package from:

[https://content.epicefi.com/firmware/](https://content.epicefi.com/firmware/)

Inside the latest folder, **choose the correct firmware depending on your ECU model**:

* **BossBrain_F427**
* **BossECU_48**
* **uaefi**

Using the wrong firmware will prevent the ECU from operating correctly.

---

### 4️⃣ Connect to the ECU and backup the tune

Open **TeraFlash**:

[https://content.epicefi.com/teraflash/](https://content.epicefi.com/teraflash/)

Connect to the ECU and **create a backup of the current firmware** before updating.

---

### 5️⃣ Flash the new firmware

In **TeraFlash**:

1. Select the **`.bin` firmware file** you downloaded.
2. Click **Flash**.
3. Wait until the flashing process finishes.

---

### ⚠️ If the ECU fails to connect

If TeraFlash cannot connect to the ECU, you may need to place the ECU into **DFU (Device Firmware Update) mode**.

#### Entering DFU Mode

On the ECU board there are two buttons: **BOOT** and **RESET**.

Follow these steps:

1. **Press and hold** the **BOOT** button.
2. While holding **BOOT**, **press RESET once**.
3. **Release BOOT**.

The ECU is now in **DFU mode**.

Reconnect and retry the firmware flashing process.

---

### 6️⃣ Create a new project with the new firmware

After flashing the firmware:

1. Create a **new project** using the **new `.ini` file** from the firmware package.
2. When connecting to the ECU, if prompted about which tune to load, select:

> **Read from Controller**

---

### 7️⃣ Load your previous tune

Open the `.msq` file that you saved earlier on the **desktop**.

---

### 8️⃣ Resolve any configuration conflicts

If any errors appear while loading the old tune:

* The message will usually indicate **which table is causing the conflict**.
* Most commonly this happens in **axis values**.

Example of an incorrect axis:

```
0 1 1 3 4 5
```

Correct version:

```
0 1 2 3 4 5
```

Adjust the values until the project loads **without errors**.

---

### 9️⃣ Restart the ECU

Once everything loads correctly:

1. **Restart the ECU**
2. **Disconnect it**
3. **Reconnect it to the car**

---

### ✅ Done!

Your ECU firmware is now updated and your previous tune has been restored.

---

💡 **Tip:** Always keep a backup of your `.msq` and `.bin` files before performing any firmware update.
