# Browser Privacy Audit – EFF Cover Your Tracks

**Course:** Cybersecurity Portfolio  
**Tool used:** [EFF Cover Your Tracks](https://coveryourtracks.eff.org)  
**Date:** June 2026

---

## Objective

Test how trackable my default browser is using the EFF's Cover Your Tracks tool, then apply mitigations and re-test to demonstrate measurable improvement.

---

## Before – Google Chrome (default, with McAfee WebAdvisor)

**Result: Not protected against tracking**

| Check | Result |
|---|---|
| Blocking tracking ads? | ❌ No |
| Blocking invisible trackers? | ❌ No |
| Fingerprint protection? | ❌ Unique fingerprint |

**Fingerprint score:** 18.41 bits of identifying information — unique among 349,076 browsers tested in the past 45 days.

### Observations
- Edge with default settings offered zero tracker or ad blocking.
- McAfee WebAdvisor was active but provided no privacy benefit — it only flagged potentially dangerous sites, not trackers.
- A unique fingerprint means any website could identify and track this browser across sessions without using cookies, making cookie-clearing ineffective as a privacy measure.

---

## Mitigation Applied

**Switched to Brave Browser** (default settings, no extensions added)

Brave was chosen because it includes built-in:
- Shield blocking for ads and trackers
- Fingerprint randomization (changes fingerprint per session/site)
- No need for third-party extensions

---

## After – Brave Browser (default settings)

**Result: Strong protection against web tracking**

| Check | Result |
|---|---|
| Blocking tracking ads? | ✅ Yes |
| Blocking invisible trackers? | ✅ Yes |
| Fingerprint protection? | ✅ Randomized fingerprint |

**Fingerprint score:** Randomized — browser cannot be uniquely identified across sites.

---

## Summary

| Metric | Edge + McAfee | Brave (default) |
|---|---|---|
| Tracking ad blocking | ❌ | ✅ |
| Invisible tracker blocking | ❌ | ✅ |
| Fingerprint protection | ❌ Unique (18.41 bits) | ✅ Randomized |
| Overall verdict | Not protected | Strong protection |

---

## Key Takeaways

- **Default browser settings are insufficient** for privacy — even with a security extension like McAfee WebAdvisor active.
- **Browser fingerprinting** is a tracking method that survives cookie deletion. It works by combining browser attributes (user agent, screen size, fonts, timezone, etc.) into a near-unique profile.
- **Brave's fingerprint randomization** defeats this by returning slightly different values each time, making cross-site tracking unreliable.
- Switching browsers — without installing any extensions — was enough to go from 0/3 to 3/3 on the EFF's test.

---

## References

- [EFF Cover Your Tracks](https://coveryourtracks.eff.org)
- [Brave Browser](https://brave.com)
- [What is browser fingerprinting? – EFF](https://coveryourtracks.eff.org/learn)
