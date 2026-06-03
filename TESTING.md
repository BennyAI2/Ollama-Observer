# Manual Smoke Test Checklist

Use this checklist before sharing a build or publishing a release.

## Launch And Window

- App launches without crashing
- Window icon and taskbar icon use the current logo
- Main dashboard loads with live telemetry
- History and Settings buttons open the correct views

## Tray Behavior

- Closing the window sends the app to tray when `Close to tray` is enabled
- Tray icon right-click menu shows `Open`, `Create desktop shortcut`, and `Exit`
- `Exit` fully shuts the app down
- `Start minimized to tray` starts the app hidden when enabled

## Dashboard

- Ollama running state updates correctly
- Loaded model information updates when a model is active
- System CPU, memory, GPU, VRAM, and temperature values refresh
- Ollama CPU and memory values refresh
- Running process table populates when Ollama is active
- Running process graph view opens and renders history bars

## History

- Passive mode records inferred activity sessions
- Proxy mode records exact prompt calls when requests go through the proxy
- Latest calls appear first
- Duration, CPU, memory, GPU, VRAM, and process columns are populated

## Settings

- App settings save successfully
- Ollama environment settings validate correctly
- Saving Ollama environment settings shows restart confirmation
- Cancelling the restart confirmation leaves Ollama running
- Confirming restart applies the settings and restarts Ollama

## Proxy Mode

- Enabling `Exact prompt history (proxy mode)` and saving app settings starts the proxy
- `http://127.0.0.1:11435` responds when proxy mode is enabled
- Requests sent through the proxy appear as exact history entries
- Switching back to passive mode disables the proxy listener

## Alerts

- Tray alert appears when Ollama stops
- Tray alert appears when VRAM usage exceeds the threshold
- Tray alert appears during sustained overload conditions
