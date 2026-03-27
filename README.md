# OpenClaw Experiments

Experiments with [OpenClaw](https://openclaw.ai) for running 24/7 AI agent teams at low cost.

## Inspiration

Based on Ziwen's article: ["How to Run a 24/7 AI Company with OpenClaw for $50/Month"](https://x.com/ziwenxu_/status/2023610499024171077)

> "I spent 100 hours and $1,000 learning the hard way: complexity is expensive. Most people think you need a $500 - $1,000 per month API budget to run an autonomous AI team."

## What is OpenClaw?

OpenClaw (338k+ GitHub stars) is an open-source personal AI assistant that:

- Runs on any OS, any platform
- Connects to WhatsApp, Telegram, Discord, or any chat app
- Actually *does* things: clears inbox, sends emails, manages calendar, checks in for flights
- Has persistent memory across sessions
- Supports cron jobs, reminders, background tasks
- Is self-hackable - can build and extend itself
- Runs locally (your data stays yours)

## Key Repos

| Repo | Description | Stars |
|------|-------------|-------|
| [openclaw/openclaw](https://github.com/openclaw/openclaw) | Main assistant | 338k |
| [openclaw/clawhub](https://github.com/openclaw/clawhub) | Skill directory | 7k |
| [openclaw/skills](https://github.com/openclaw/skills) | Archived skills | 3.5k |
| [openclaw/acpx](https://github.com/openclaw/acpx) | Agent Client Protocol CLI | 1.6k |
| [openclaw/lobster](https://github.com/openclaw/lobster) | Workflow shell | 957 |

## Goals

1. **Cost Optimization** - Run AI teams at $50/month instead of $500-1000
2. **Multi-Agent Coordination** - Multiple OpenClaw instances working together
3. **Integration with Mitosis** - How OpenClaw patterns can enhance OS/1 agents
4. **Skill Development** - Building custom skills for specific workflows

## Setup

```bash
# Install OpenClaw
npm install -g openclaw

# Initialize
openclaw init
```

## Experiments

- [ ] Basic setup and cost analysis
- [ ] Multi-instance coordination
- [ ] Custom skill development
- [ ] Integration patterns with Mitosis agents
- [ ] Comparison: OpenClaw vs native OS/1 approach

## Related

- [Mitosis Labs](https://mitosislabs.ai) - Agent replication platform
- [OS/1 Research](https://github.com/pj-cmyk/os1-research) - Research repo

## References

- [OpenClaw Website](https://openclaw.ai)
- [OpenClaw GitHub](https://github.com/openclaw/openclaw)
- [Ziwen's Article](https://x.com/ziwenxu_/status/2023610499024171077)
