# ♻️ RecycloLux

**A multilingual, interactive game for learning how to sort household waste in Luxembourg.**

RecycloLux turns Luxembourg's waste-sorting rules into a practical learning experience. Instead of reading a long list of disposal instructions, users practise with realistic everyday objects, choose the correct disposal route, receive immediate explanations, and review their mistakes.

The project is designed for **newcomers, children, adults, seniors, and anyone who occasionally asks: “Which bin does this actually go in?”**

**Live demo:** available through the deployment link in this repository's **About** section.

---

## Why RecycloLux?

Waste sorting can look simple until an object does not fit neatly into one category.

Can a pizza box go in paper recycling?  
What happens to aluminium foil?  
Where should batteries, medicines, electronics, corks, or paint go?  
Does a plastic flower pot belong in the yellow PMC bag?

These decisions become more difficult when:

- local rules differ from rules in another country;
- packaging contains several materials;
- special collection points are required;
- rules have changed over time;
- official information is distributed across different services and websites;
- residents are unfamiliar with Luxembourg's waste system.

RecycloLux addresses this through **learning by doing**.

---

## ✨ Main features

### 🎮 Interactive sorting game

Players are shown everyday waste items and choose the appropriate disposal route.

Each item includes:

- a visual representation;
- a short description;
- a sorting category;
- an explanation after answering;
- an optional hint;
- difficulty and audience metadata.

The current dataset contains **91 real-world waste items**.

---

### 👶🧑👴 Different audiences

The game can adapt its item pool for:

- **Children** — age 12 and under
- **Adults** — age 13–64
- **Seniors** — age 65+

Some objects are shared across all audiences, while others are reserved for users for whom they are more relevant.

This allows the same knowledge base to support different learning contexts.

---

### 🌱🔥⚡ Three difficulty levels

**Beginner**

Common and relatively straightforward household objects.

**Advanced**

More ambiguous or easily confused waste items.

**Expert**

The broadest item pool with additional time pressure.

Players can choose:

- **10 items** — short session
- **30 items** — extended session
- **Endless mode**

---

## 🌍 Four languages

RecycloLux currently supports:

- 🇬🇧 English
- 🇫🇷 Français
- 🇩🇪 Deutsch
- 🇱🇺 Lëtzebuergesch

The language can also be changed while playing.

The multilingual design is especially important in Luxembourg, where residents may encounter environmental information in several languages.

---

## 🔍 Waste search

Not sure about an object?

The **Search** function allows users to look through the knowledge base without starting a game.

Search results provide:

- the recommended disposal route;
- a short explanation;
- relevant preparation instructions where applicable;
- information about special collection when an ordinary household bin is not appropriate.

Examples include items such as:

- plastic packaging;
- glass;
- paper and cardboard;
- food waste;
- batteries;
- electronic waste;
- medicines;
- hazardous household materials.

---

## 💡 Learning, not just scoring

The objective of RecycloLux is not simply to reward correct answers.

Every decision is an opportunity to understand **why** an object belongs in a particular waste stream.

The game therefore includes:

- contextual hints;
- explanatory feedback;
- score and progress indicators;
- lives;
- timed challenges at higher difficulty;
- a final review of incorrectly sorted items.

Users can return to the objects they found difficult rather than only seeing a final numerical score.

---

## 🚩 Disagree with an answer?

Waste rules can change, and individual cases can be ambiguous.

RecycloLux includes a reporting workflow so users can flag an answer they believe is incorrect.

Reports can help identify:

- outdated information;
- ambiguous items;
- changes in official guidance;
- explanations that need clarification.

The aim is to treat the knowledge base as something that can be reviewed and maintained rather than as a permanently fixed list.

---

## 🔎 Missing-item feedback

If a user searches for an object that is not yet covered, the application may anonymously record the missing search term.

This helps identify which waste items should be added next.

The feature is intended for **knowledge-base improvement**, not user profiling.

---

## 🔒 Privacy

