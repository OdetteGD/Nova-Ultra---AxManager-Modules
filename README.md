Hey guys, here is the official release of Nova Ultra. I built this module because I was tired of typing manual su commands in Termux just to change my kernel settings before gaming.
This is a fully interactive WebUI root module. You just open the dashboard, tap the toggles, and the script applies the sysctl/setprop commands directly to your kernel in real-time.
🎨 The UI & Customization
Custom Background: I designed the top banner specifically for landscape/nakahiga anime styles. If you want to use your own pic, just replace the bg.jpg file inside the module folder. The UI automatically adds a dark gradient at the bottom so the text stays readable.
Live System Monitor: The green terminal text at the top isn't just for show. It runs a loop every 3.5 seconds to pull real hardware data directly from your root directory. It shows your actual device uptime, true battery temp, real RAM usage, and CPU load.
⚙️ What’s Inside?
1. Performance & Display
CPU Governors: Quick toggles to switch between Adaptive, Balance, Gaming, and Max Core modes.
FPS Locker: Force your SurfaceFlinger to lock at 30, 45, 60, 90, 120, or 144Hz. Good for bypassing game limits or saving battery.
2. Graphics & Touch
Force GPU Render: Forces hardware acceleration (debug.sf.hw 1). Moves UI rendering from the CPU to the GPU for way smoother scrolling.
Unlock V-Sync: Edits the EGL buffer count to fix frame pacing and remove Android's default frame cap.
Ultra Touch: Sets scroll friction to 0 and bumps the max touch events. Basically gives you zero input delay.
Instant UI: Cuts all Android animation scales to 0.5x so everything feels snappy.
3. System & Memory (LMK)
Dex2Oat Speed Compiler: Forces Android to compile your apps using the "speed" profile. Apps will take up slightly more storage space, but they will open instantly.
Smart LMK: Edits swappiness and vfs_cache_pressure. This stops Android from aggressively killing your heavy games just because you switched to Messenger or Spotify for two seconds.
Focus Mode: Completely disables background Auto-Sync (like Google Photos/Drive backups) so you don't get random ping spikes while playing.
4. Network & Security
TCP BBR: Replaces the default Android TCP routing with Google's BBR algorithm. If your mobile data is unstable, this prevents massive ping spikes.
Secure ICMP: Blocks ICMP redirects to
