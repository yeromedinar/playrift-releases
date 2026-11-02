# Playrift

Open a game on your PC, send a friend a link, and they're in. They play from
their phone, laptop or TV, wherever they are, with nothing to install and no
account to make. You don't open ports on your router, and you decide who gets
in.

This repo only holds the Windows installers. Grab the latest one here:

**[Download Playrift for Windows](https://github.com/yeromedinar/playrift-releases/releases/latest/download/Playrift_x64-setup.exe)**

> Playrift is still in development. Things break, and some of what's below
> will change.

## What happens when you share

You start a game and hit **Share** in the Playrift panel. Playrift finds the
game window on its own and gives you a link and a QR code. Paste the link in
WhatsApp, Discord, iMessage or wherever you talk. The preview already says
who's inviting and to what game.

Your friend opens it in their browser and sees the game's cover while they
wait. You get a notification, accept them, and they drop straight into the
game: they see it, hear it, and press buttons on a virtual Xbox controller
plugged into your PC.

If they have a controller, they connect it to their phone or computer and
it just works. If they don't, touch controls show up on the screen.

## You stay in control of your PC

- Nobody plays until you accept them, one by one.
- Guests get a game controller and nothing else. No keyboard, no mouse, no
  files.
- Only the game window is shared, not your whole screen, and only the game's
  sound (so your Discord call stays yours).
- You can kick whoever is playing from the panel, and stop sharing from the
  panel or the tray icon.
- The Playrift server only introduces your PC to your friend's browser. The
  video, the sound and the controller go straight between you, or through an
  encrypted relay when a network doesn't allow a direct connection. Nothing
  is recorded or stored.

## What you need

**On your PC (the host)**

- Windows 10 or 11, 64-bit.
- An AMD Radeon graphics card. Playrift uses AMD's hardware encoder for now;
  NVIDIA and Intel aren't supported yet.
- A good upload speed. Playrift lowers the quality on its own when the
  connection can't keep up, but the faster your upload, the better your
  friend sees the game.

**For your friend (the guest)**

- A recent browser: Chrome, Edge or Safari, on a phone, a computer or a TV.
- A controller is nice to have, not required.

For now, one friend plays at a time.

## Installing

1. Download `Playrift_x64-setup.exe` from the link above.
2. Open it. The installer isn't code-signed yet, so Windows will say
   **"Windows protected your PC"**. Click **More info**, then **Run anyway**.
3. Windows asks once for permission. That lets the installer set up the
   virtual controller driver
   ([ViGEmBus](https://github.com/nefarius/ViGEmBus)) and a firewall rule so
   your friend can reach Playrift.

Each release lists the SHA-256 of the installer in its notes, if you want to
check the file you downloaded.

## If something goes wrong

Playrift keeps its logs in `%LOCALAPPDATA%\app.playrift.desktop\logs\`.
They never include room links, relay passwords or what your guest pressed.
If you're helping test, send those files along with what happened.

## Credits

Playrift uses [FFmpeg](https://ffmpeg.org) under the LGPL (its license ships
with the installer) and [ViGEmBus](https://github.com/nefarius/ViGEmBus) for
the virtual controller.

[playrift.app](https://playrift.app)
