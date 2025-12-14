# Task Desk - Final Legal Documents & Implementation

**Developer:** Jaka Kavčič  
**Bundle ID:** jakakavcic.taskdesk

---

## 📦 Package Contents

### Legal Documents (Word - for your records)
- `Privacy_Policy_TaskDesk.docx`
- `Terms_of_Service_TaskDesk.docx`
- `EULA_TaskDesk.docx`

### Web Files (HTML - host these online)
- `privacy-policy.html`
- `terms-of-service.html`
- `eula.html`

### Code
- `SettingsView.swift` - Complete Settings screen with tips

---

## 🚀 Setup Instructions

### Step 1: Host Legal Documents on GitHub Pages (Free)

1. Go to [github.com](https://github.com) and create a new repository called `taskdesk-legal`

2. Upload the 3 HTML files:
   - `privacy-policy.html`
   - `terms-of-service.html`
   - `eula.html`

3. Go to repository **Settings** → **Pages**

4. Under "Source", select **main** branch and click **Save**

5. Your URLs will be (replace `yourusername` with your GitHub username):
   ```
   https://yourusername.github.io/taskdesk-legal/privacy-policy.html
   https://yourusername.github.io/taskdesk-legal/terms-of-service.html
   https://yourusername.github.io/taskdesk-legal/eula.html
   ```

6. **Update** `LegalURLs` in `SettingsView.swift` with your actual URLs

---

### Step 2: Set Up Tips in App Store Connect

1. Log in to [App Store Connect](https://appstoreconnect.apple.com)

2. Go to your app → **Monetization** → **In-App Purchases**

3. Create 4 **Consumable** products:

| Reference Name | Product ID | Price |
|---------------|------------|-------|
| Small Tip | `jakakavcic.taskdesk.tip.small` | €0.99 |
| Medium Tip | `jakakavcic.taskdesk.tip.medium` | €2.99 |
| Large Tip | `jakakavcic.taskdesk.tip.large` | €4.99 |
| Huge Tip | `jakakavcic.taskdesk.tip.huge` | €9.99 |

4. For each product, fill in:
   - **Type:** Consumable
   - **Display Name:** Small Tip ☕️ (etc.)
   - **Description:** Support Task Desk development
   - **Screenshot:** Take screenshot of Tip Jar in your app

---

### Step 3: Xcode Setup

1. Add **In-App Purchase** capability:
   - Select your target → Signing & Capabilities → + Capability → In-App Purchase

2. Add `SettingsView.swift` to your project

3. Update `LegalURLs` with your GitHub Pages URLs

---

### Step 4: App Store Connect - App Information

1. Go to **App Information**

2. **Privacy Policy URL:** Enter your hosted URL:
   ```
   https://yourusername.github.io/taskdesk-legal/privacy-policy.html
   ```

3. **App Privacy** (Nutrition Labels):
   - When asked "Do you collect data?" → Select **No**
   - (Since Task Desk doesn't collect any user data)

---

### Step 5: Testing Tips

**Option A: StoreKit Testing (Simulator)**

1. File → New → File → StoreKit Configuration File
2. Name it `Tips.storekit`
3. Add your 4 products
4. Edit Scheme → Run → Options → StoreKit Configuration → Select your file
5. Test in Simulator

**Option B: Sandbox Testing (Real Device)**

1. App Store Connect → Users and Access → Sandbox → Testers
2. Create a test account with real email
3. On device: Settings → App Store → Sign Out
4. In app, purchase will prompt for Sandbox login

---

## ✅ Pre-Submission Checklist

- [ ] HTML files hosted on GitHub Pages
- [ ] URLs updated in `SettingsView.swift`
- [ ] Privacy Policy URL added in App Store Connect
- [ ] 4 tip products created in App Store Connect
- [ ] In-App Purchase capability added in Xcode
- [ ] App Privacy questionnaire completed (No data collected)
- [ ] Tips tested with Sandbox account

---

## 📱 Info.plist Keys

Add these to your Info.plist:

```xml
<key>NSLocationWhenInUseUsageDescription</key>
<string>Task Desk uses your location to provide context-aware task suggestions. Your location stays on your device and is never shared.</string>

<key>NSCalendarsUsageDescription</key>
<string>Task Desk needs calendar access to sync your tasks with calendar events.</string>
```

---

## 📧 Contact Info (in documents)

**Jaka Kavčič**  
Gallusovo nabrežje 7  
1000 Ljubljana, Slovenia  
kavcic.jaka@hotmail.com

---

All documents are final and ready to use. Good luck with Task Desk! 🚀
