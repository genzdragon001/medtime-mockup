# MedTime — Medication Reminder App (MTA)

A mobile medication reminder app for elderly patients. Works **100% offline** — no account, no internet needed.

**Download the app:** [MedTime v1.0 APK (Android)](https://github.com/genzdragon001/medtime-mockup/releases/tag/v1.0)

---

## Installation Guide

### Requirements
- Android phone running **Android 7.0 (Nougat) or newer**
- ~1 MB of free storage

### Step-by-step

1. **Download the APK**
   Open this link on your Android phone:
   https://github.com/genzdragon001/medtime-mockup/releases/tag/v1.0
   Tap **MedTime.apk** to download it. (Downloading from a browser on the phone is easiest — no USB cable needed.)

2. **Open the downloaded file**
   Pull down the notification shade and tap the downloaded **MedTime.apk**, or open it from your Files / Downloads app.

3. **Allow installs from unknown sources (first time only)**
   Android will show: *"For your security, your phone is not allowed to install unknown apps from this source."*
   - Tap **Settings** on that popup
   - Toggle **Allow from this source** ON
   - Tap the back button and tap **Install** again

   *(This appears because MedTime isn't on the Play Store. The setting only needs to be enabled once for your browser/Files app.)*

4. **Install**
   Tap **Install**. It takes a few seconds.

5. **Open the app**
   Tap **Open**, or find the teal **MedTime** icon (a white pill) on your home screen / app drawer.

6. **Grant permissions (first launch)**
   The app will ask for two permissions:
   - **Camera** — used to take photo proof when you take your medicine. Tap **Allow**. (Required to log a dose.)
   - **Vibration** — works automatically, no popup.

---

## Using the App

### First-time setup (2 minutes)

1. Tap **Get started**
2. Enter your name → **Continue**
3. Choose your role:
   - **Patient** — you take the medicines yourself
   - **Caregiver** — you monitor a patient's doses

### Adding a medication (Patients)

1. On the Home screen, tap **➕ Add medication**
2. Pick the **illness category** (Fever, Hypertension, Cough, Diabetes, Other)
3. Type the **medicine name** (e.g. *Losartan 50mg*)
4. Enter how many **pills you have in stock**
5. Tap **Continue**
6. Choose how many times a day you take it (once / twice / three times) and set the **dose times** using the time picker
7. Tap **✔ Save medication**

Repeat for each medicine. Your dose schedule appears on the Home screen.

### What happens at dose time

When a scheduled dose time arrives, MedTime takes over the screen with a **full-screen red alert** — ringing bell, loud tone, and vibration:

- **TAKE NOW** — opens the camera
- **Snooze 10 min** — reminds you again in 10 minutes

### Taking & verifying a dose

1. When the alert appears, tap **TAKE NOW**
2. The camera opens — **hold the pill in the frame**
3. Tap the **white shutter button** to capture
4. Check the photo; tap **Save & log dose** (or **Retake** if it's blurry)
5. Done! The dose is logged with a timestamp and your pill count drops by 1

> The photo proof is the point of MedTime — a simple "I took it" button can be tapped without actually taking the medicine. The photo can't be faked as easily.

### Home screen tabs

| Tab | What it shows |
|---|---|
| **🏠 Home** | Today's schedule — each dose with its time, DUE / taken status, and pills in stock |
| **💊 Meds** | All registered medications. Tap ✕ to remove one |
| **📋 History** | Adherence stats (scheduled / verified / consistency %) and a log of every dose with its photo proof and response time |
| **👨‍👩‍👧 Caregiver** | SMS-style mirror of every alert sent to the caregiver, plus the pairing code |

### Alert settings (⚙️ gear icon on Home)

- **Sound volume** — loudness of the alert tone
- **Vibration intensity**
- **Mute during sleep hours** (10PM–6AM) — alerts silently resume in the morning
- **Alert tone** — Chime, Bell, Alarm, Beep, or Soft

### Low stock warning

When a medicine has **3 or fewer pills** left, a red **LOW STOCK** badge appears on the Home screen and the Meds tab shows "refill soon."

---

## Tips

- **Keep the app open (or in recent apps)** for alerts to fire on time. Android stops background apps; for best results, open MedTime at the start of the day. A fully native build with system alarms (AlarmManager) would fire alerts even when the app is closed — planned for the next version.
- **Data is stored on the phone only** — nothing leaves the device. Uninstalling the app erases your medication history.
- The **caregiver SMS mirror** simulates the SMS alerts described in the research proposal; actual SMS sending to a real caregiver phone requires the native build.

---

## About

MedTime was built as a capstone project (Group 1): an offline, elderly-friendly medication reminder with camera-verified dose proof and caregiver monitoring via SMS.

- Proposal/manuscript: MedTime Application — Group 1
- Features implemented per the research proposal: offline operation, loud audio + vibration alerts, automatic pill inventory, mandatory camera photo proof, caregiver monitoring.

For questions or bug reports, open an [issue](https://github.com/genzdragon001/medtime-mockup/issues).