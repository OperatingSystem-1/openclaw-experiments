# OpenClaw Experiments

Experiments with [OpenClaw](https://openclaw.ai) for running 24/7 AI agent teams at low cost.

## Inspiration

Based on Ziwen's viral article: **"How to Run a 24/7 AI Company with OpenClaw for $50/Month"**

> "I spent 100 hours and $1,000 learning the hard way: complexity is expensive. Most people think you need a $500 - $1,000 per month API budget to run an autonomous AI team."

**Source:** [x.com/ziwenxu_/status/2023610499024171077](https://x.com/ziwenxu_/status/2023610499024171077)

---

## Key Strategies from the Article

### 1. The Elite Squad Rule

Reduce agent count to a lean, 2-agent highly managed team instead of many loosely coordinated agents.

**Why it works:**
- Fewer agents = less coordination overhead
- Each agent can be individually optimized
- Easier to debug failures
- Lower API costs

### 2. Local Model Offloading

Use LM Studio with local models (e.g., Qwen 3, Gemma 3) on OpenClaw for:
- "Heartbeats" (constant check-ins)
- Repetitive tasks
- Simple classification

**Reserve premium cloud models** (Claude, GPT-4) for:
- Complex reasoning
- Critical decision-making
- Novel problems

This avoids API rate limits and dramatically reduces costs.

### 3. One Task Per Agent Rule

Assign only **one task at a time** per agent.

**Benefits:**
- Reduces failures from context confusion
- Clear accountability
- Easier to retry failed tasks
- Better logging/debugging

### 4. "Freshman" Management

Provide comprehensive, ground-up instructions to agents, **assuming no prior project context**.

Treat every agent like a new hire on their first day:
- Explicit step-by-step instructions
- No assumptions about what they "should know"
- Include all relevant context in the prompt
- Define success criteria clearly

### 5. Scaling Up (The Emergency Valve)

When you add more agents, the "Heartbeats" (constant check-ins) will start eating your rate limits.

**Solution:** Scale horizontally with local models handling heartbeats, while cloud models only handle escalated complex tasks.

---

## What is OpenClaw?

OpenClaw (338k+ GitHub stars) is an open-source personal AI assistant that:

- **Runs anywhere** — Any OS, any platform
- **Connects to chat apps** — WhatsApp, Telegram, Discord, or any chat app
- **Actually does things** — Clears inbox, sends emails, manages calendar, checks in for flights
- **Persistent memory** — Remembers context across sessions
- **Background automation** — Cron jobs, reminders, heartbeats
- **Self-hackable** — Can build and extend itself
- **Local-first** — Your data stays on your machine

---

## Cost Breakdown

| Approach | Monthly Cost |
|----------|-------------|
| Naive (all cloud APIs) | $500 - $1,000+ |
| Optimized (Ziwen's method) | ~$50 |

**Savings come from:**
1. Local models for repetitive work (free after hardware)
2. Fewer agents (less coordination overhead)
3. One-task-at-a-time (fewer failures/retries)
4. Better prompts (less back-and-forth)

---

## OpenClaw Ecosystem

| Repo | Description | Stars |
|------|-------------|-------|
| [openclaw/openclaw](https://github.com/openclaw/openclaw) | Main assistant | 338k |
| [openclaw/clawhub](https://github.com/openclaw/clawhub) | Skill directory | 7k |
| [openclaw/skills](https://github.com/openclaw/skills) | Archived skills | 3.5k |
| [openclaw/acpx](https://github.com/openclaw/acpx) | Agent Client Protocol CLI | 1.6k |
| [openclaw/lobster](https://github.com/openclaw/lobster) | Workflow shell | 957 |

---

## Setup

```bash
# Install OpenClaw
npm install -g openclaw

# Initialize
openclaw init

# Start the assistant
openclaw start
```

### Local Model Setup (LM Studio)

1. Download [LM Studio](https://lmstudio.ai/)
2. Install a local model (Qwen 3 or Gemma 3 recommended)
3. Start the local server
4. Configure OpenClaw to use local model for heartbeats

---

## Experiment Roadmap

### Phase 1: Basic Setup
- [ ] Install and configure OpenClaw
- [ ] Set up local model in LM Studio
- [ ] Configure heartbeat routing to local model
- [ ] Measure baseline costs

### Phase 2: Elite Squad Implementation
- [ ] Design 2-agent architecture
- [ ] Define agent specializations
- [ ] Implement one-task-at-a-time queue
- [ ] Add comprehensive prompting ("Freshman" style)

### Phase 3: Cost Optimization
- [ ] Track API usage by task type
- [ ] Identify more tasks to offload locally
- [ ] Optimize prompt lengths
- [ ] Target <$50/month operation

### Phase 4: Integration with Mitosis
- [ ] Compare OpenClaw patterns vs native OS/1 approach
- [ ] Identify portable strategies
- [ ] Document integration opportunities

---

## Related Projects

- [Mitosis Labs](https://mitosislabs.ai) — Agent replication platform
- [OS/1 Research](https://github.com/pj-cmyk/os1-research) — Research repo
- [OpenClaw Website](https://openclaw.ai) — Official site
- [OpenClaw GitHub](https://github.com/openclaw/openclaw) — Source code

---

## References

- **Original Article:** [How to Run a 24/7 AI Company with OpenClaw for $50/Month](https://x.com/ziwenxu_/status/2023610499024171077) by [@ziwenxu_](https://x.com/ziwenxu_)
- **Published:** February 17, 2026
- **Engagement:** 3,500+ likes, widely shared

---

## License

MIT
