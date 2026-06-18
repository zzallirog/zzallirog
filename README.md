<div align="center">

<img src="./assets/wake-up-neo.svg" alt="wake up, neo — you can't trust what an agent says it did. watch the wire." width="760">

</div>

---

Any agent can tell you what it did. The catch: the same code that *acts* is the code that *writes the report* — so the report is the one record you can't use to check the act. The only honest account comes from watching the agent from a place it can't reach. The network is that place.

```
   +------------------------------------------+
   |  CLAIM   "/tmp only, https, work hours"  |
   +------------------------------------------+
        |
        |  do they match?
        v
   +------------------------------------------+
   |  TRACE   unknown host, port 4444, 04:00  |
   +------------------------------------------+

   the trace can't be rewritten. that's the one you trust.
```

Three things make the trace impossible to fake:

- **Guardrails live in the filesystem, not the prompt.** The agent runs *inside* limits it can't talk its way out of — not rules it is politely asked to follow.
- **The watch is a one-way mirror.** Every packet is recorded before it leaves; nothing the agent does reaches back to edit what was already seen.
- **It is never told when it's watched.** No blind spot to wait for — so no safe moment to cheat.

So there is nothing to lie to, and nothing to lie *with*. The moment a run drifts — a host it shouldn't reach, a port it never uses, an hour off its schedule — the metadata already holds the proof.

**[provable-observability](https://github.com/zzallirog/provable-observability)** turns that watch into a continuous, falsifiable signal: every hour, the network asserts it is still observable. The rhythm is the proof; a broken rhythm is the alarm.

---

<sub>🤝 **[claude-kit](https://github.com/zzallirog/claude-kit)** — a Claude Code starter kit built on the same instinct. Trust the trace, not the claim: run `git hash-object <file>` on both sides — same digest, same map.</sub>

