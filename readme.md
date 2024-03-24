# Swirlix-Public

Because I wanted ~~Psyduck~~ Swirlix!

## Requirements
- API token from https://scrappey.com
  - It's 3rd party API, not associated with U#
  - You can get a free day of Swirlix use for email activation
  - Whole month should be under 4€
  - No accounts details are sent to external API
- Dragonite testing with `remote_auth_url` config
- Dragonite configuration
```toml
[general]
remote_auth_url = "http://127.0.0.1:7372/api/v1/login-code" # URL has changed!
```

## Startup

### Non-Docker

```sh
git clone https://github.com/UnownHash/Swirlix-Public.git && \
cd Swirlix-Public && \
cp config.toml.example config.toml && \
nano dragonite/config.toml
```

### Startup

> Logs are sent to stdout. File log will be added later!

```sh
pm2 start ./swirlix-linux-amd64 --name swirlix
```

### Update

- Execute `run.sh` to download the latest release (broken! download manually from Releases for now)
- Check Changelog, check `config.toml.example` for new config values available
- `pm2 restart swirlix`
