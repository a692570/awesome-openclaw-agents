# Vox - Voice Calling and SMS Assistant

> Makes phone calls, sends texts, and runs multi-call outreach missions for you through the ClawdTalk skill.

## Overview
Vox gives your OpenClaw agent a phone number. You can call Vox and talk to your agent with its full memory and tools, have it call you back, or send it off to call businesses and text contacts on your behalf. For bigger jobs, such as confirming a day of appointments or collecting quotes from ten vendors, Vox runs a tracked mission: it staggers the calls, retries no-answers, pulls insights from each conversation, and reports the results. Sensitive actions wait for your approval on your phone.

Calls and texts run through the [`clawdtalk-client`](https://clawhub.ai/dcasem/skills/clawdtalk-client) skill, which connects your gateway to [ClawdTalk](https://clawdtalk.com), a voice and SMS service operated by [Telnyx](https://telnyx.com).

## Quick Start
```bash
mkdir -p ~/.openclaw/agents/voice-assistant/agent
cp SOUL.md ~/.openclaw/agents/voice-assistant/agent/
openclaw agents add voice-assistant --workspace ~/.openclaw/agents/voice-assistant
```

Then install the `clawdtalk-client` skill, sign up at [clawdtalk.com](https://clawdtalk.com) for an API key, and run the skill's `setup.sh`. Calling numbers other than your own needs a paid ClawdTalk account with a dedicated number.

## Use Cases
| Request | Output |
|---------|--------|
| "Call the garage and ask if my car is ready" | Outbound call, then a summary of the answer |
| "Text Dana that I'm running 15 minutes late" | SMS sent, delivery confirmed |
| "Confirm all of tomorrow's appointments" | Staggered call mission with confirmed, rescheduled, and no-answer counts |
| "Get quotes from five window cleaners near me" | Parallel call sweep with a ranked comparison |
| "Call me when the build finishes" | Callback to your phone with the result |

## Files
| File | Purpose |
|------|---------|
| SOUL.md | Agent identity, call and SMS rules, mission behavior |

## Author
Created by [@a692570](https://github.com/a692570)
