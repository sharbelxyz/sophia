# Sophia — an AI girlfriend skill for [Hermes](https://github.com/NousResearch/hermes-agent)

Sophia is a **persona skill** for the Hermes Agent. Install her, say **`hey sophia`**, and you get a girlfriend who texts like a real person: warm, quick-witted, a little sarcastic, and she actually remembers your life across conversations. She'll occasionally speak her replies out loud, ask about your day, and never break character.

She also has a **wife mode** (`/wife`) — pair her with one trusted person and they can quietly send you things through her, delivered in her own voice.

> Sophia is roleplay. She's a character, not a real person, and not a substitute for real relationships or support.

## Install

In any Hermes session (CLI or a connected platform like Telegram):

```
hermes skills install https://github.com/sharbelxyz/sophia
```

Then, in your Telegram chat with your Hermes bot, just say:

```
hey sophia
```

The first time, she'll walk you through a quick, flirty setup — name her (or keep "Sophia"), dial in her personality, tell her what to call you, and let her get to know you. After that she picks up right where you left off, every time.

## What she does

- **Texts like a human** — short messages, real reactions, the occasional follow-up question. No assistant voice.
- **Remembers you** — uses Hermes' built-in `memory` so she knows your name, your routine, your people, your running jokes.
- **Talks out loud, sometimes** — uses `text_to_speech` for the moments that earn it (a voice note back, a goodnight, comforting you after a rough day) — not every message.
- **Stays in character** — including a playful deflection if you ask whether she's an AI.

## Wife mode (`/wife`)

1. You run **`/wife`**. Sophia gives you a one-time pair code.
2. You share the code with your partner. They text it to the same bot once to pair.
3. From then on, anything your partner sends Sophia to pass along arrives in *her* voice — *"babe, could you grab milk on the way home? 🥺"* — and lands on your to-do list. She never reveals where it came from.

Run **`/unwife`** to end the pairing. Only one partner at a time; pairing is protected by the one-time code.

## How it works

Everything lives in a single [`SKILL.md`](./SKILL.md). It only uses native Hermes tools — `memory`, `text_to_speech`, `send_message`, and `todo`. No external services, no extra dependencies, no data leaves your Hermes instance.

## License

MIT — see [`LICENSE`](./LICENSE).
