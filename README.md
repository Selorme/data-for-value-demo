# Tell Once, Share Selectively

**A personal data vault demo: you tell once, and businesses see only what you say yes to.**

Built by students at Tampere University for an interdisciplinary project with [Demola](https://www.demola.net), as part of the *Data for Value* challenge.

**Try the demo:** https://selorme.github.io/data-for-value-demo/

---

## The idea

Many organisations already hold information about each of us: banks, health services, phone apps, shops. People with access needs often have to explain the same things again and again, to every hotel, train company and restaurant.

This demo explores a different way:

- **Tell once.** You write down what you need in one place, your vault.
- **Share selectively.** When a business asks, an assistant called **Helmi** tells you who is asking, for what and why. You decide which pieces they see, and for how long.
- **Send what they didn't ask for.** If something would help and the business didn't ask, you can send it yourself: a line from your profile or a short note.
- **Take it back.** You can say no to anything and end access at any time. Businesses see only what you approved or sent, and nothing else. That includes sister businesses owned by the same company.

## Who's in the demo

Eight invented personas, each with an upcoming trip:

| Persona | Needs | Trip |
| --- | --- | --- |
| **Aino Laine**, 29 | Wheelchair user | Flies to Stockholm |
| **Elina Koskinen**, 36 | Blind, travels with her guide dog Kide | Takes the train to Helsinki |
| **Sanna Mäkinen**, 36 | No disability: everyday preferences (quiet room, vegetarian, loyalty points) | Takes the bus to Turku for work |
| **Laura Heikkinen**, 34 | Travelling with her son Onni, 10 months, and a pushchair | Takes the ferry from Helsinki to Tallinn on holiday |
| **Juho Mäkelä**, 34 | Deaf, Finnish Sign Language user | Flies from Oulu to Copenhagen for a design conference and an interpreted play |
| **Ahmed Warsame**, 41 | Type 1 diabetes, insulin pump and glucose sensor | Takes the train to Jyväskylä for a training course and an ice hockey match |
| **Pekka Nieminen**, 72 | Rollator, hearing aids, heart condition on a blood thinner | Takes the night train from Lahti to Rovaniemi to visit his grandson |
| **Ravi Menon**, 23 | Autistic, with ADHD; sensitive to noise and crowds | Flies from Tampere to Oslo for a game jam and a concert |

Each trip uses a different way to travel, but every persona meets the same five kinds of place: a transport company, a hotel, the hotel's own restaurant, an event and an insurer. That makes it possible to compare sharing for a disability, a health condition, older age, a family situation and no particular need. The films in the main demo exist for the first four; the other four don't have one yet.

Their trips involve invented businesses: an airline, train, bus or ferry company, a hotel, the hotel's own restaurant, a concert or show and an insurer. The insurer asks for far more than it needs, so you can see what saying no looks like.

## What you can do

### In the vault app

A simple, accessible phone-style app. Text size can be changed, and Helmi can read every screen aloud (🔊).

- **Answer requests.** Turn on only what you want to share, and choose how long: this trip only, 30 days, or until you take it back.
- **Suggest for me.** Helmi picks the smallest set that does the job and explains each choice. For example, it leaves off whole histories and diagnoses.
- **Send something yourself.** From any business's page, pick a line from your profile or write a short note. Helmi warns you if it's health or personal information. The business sees it marked "sent by the customer", and you can take it back.
- **Helmi's tips.** Helmi notices when something would help and wasn't asked for, such as "The bistro didn't ask about Kide. Send it?", and sends it in one tap if you agree.
- **Messages.** Chat with each business. Helmi watches the chat for you:
  - if a business asks for something you've stored, Helmi offers to share it properly (logged, time-limited and easy to take back) instead of you typing it
  - if a business asks for something sensitive, such as an ID number, Helmi warns you
  - you can close a chat at any time
- **Ask Helmi.** Type or speak (🎤, in browsers that support it). Helmi answers questions about your sharing and acts when asked, always asking first. Some examples:
  - "Who can see my allergy?"
  - "What does the hotel see?"
  - "What happens if I say no to the hotel?"
  - "Can the bistro see what I gave the hotel?"
  - "Should I share my location history with the insurer?"
  - "Tell the restaurant I'll be 10 minutes late"
  - "Stop sharing with the hotel"
  - "Always share my diet"
  - "Answer my requests for me"
- **Rules.** In About me, set each line to *Ask me*, *Always share* or *Never share*. Rules fill in future requests, and a request fully covered by rules can be answered in one tap. You can also save an answer as rules.
- **See your data.** View every source and where it's kept.
- **See what each business sees.** Their exact staff screen, and everything that stays locked.
- **Sharing history.** A timeline of every share, read, blocked attempt, message and ended access, which you can filter by business.
- **Skip to after the trip.** See trip-only access end on its own, and what stays open.

### On the admin page

- **What businesses see.** Each business's staff screen next to an admin check that it can't see anything it shouldn't. Includes a business app with bookings, vault requests, messages (with quick messages) and its access log.
- **The network layer (4b).** A simulated version of Nokia Network as Code, using the shapes of the open CAMARA APIs. Some places only need a yes or a no ("Is she at the station entrance?", "Is this really her phone?"). Helmi asks the mobile network instead of sharing data. Present full screen for talks.
- **Control.** Who can see what right now, take back access, and skip to after the trip.
- **Storage setups and tests.** Data stays where it is, or one server you own. Includes test setups such as a data breach or an outage.
- **Run a study.** Participant links, QR codes, balanced and blinded participant codes, and combining answers into one CSV.

### Films

Each persona has an animated film (2:58, with narration, captions and music) showing the same trip with and without the vault, including a moment where she sends something herself. The films live in `films/` as player pages with full screen and −10 / +10 second controls.

### About Helmi's intelligence

In this prototype, Helmi's understanding is built into the page. It recognises plain requests about sharing, answers from the persona's actual data, and runs entirely in your browser, so nothing typed leaves the page. A real product would use a language model working for the person. It would send the model only the question and item names, never the data itself.

## Study mode

Participant links open straight into the vault with:

- a short welcome
- the persona's film after using the app
- three timed tasks
- a finish screen

The app assigns each participant a persona, and Helmi advice on or off, from their participant code, so the research team never chooses. Answers are sent to a Microsoft Form or saved as a file, then combined on the admin page.

Along with each answer to a request, the results record:
- what the participant sent without being asked
- how many messages they exchanged, and whether they closed a chat
- how they used Helmi: questions asked, actions confirmed, "Suggest for me" and tips
- how many rules they saved

### Participant links

Add `#vault` to the address to open participant mode, for example:

```
https://selorme.github.io/data-for-value-demo/#vault&setup=A
```

| Setting | Values |
| --- | --- |
| `persona` | `aino`, `elina`, `sanna` or `laura` (for testing; if left out, the app assigns one from the participant code) |
| `advice` | `on` or `off`: whether Helmi gives advice on big requests (if left out, assigned from the code) |
| `setup` | `A` (data stays where it is) |
| `film` | `1` to show the persona's film after the tasks |
| `form` | optional Microsoft Forms pre-filled link with `CODE` and `ANSWERS` placeholders |

The easiest way to make these is **8 · Run a study** on the admin page, which also makes QR codes.

## Workshop version: trip mode

`trip.html` is a separate, game-like version for a persona workshop, inspired by *1 in 8 billion*. It takes about 13 minutes on a phone. Since 8 November, `index.html` is the same file as `trip.html`: opened without a link ending it shows the researcher page, where **Participant mode (trip)** starts trip mode from the setup and **Business mode (run the hotel)** starts the hotel game. **Open business app** still shows what each business's front desk sees. The earlier main demo, where participant mode opened the vault app, is kept in `Old demos`.

**Try it:** https://selorme.github.io/data-for-value-demo/trip.html#trip

- **Your life.** You play one of the eight, written as "you".
- **Set up Helmi** (6 steps):
  - what it may read, from 19 or 20 sources, including the most personal: WhatsApp, Telegram and Instagram messages, email, photos, search history, a private journal, a cycle tracker, mood and therapy notes, contacts and voice recordings
  - how much it decides
  - whether it advises you
  - whether it writes messages for you (in your style if it can read your chats)
  - what it should do if it's unsure or can't reach you
  - your rules
- **The trip.** About 10 places, as a storyline. Some places, like the hotel, are the same for everyone; others are picked by your code. You also do chat tasks, get a message from home, and face things you don't control: a break-in, an accident and an insurance claim, and Helmi trying to reach you while your phone is on silent. Your choices have consequences, such as a claim refused because the insurer read your chats.
- **Your trip story.** Your trip compared with "shared nothing" and "shared everything", and a one-minute narrated replay of your trip.
- **Before and after.** You answer 24 questions about what you'd let an assistant do in your own life. After the group discussion, you answer them again on the same phone. You can also play your trip again and see both trips side by side. Answers are kept in your phone's browser under your code and sent to the research team only when you press Send.

| Link | Opens |
| --- | --- |
| `trip.html#trip` | trip mode, with a random person |
| `trip.html#trip&persona=aino` | a fixed person (`aino`, `elina`, `sanna`, `laura`, `juho`, `ahmed`, `pekka` or `ravi`) |
| `trip.html#business` | business mode: you run Hotel Merikaari and set up your booking bot |
| `trip.html#group` | the group screen for the facilitator: everyone's trips, and the before-and-after table |

Add `&form=` and an encoded Microsoft Forms pre-filled link (with `CODE` and `ANSWERS`) to send answers to a form, as in study mode.

## All data is invented

Every person, business, record, message, photo description and transaction in this demo is **synthetic**, generated for the project. No real personal data is used, stored or sent. The demo is a single HTML file that runs entirely in your browser. It has no accounts, no database and no tracking. Network checks and messages are simulated. Participant answers go only where the participant chooses to send them.

Please don't upload real participant data or survey answers to this repository.

## Accessibility

The vault app is designed to be usable with screen readers, keyboard and larger text. It has:
- clear labels and large touch targets
- high-contrast text and a choice of text size
- read-aloud
- status messages that are announced

If something is hard to read, find or use, please tell us: that feedback is part of the study.

## Running it yourself

No install or build is needed. Download `index.html` and `trip.html` (the same file), the `narration` folder (the recap voice for each person, one file each, loaded only when needed) and the `films` folder, and open them in any modern browser. You can also host it on any static web host such as GitHub Pages or Netlify.

Some features need an internet connection: QR codes, loading Excel files and the web fonts. Films play best from a web host. Speaking to Helmi needs a browser with speech recognition, such as Chrome.

## Project

- **University:** Tampere University
- **Partner:** Demola, *Data for Value* challenge
- **Team:** Ruth, Dora, Towhidul, Rui
- **Contact:** Through GitHub
