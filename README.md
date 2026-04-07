# esphome-packages
[Packages](https://esphome.io/guides/configuration-types.html#packages) for my [ESPHome](https://esphome.io) devices.

## Quick start

1. Copy one of the top-level example configs (for example, `electrolux-ac-esp8266.yaml` or `gree-ac-esp8266.yaml`).
2. Add a `secrets.yaml` with at least:
   - `wifi_ssid`
   - `wifi_password`
   - `ap_password`
   - `ota_password`
   - `api_key`
3. Build/validate locally:
   - `esphome config <your-config>.yaml`
   - `esphome run <your-config>.yaml`

## Security checklist (recommended)

- Always override fallback AP password (`ap_password`) from `common/minimal.yaml`.
- Always set a non-empty OTA password (`ota_password`).
- Use a unique API encryption key (`api_key`) per environment.
- Keep secrets in `secrets.yaml` and never commit them.

## Configuration notes

- Top-level sample files are intended as entrypoints for specific devices.
- Shared behavior is composed through package includes under `common/`, `hardware/`, and `climate/`.
