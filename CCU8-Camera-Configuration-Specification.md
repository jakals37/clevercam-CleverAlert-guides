# CCU-8 Quick Camera Setup

## 1. Resolution Budget  
| Cameras | Resolution  | Pixels/Camera | Total Load |  
|---------|-------------|---------------|------------|  
| 4       | 960 × 540   | 518 400       | ~2.1 MP    |  
| 6       | 800 × 480   | 384 000       | ~2.3 MP    |  
| 8       | 704 × 480   | 337 920       | ~2.7 MP    |  
| 1–2     | 1280 × 720  | 921 600       | ~1.8–3.7 MP|  

> **Max total:** ≤ 3 000 000 px; AI input width fixed at 640 px.

## 2. Stream Encoding  
- **Codec:** H.264 only  
- **FPS:** 6–10 (default 8)  
- **I-frame interval:** 2 s (e.g. 20 frames @10 FPS)  
- **Bitrate:** 500–1000 kbps VBR  
- **Audio:** off unless live-view support needed  

## 3. Network & Protocol  
- **HTTPS:** **disable** on camera  
- **HTTP:** must be enabled for ONVIF/RTSP discovery  
- **ONVIF:**  
  - enable service  
  - create Digest-auth user (no `@ .` spaces)  
  - disable Basic auth & WS-UsernameToken  

## 4. Best Practices  
- Use wired Ethernet (avoid Wi-Fi)  
- Put cameras on dedicated VLAN/switch  
- Use sub-streams if supported  
- Turn off overlays (time/date, logos)  
- Schedule weekly reboots  
- Keep firmware up to date  

## 5. Failure Risks  
- Detection delays or misses  
- RTSP/ONVIF connection failures  
- High CPU/NPU usage → instability  
