# WID – Outstanding work & roadmap

**Last updated:** 18 November 2026  
**Current target:** v0.9.2 beta fixes → internal re-test → wider beta → 1.0  

**Issue tracker:** [github.com/jhaas-repo/WID-Android/issues](https://github.com/jhaas-repo/WID-Android/issues)

This document tracks **pre-production fixes**, **operational tasks**, and **planned product work**. Living list — reorder and check off as you go.

---

## 1. Pre-production fixes (from beta feedback)

Fix before wider / production confidence. Ordered by priority.

| Priority | GitHub | Issue | Notes | Status |
|----------|--------|--------|--------|--------|
| **P0** | [#15](https://github.com/jhaas-repo/WID-Android/issues/15) | **Passphrase attempt protection** | Unlimited wrong unlock attempts; add lockout / cooldown after N failures | ☐ |
| **P0** | [#11](https://github.com/jhaas-repo/WID-Android/issues/11) | **App lock restores previous screen** | After auto-lock / minimize, return to the screen the user was on; avoid losing unsaved entry work (or warn if dirty) | ☐ |
| **P1** | [#9](https://github.com/jhaas-repo/WID-Android/issues/9) | **Biometric opt-in** | Do not auto-enable biometric; prompt to enable; allow change in Settings | ☐ |
| **P1** | [#10](https://github.com/jhaas-repo/WID-Android/issues/10) | **Attachments only on Save** | Stage attachments until Save is pressed; don’t persist on pick alone | ☐ |
| **P1** | [#14](https://github.com/jhaas-repo/WID-Android/issues/14) | **Security log – settings events** | Log settings changes (theme, timeout, biometric clear, etc.) | ☐ |
| **P2** | [#8](https://github.com/jhaas-repo/WID-Android/issues/8) | **Attachments by entry type** | Decide: attachments on all types vs only where it makes sense; align UI | ☐ |
| **P2** | [#7](https://github.com/jhaas-repo/WID-Android/issues/7) | **Vault type filter** | Add entry-type filter alongside category chips | ☐ |

**Ship rule:** P0 + P1 should land in the next beta build (e.g. **0.9.2**). P2 if capacity allows.

---

## 2. Outstanding tasks (ops / release)

### Release & store

| # | Task | Notes | Status |
|---|------|--------|--------|
| 1 | Ship **v0.9.2** (beta-fix build) after P0/P1 | Bump `versionName` / `versionCode`; tester notes | ☐ |
| 2 | **Double-check app** end-to-end | Include new: lockout, lock navigation, biometric prompt, attachment save, security log | ☐ |
| 3 | **Double-check Play Store listing** | Short/full description, screenshots, feature graphic, content rating, data safety | ☐ |
| 4 | **Refine store page** where needed | Screenshots match current UI | ☐ |
| 5 | **Update Google Play Console details** | Developer name, contact email, address | ☐ |
| 6 | Confirm **privacy policy URL** | `https://therabbitsburrow.github.io/wid/privacy.html` | ☐ |

### Monetisation

| # | Task | Notes | Status |
|---|------|--------|--------|
| 7 | **Finalise paid version approach** | One-time unlock; price; free vs full limits | ☐ |
| 8 | Implement **Google Play Billing** | One-time product; replace debug premium flag | ☐ |
| 9 | Test purchase / restore on internal track | License testers; restore after reinstall | ☐ |

### Website & presence

| # | Task | Notes | Status |
|---|------|--------|--------|
| 10 | **Roadmap page on website** | Public summary — done; keep in sync with this doc | ☑ |
| 11 | **Developer blog page** | Monthly progress under `/blog/` | ☐ |
| 12 | **Add website link in app About** | Settings → About → site | ☐ |
| 13 | Contact email on privacy + beta pages | Replace any `[INSERT CONTACT EMAIL]` | ☐ |

### Docs & process

| # | Task | Notes | Status |
|---|------|--------|--------|
| 14 | Tag git releases (`v0.9.2`, etc.) | Optional but useful | ☐ |
| 15 | **Release notes** per beta build | Link fixed GitHub issue numbers | ☐ |
| 16 | Open-beta criteria | e.g. no P0 for 7 days on internal | ☐ |

---

## 3. Product roadmap (future features)

### Near future (toward / just after 1.0)

| Item | Source | Description |
|------|--------|-------------|
| **Play Billing (one-time Full unlock)** | Plan | Production entitlements; upgrade UI; restore purchases |
| **Emergency Access Kit as PDF** | Plan | Printable/shareable PDF kit for trusted contacts |
| **Single vault item → PDF share** | [#13](https://github.com/jhaas-repo/WID-Android/issues/13) | Share one entry (e.g. insurance details) as PDF for real-world needs |
| **About → Website** | Plan | Deep link from Settings |
| **Store listing polish** | Plan | Final screenshots; optional short video |
| **Stable 1.0** | Plan | Core feature freeze; critical fixes only |

### Next wave (1.x)

| Item | Source | Description |
|------|--------|-------------|
| **Richer Emergency Kit** | Plan | PDF + optional QR; owner label; branding |
| **Biometric modality options** | [#12](https://github.com/jhaas-repo/WID-Android/issues/12) | Choose which device biometrics are allowed |
| **Backup format v3** | Plan | Caps, checksums, clearer migration |
| **Security log improvements** | Plan + [#14](https://github.com/jhaas-repo/WID-Android/issues/14) | Richer events, optional export (beyond settings logging) |
| **Onboarding tweaks** | Plan | Clearer passphrase warning; tips after first entry |
| **Accessibility pass** | Plan | Font scaling, contrast, content descriptions |

### Later / larger bets

| Item | Source | Description |
|------|--------|-------------|
| **Multi-device encrypted sync** | Plan | Optional E2E/zero-knowledge sync; likely subscription; device list/revoke; offline-first when offline |
| **Multiple vaults per person** | [#16](https://github.com/jhaas-repo/WID-Android/issues/16) | e.g. personal vs business vaults on one device |
| **Share folders with different contacts** | [#18](https://github.com/jhaas-repo/WID-Android/issues/18) | Per-contact / per-folder access model (major design change) |
| **Import from phone password manager** | [#17](https://github.com/jhaas-repo/WID-Android/issues/17) | Optional import/sync from system or third-party managers (platform limits apply) |
| **iOS version** | Plan | Same threat model; large project |
| **Estate checklist templates** | Plan | Non-legal prompts/categories |
| **Independent security review** | Plan | If the product grows |

### Explicitly out of scope (for now)

- Replacing a lawyer/will  
- Guaranteed access if device is destroyed and no backup exists  
- Server-side recovery of master passphrase  

---

## 4. Suggested sequence

```
Now     →  Pre-prod P0/P1 (#15, #11, #9, #10, #14)
        →  v0.9.2 internal build + re-test
Next    →  P2 if needed (#8, #7); Billing; store/console polish
        →  Website blog + About link
Then    →  PDF Emergency Kit + optional single-item PDF (#13)
        →  1.0 when P0-free and Billing live
Later   →  Multi-device sync, multi-vault (#16), folder sharing (#18), password import (#17)
```

---

## 5. Version sketch

| Version | Intent |
|---------|--------|
| **0.9.1** | Prior beta fixes (UX, emergency reuse, backup attachments, help) |
| **0.9.2** | Pre-prod beta feedback: lockout, lock navigation, biometric opt-in, attachment save, security log |
| **0.9.x** | Billing + store polish |
| **1.0** | Stable core + one-time Full unlock |
| **1.1** | PDF kits / item share PDF |
| **2.0** | Multi-device encrypted sync and/or multi-vault / multi-platform |

---

*WID – When I Die · The Rabbit’s Burrow · Issues: jhaas-repo/WID-Android*
