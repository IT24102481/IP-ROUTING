# lk-vpn

Route your x-ui Xray traffic through a Sri Lanka exit node.  
Your v2ray clients will see a **Sri Lanka IP** instead of your VPS IP.

## How it works

```
[Your v2ray client]
        ↓
[Your SG VPS - x-ui inbound]
        ↓
[LK Exit Node - VLESS/WS/TLS]
        ↓
[Internet — appears as Sri Lanka IP]
```

## Install

```bash
bash <(curl -Ls https://raw.githubusercontent.com/IT24102481/lk-vpn/main/lk-vpn.sh)
```

## Requirements

- Ubuntu/Debian VPS with **x-ui** already installed
- `python3` and `curl` available (default on most VPS)

## Menu Options

| Option | Action |
|--------|--------|
| 1 | Apply LK exit node to Xray config |
| 2 | Remove LK exit node (restore original config) |
| 3 | Check current exit IP |
| 4 | Restart x-ui |

## Notes

- A backup of your original config is saved before any changes
- To restore at any time, select option 2 from the menu
