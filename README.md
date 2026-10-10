# CyberBlock Rules

Auto-updating blocklists for **CyberBlock**, my ad- and tracker-blocking browser extension. The extension reads `manifest.json` on a schedule and pulls each rule set from this repo, so new rules ship without publishing a new extension version.

| Rule set | Rules | Blocks |
|---|:---:|---|
| `ad_rules.json` | 50 | Ad networks and ad servers |
| `tracker_rules.json` | 35 | Analytics and tracking scripts |
| `popup_rules.json` | 40 | Pop-up and pop-under sources |
| `malware_rules.json` | 20 | Known malicious domains |
| `redirect_rules.json` | 12 | Forced-redirect patterns |

## How updates work

```
manifest.json  ──  version: 2026.04.15
   └─ rules → raw.githubusercontent.com/.../<rule_set>.json
```

- `manifest.json` holds the current rules `version` and the URL of each rule set.
- The extension reads the manifest to discover and download the latest rule sets.
- To release an update, edit the JSON rule files and bump `version`.

The privacy policy for the extension is in [`privacy-policy.html`](privacy-policy.html).

---

<sub>Built by <b>Mehul Gupta</b> · <a href="https://mgupta646.github.io/">Portfolio</a></sub>
