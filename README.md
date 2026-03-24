# ShidoSync
| Component  | Role                    |
| ---------- | ----------------------- |
| Agent      | Stream + execute inputs |
| Backend    | Signaling + relay       |
| Frontend   | View + capture inputs   |

```
Agent (Python) ──WebSocket──► Backend (Node.js) ◄──WebSocket── Viewer (Browser)
      │                          (signaling relay)                     │
      └────────────── WebRTC (video + audio, direct P2P) ──────────────┘
                    Control messages go back through the backend WS
```