RecycloLux is designed to collect as little personal information as possible.

The application does not require:

- an account;
- a name;
- an email address;
- location information;
- advertising identifiers;
- tracking cookies.

There is no advertising or behavioural tracking.

Unknown-item searches are intended to be collected anonymously only for improving coverage of the waste-item dataset.

---

## 📚 Knowledge base

The waste-sorting information in RecycloLux is based on guidance from relevant Luxembourg waste-management sources, including:

- **Valorlux**
- **Ville de Luxembourg**
- **SuperDrecksKëscht**

The dataset converts this guidance into structured records suitable for:

- game questions;
- multilingual explanations;
- search;
- difficulty selection;
- age-specific item pools;
- correction and maintenance workflows.

RecycloLux is an **independent educational project**, not an official service of these organisations.

Waste collection arrangements can change. Where there is any uncertainty, users should verify current instructions with the relevant municipality or official waste-management service.

---

## 🧠 Data model

Each waste item is represented as structured data containing information such as:

```text
id
name
description
hint
waste category
difficulty level
audience group
special disposal type
multilingual explanation
visual representation
```

The same structured record can therefore support both the game and the search interface.

Special disposal types can represent cases such as:

```text
battery
medication
bulky waste
hazardous waste
electronic waste
textiles
```

This structure also makes it possible to expand the project without redesigning the interface for every new item.

---

## 🛠️ Technology

RecycloLux is intentionally lightweight.

The current implementation uses:

- **HTML**
- **CSS**
- **Vanilla JavaScript**
- inline structured item data
- inline SVG illustrations

The application is currently implemented as a compact browser-based project centred on `index.html`.

There is no frontend framework required to run the main interface.

This makes the project easy to:

- inspect;
- modify;
- deploy;
- fork;
- use as a small educational prototype.

---

## 🚀 Run locally

Clone or download the repository and open:

```text
index.html
```

in a modern browser.

For development, you can also serve the directory with any lightweight local HTTP server.

For example:

```bash
python3 -m http.server 8000
```

Then open the local address shown by the server.

---

## 📁 Current repository structure

```text
recyclo-lux/
│
├── index.html
└── README.md
```

The application logic, styles, interface, item pool, and SVG item illustrations are currently kept together in the main HTML file.

A future version could separate these into modules as the project grows.

---

## 🗺️ Possible future development

Potential extensions include:

- expanding the waste-item knowledge base;
- improving Luxembourgish translations;
- separating item data from application logic;
- municipality-specific guidance;
- accessibility testing;
- additional educational modes;
- classroom or teacher-oriented functionality;
- statistics about commonly misunderstood waste items;
- improved moderation of correction reports;
- versioning of sorting rules when official guidance changes;
- open structured-data export of the knowledge base.

---

## 🎯 Project philosophy

RecycloLux is an experiment in translating **structured public knowledge into an interactive learning system**.

The project combines:

**official guidance**  
→ **structured data**  
→ **multilingual explanations**  
→ **interactive decisions**  
→ **feedback**  
→ **knowledge-base improvement**

Rather than treating a public-information website as something users simply read, RecycloLux explores how people can **learn a rule system through interaction**.

---

## ⚠️ Disclaimer

RecycloLux is an educational project.

Although the knowledge base is built from official guidance, waste-management rules, collection systems, and accepted materials may change.

For important or unusual disposal decisions—particularly hazardous waste, electronic waste, medicines, chemicals, or municipality-specific collection arrangements—always consult the latest official guidance.

---

## 👤 Author

**Wanshu Zhang**

PhD researcher at the Luxembourg Centre for Contemporary and Digital History (C²DH), University of Luxembourg.

Research interests include digital history, computational linguistics, LLM evaluation, information networks, knowledge representation, and user-facing digital systems.

---

## 📄 License

A license has not yet been specified in this repository.

Before encouraging redistribution, modification, or reuse, add an explicit open-source license appropriate to the intended use of the project.
