ActivityEraser ⚙️🧹

A selective Windows activity traces cleaner with a graphical interface built on Fyne. Supports three cleaning modes (Safe, Extended, Maximum), plus “log export” capability without deletion.
⚠️ Important Notice

This tool is intended for privacy and system maintenance on personal computers, test labs, or device preparation for sale. It must not be used to conceal unlawful actions, obstruct audits, or hinder investigations. Always export logs before erasing event records. See POLICY.md for details.
✨ Features

    🗂️ Shell traces cleanup: ShellBags (BagMRU/Bags), RunMRU, ComDlg32 (Open/Save MRU), Jump Lists/Recent, UserAssist

    👤 User system traces: BAM UserSettings for the current SID

    🚀 Extended modes: Prefetch/ReadyBoot/SuperFetch files, Minidump files, Event Log cleanup (with preliminary export option)

    🖥️ Fyne GUI: Mode confirmations, README, modal export progress, quick access to result folders

🧭 Modes

    🟢 Safe — Cleans only user-level traces (no Prefetch/Minidump/Event Logs)

    🟡 Extended — Includes Safe + Prefetch, ReadyBoot, SuperFetch, Minidump, AppCompat Layers

    🔴 Maximum — Includes Extended + full Event Log cleanup (plus separate log export button)

⚠️ Risks

    🐢 Clearing Prefetch/ReadyBoot may temporarily slow down initial boots or launches

    🧩 Deleting Minidump and Event Logs erases diagnostic data

    🧹 Resetting ShellBags, ComDlg32, UserAssist, Jump Lists removes navigation and recent files history

📚 License and Policy

    📄 License: MIT (see LICENSE)

    🛡️ Responsible usage policy: see POLICY.md

    🔐 Security notes: see SECURITY.md

🔧 Installation & Usage

    Requires Windows and a valid Go installation

    Run as administrator for access to HKLM, BAM, and Event Logs

    Build instructions:

go get fyne.io/fyne/v2
go get golang.org/x/sys/windows golang.org/x/sys/windows/registry
go build -o ActivityEraser.exe .

Alternatively, use the prebuilt release
