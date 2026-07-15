# OP-Ram - The BEST RAM Booster!

A Windows utility that "doubles your RAM" with dramatic effect!  

## Features

- **Admin Required**: Auto-elevates via UAC on launch
- **Always on Top**: Main window stays visible above all others
- **Close Confirmation**: Prevents accidental closure with a confirmation dialog
- **Fake Terminals**: 6 Windows appearance with "hacker" green code that auto-disables input and closes after 1s
- **15-Second Loading**: Animated progress bar with Matrix-style terminal text
- **Registry Tracking**: Uses `HKCU\Software\OP-Ram\Used` to detect first-run vs repeat usage
- **Single-Use UI**: 
  - First run → "Success" popup: ✅ "+8GB RAM successfully added to your PC!"
  - Subsequent runs → "Failure" popup: ❌ "This offer has already been used!"

## Visual Preview

```
┌──────────────────────────────────────────────────────────────┐
│  OP-Ram                                                      ║
│  The most advanced RAM optimization tool                     ║
│                                                              ║
│  [Double your RAM? [ONE TIME USAGE]]                         ║
│                                                              ║
│  ┌──────────────────────────────┐  ┌─────────────────────┐   ║
│  │  SM-25ASMEMEM                │  │  RANDOM ACCESS      │   ║
│  │  ~0xDEC6F4                   │  │  MEMORY_ALLOCATION  │   ║
│  │  CPU: 1919MHz                │  │  PAGE_FAULT         │   ║
│  └──────────────────────────────┘  └─────────────────────┘   ║
│                                                              ║
│  Loading Memory... 92%                                       ║
└──────────────────────────────────────────────────────────────┘
```

## Build & Run, or just use the pre-compiled

```batch
REM Install Rust: https://www.rust-lang.org/tools/install
git clone https://github.com/yourname/op-ram
cd op-ram
cargo build --release
start target\release\op-ram.exe
```

## How It Works

1. **Launch** - Shows admin prompt if needed (UAC)
2. **First Run** - Clicks "Double your RAM?" writes registry key `HKCU\Software\OP-Ram\Used`
3. **Max RAM Sequence** - 
   - Triggers 6 fake terminal windows with scrolling green symbols
   - Each terminal auto-disables input (can't be interacted with)
   - Windows close automatically after ~1 second
   - Loading bar fills over 15 seconds
4. **Completion** - Dramatic success popup claims +8GB RAM added!
5. **Repeat Runs** - Shows "already used" warning with Failure popup

## Safety & Disclaimer

- **FULLY fake RAM modification tool I made troll my brother. **
- Registry key is harmless (`Windows\CurrentUser\Software\OP-Ram`)
- All spawned "terminal" windows are read-only and self-terminate
- The app is designed as a fun joke utility, not a system tool

Right-click the .exe to "Properties → Details" and you'll see the hidden admin manifest!
