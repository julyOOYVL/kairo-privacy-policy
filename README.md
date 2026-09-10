# Quarza - Legal Website

Welcome to the official repository for **Quarza**, the personal-finance app built on a single idea: *your time becomes money, and your money builds your future*. Every amount in the app can also be read as hours of your own work. This repository hosts the Privacy Policy website for the app.

## About Quarza

Quarza is a multilingual, offline-first personal-finance application available in English, Spanish, French and Chinese. It runs entirely on the device: no account, no sign-up, and no internet connection required. Its main features include:

### 1. Your time, priced

* Your real hourly rate, not the one on the contract: taxes withheld, commuting and the cost of going to work are all subtracted.
* Any amount in the app can be flipped into hours of work with one tap.
* "What does it really cost?" — turn a price into the working hours it takes to pay for it.

### 2. Jobs and shifts

* Several jobs at once, each with its own rate, colour and pay cycle.
* Per-weekday rates, so nights, weekends and holidays are paid at what they are actually worth.
* A shift timer with an ongoing notification, plus templates and quick-hours entry for the shifts you repeat.
* The rate is frozen onto each shift when you log it: changing a job's rate never rewrites your history.

### 3. Payslip verification

* Enter the gross and net figures from your payslip and compare them with what you actually worked.
* The app tells you what it expected, what the difference is, and what percentage was withheld.
* Pay cycles that do not start on the 1st are supported, so a 14th-to-13th month works everywhere in the app.

### 4. Money

* Expenses, income and transfers, with your own categories, icons and colours.
* Accounts and their balances, debts and their payments, recurring expenses.
* Balances are always calculated, never stored: what you see is the sum of what you entered.
* Generated is not received — a shift is money you earned, not money that reached your account, and the app keeps the two apart.

### 5. The future

* Savings goals with their target date, and the money you allocate to each one.
* Debt tracking with the real remaining balance.
* Scenarios and an emergency-fund view.

### 6. Statistics and observations

* Month-by-month charts of income against expenses, hours worked and savings rate.
* Plain-language observations: more hours for less money, a payslip that falls short, a rate that changed.

### 7. Your data stays yours

* Full JSON backups and CSV export to any spreadsheet.
* Restore from a backup, and a one-action wipe of everything.
* Optional app lock with biometrics, and an optional daily reminder.

## Repository Purpose

This repository contains the static website for Quarza's Privacy Policy. The website is hosted on GitHub Pages and provides a public link to comply with Google Play Store and App Store requirements.

## Publishing on GitHub Pages

The site is a single static file, so there is no build step:

1. Create a public repository and push `index.html` and this `README.md` to the default branch.
2. In the repository, open **Settings → Pages**.
3. Under *Build and deployment*, choose **Deploy from a branch**, select your default branch and the `/ (root)` folder, and save.
4. After a minute the page is live at `https://<your-user>.github.io/<repository>/`.
5. Paste that URL into the *Privacy Policy* field of the Google Play Console and App Store Connect listings.

`index.html` must stay at the repository root and keep that exact name: GitHub Pages serves it as the index of the site.

## Maintaining This Page

`index.html` is fully self-contained: all CSS, SVG and JavaScript are inline, and there is nothing to build or install. A few things worth knowing before editing it:

* **The content is duplicated in two language blocks** (`data-lang="en"` and `data-lang="es"`). Any change must be made in **both**, or the two versions will stop saying the same thing.
* Section `id`s are prefixed by language (`en1`, `es1`, …) because both blocks live in the same document and no two elements may share an `id`.
* Update the "Last updated" date whenever the content changes — in both languages.
* **Section 5 covers the 30-day trial and the one-time purchase.** If the pricing model ever changes — a subscription, a different trial length, a second product — that section and the app's store listing have to change with it.
* The palette is taken from the app's own dark theme (`src/ui/theme/theme.ts`): amber is time, green is money generated. If the app's colours move, move these too.
* The only external resource is the Google Fonts stylesheet. Everything else, including every icon, is inline SVG.

## What the policy actually claims

These statements are load-bearing: if the app ever stops being true to them, the policy is wrong and has to be corrected before the next release.

* The app makes **no network requests of its own**. The only outbound traffic is the store, and only when buying or restoring a purchase.
* There is **no analytics, advertising or social SDK** of any kind.
* The app **never asks for bank credentials** and has no connection to any financial institution.
* It does **not** access location, contacts, camera, microphone, calendar or photos.
* The only data that can outlive an uninstall are the two trial dates kept in the system keychain.

## Contact

For questions regarding this repository or the app, please contact:

📧 Email: [julioponsdev777@gmail.com](mailto:julioponsdev777@gmail.com)

*Note: This repository only contains the legal website, not the app code.*
