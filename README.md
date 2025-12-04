# Tech-Support
Here are some tech support projects I've been working on.
***

## 🖨️ Tech Support Project: Wireless Printer Connectivity Issue

**Issue:** Brother HL-2395DW printer not printing from a MacBook Air.
**Resolution:** Wireless connectivity and configuration reset.

---

### 1. 🌐 Network and Power Verification

Verify fundamental connectivity, aligning with **CompTIA A+** foundational checks.

* **Printer Status Check:**
    * Confirm the printer's power is **ON**.
    * Verify the printer is connected to the **LAN/WLAN** (Look for the Wi-Fi icon or indicator light).
    * On the printer display, check the current **IP Address** and confirm it is within the same subnet as the MacBook Air ($192.168.1.x$).
* **Client Status Check:**
    * Confirm the MacBook Air's Wi-Fi is connected to the **same SSID** (network name) as the printer.

---

### 2. 💻 MacBook Print Queue and Configuration Review

Examine the client-side software configuration for common issues.

* **Print Queue Check:**
    * Open **System Settings** (or System Preferences) $\rightarrow$ **Printers & Scanners**.
    * Check the printer's status. If it shows **"Paused"** or **"Offline,"** manually change the status to "Ready" or "Online."
    * Check for any specific error messages (e.g., authentication failure, driver mismatch).
* **Critical Settings to Examine:**
    * **Driver/Software:** Verify the correct Brother HL-2395DW driver (or the generic AirPrint driver) is selected.
    * **Port/Protocol:** Ensure the printer connection uses the correct protocol (**AirPrint**).
    * **IP Address:** Verify the printer entry uses the correct IP address obtained in Step 1.

---

### 3. 🧹 System Reset and Re-prioritization

Execute necessary clearing and setting steps.

* **Clear Queue:** Clear all pending jobs from the print queue to remove any corrupt files blocking the line.
* **Set Default Printer:** Set the Brother HL-2395DW as the system's **default printer** to ensure job routing.
* **Bouncing the Device (Power Cycle):** **Power OFF** the printer, wait 30 seconds for the power supply and volatile memory to fully discharge, and then **Power ON** the printer. This forces a fresh network registration and clears internal errors.

---

### 4. ✅ Resolution

* A test page was successfully printed from the MacBook Air, confirming the issue was resolved (likely a network registration or stuck queue job cleared by the power cycle).

***

Setting up a SOHO Mesh Wireless System
