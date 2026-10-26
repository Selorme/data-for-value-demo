# Tell Once, Share Selectively

**A personal data vault demo: you tell once, and businesses see only what you say yes to.**

Built by students at Tampere University for an interdisciplinary project with [Demola](https://www.demola.net), as part of the *Data for Value* challenge.

👉 **Try the demo:** https://YOUR-USERNAME.github.io/tell-once-demo/

---

## The idea

Many organisations already hold information about each of us: banks, health services, phone apps, shops. People with access needs often have to explain the same things again and again, to every hotel, train company and restaurant.

This demo explores a different way:

- **Tell once.** You write down what you need in one place, your vault.
- **Share selectively.** When a business asks, an assistant called **Helmi** tells you who is asking, for what and why. You decide which pieces they see, and for how long.
- **Take it back.** You can say no to anything and end access at any time. Businesses see only what you approved, and nothing else. That includes sister businesses owned by the same company.

## Who's in the demo

Two invented personas, each with an upcoming trip:

| Persona | Access need | Trip |
| --- | --- | --- |
| **Aino Laine**, 29 | Wheelchair user | Flies to Stockholm |
| **Elina Koskinen**, 36 | Blind, travels with her guide dog Kide | Takes the train to Helsinki |

Their trips involve invented businesses: an airline or rail company, a hotel, the hotel's bistro, a concert hall and an insurer. The insurer asks for far more than it needs, so you can see what saying no looks like.

## What you can do

- **Vault app.** A simple, accessible phone-style app. Answer requests, see your data and its sources, check what each business can see, and take back access. Text size can be changed.
- **What businesses see.** Switch to the business view to see exactly what staff see, and what stays locked.
- **Admin page.** The persona, an interactive map of where the data is held, two storage setups (data stays where it is, or one server you own), test setups such as a data breach or an outage, and tools for running a study.
- **Study mode.** Participant links open straight into the vault with a short welcome, three timed tasks and a finish screen. Answers are sent to a Microsoft Form or saved as a file, then combined on the admin page.

### Participant links

Add `#vault` to the address to open participant mode, for example:

```
https://YOUR-USERNAME.github.io/tell-once-demo/#vault&persona=aino&setup=A&advice=on
```

| Setting | Values |
| --- | --- |
| `persona` | `aino` or `elina` (random if left out) |
| `advice` | `on` or `off`: whether Helmi gives advice on each request (random if left out) |
| `setup` | `A` (data stays where it is) |
| `form` | optional Microsoft Forms pre-filled link with `CODE` and `ANSWERS` placeholders |

The easiest way to make these is **8 · Run a study** on the admin page, which also makes QR codes.

## All data is invented

Every person, business, record and transaction in this demo is **synthetic**, generated for the project. No real personal data is used, stored or sent. The demo is a single HTML file that runs entirely in your browser. It has no accounts, no database and no tracking. Participant answers go only where the participant chooses to send them.

Please don't upload real participant data or survey answers to this repository.

## Accessibility

The vault app is designed to be usable with screen readers, keyboard and larger text. It has clear labels, large touch targets, high-contrast text, a choice of text size, and status messages that are announced. If something is hard to read, find or use, please tell us: that feedback is part of the study.

## Running it yourself

No install or build is needed. Download `index.html` and open it in any modern browser, or host it on any static web host such as GitHub Pages or Netlify. QR codes and loading Excel files need an internet connection.

## Project

- **University:** Tampere University
- **Partner:** Demola, *Data for Value* challenge
- **Team:** _add names_
- **Contact:** _add team email_

This is a student research prototype, not a real product.
