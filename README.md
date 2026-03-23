# L2M Auto (Lineage2M)

Windows helper for **Lineage2M**: auto dance / heal / assist macros and an optional **PvP / safety monitor** that reads your HP from the game window.

## What you need

| Item | Notes |
|------|--------|
| **Windows 10 or 11** | 64-bit |
| **`L2M_Auto.exe`** | Main app — run this |
| **`l2m_vision.exe`** | HP monitor — must sit in the **same folder** as `L2M_Auto.exe` |

No Python or AutoHotkey install is required for this build.

Prebuilt binaries are in the **`dist/`** folder. Copy **both** `.exe` files from `dist/` into whatever folder you want to run from (they must stay together).

## First run

1. Put **`L2M_Auto.exe`** and **`l2m_vision.exe`** in the same folder (keep them together).
2. Double-click **`L2M_Auto.exe`**.
3. If Windows asks for **Administrator** access, choose **Yes** (needed so keys can reach the game window).
4. In **Target Window**, pick your Lineage2M window (use **Refresh** if it’s not listed).
5. Wait until the status shows something like **Ready – HP bar detected** (the monitor uses your on-screen HP bar).

## Main features

### Auto Dance, Heal, Assist

- Set your in-game hotkeys in the fields (Dualblade, Main Weapon, Group Heal, Assist Leader).
- Set **Buff Time**, **Heal Interval**, and **Assist Interval** (decimals allowed, e.g. `0.5`, `1.25`).
- Use the checkboxes to enable or disable each feature.
- Click the big buttons or use the hotkeys below to start/stop.

### PvP / safety monitor (optional)

- **Fight Back** — when HP drops below **Fight below (%)**, the script can press your **Fight Key** to retaliate.
- **Auto Escape** — when HP drops below **Escape below (%)**, it runs your **Escape Keys** in order (comma-separated, e.g. `5,b`).
- **AutoHunt Key** — used to resume auto-farming after a fight when HP is safe again.

Click **Start Monitor (F5)** to turn the HP watcher on; click again (or close the app) to stop it.

While the monitor is on, Windows may show a **yellow border** around the captured game window — that’s normal and means capture is active. It should go away when you stop the monitor or close **`L2M_Auto.exe`**.

## Hotkeys

| Key | Action |
|-----|--------|
| **F2** | Toggle Auto Dance |
| **F3** | Toggle Auto Heal |
| **F4** | Toggle Auto Assist |
| **F5** | Toggle PvP / HP monitor |

## Settings files

Settings are saved next to the executables as **hidden** `.ini` files (e.g. per-character config based on the window title). You can back up or delete them to reset.

## Troubleshooting

| Problem | What to try |
|---------|-------------|
| HP shows `--` or monitor won’t start | Make sure **`l2m_vision.exe`** is in the same folder as **`L2M_Auto.exe`**, then pick the correct game window and **Refresh**. Ensure the HP bar is visible on screen. |
| Keys don’t reach the game | Run **`L2M_Auto.exe`** as **Administrator** and keep the game window selected in the dropdown. |
| Yellow border won’t go away | Fully close **`L2M_Auto.exe`** (vision stops with it). If something still looks stuck, end **`l2m_vision.exe`** in Task Manager, then restart. |

## Disclaimer

This tool is for personal use. Using automation may violate the game’s terms of service. Use at your own risk.
