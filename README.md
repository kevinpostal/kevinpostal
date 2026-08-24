# Kevin Postal — Systems & Infrastructure

**Los Angeles · [ircfiber.com](https://ircfiber.com) · [kevinpostal/irc-fiber](https://github.com/kevinpostal/irc-fiber) · hireable**

D / Svelte / Ansible / Docker — I build always-on infrastructure that has to stay up. Most recent: **IRC Fiber**, a persistent IRC bouncer + web client (D + Svelte 5, BuildKit, Ansible) — `git clone --recursive` in 30s, clean history, 1Password → Codespaces.

<p align="center">
  <a href="https://github.com/kevinpostal/irc-fiber">
    <img src="https://github.com/kevinpostal/irc-fiber/releases/download/v0.3.0-demo/irc-fiber-final-minimal.gif" width="800" alt="IRC Fiber demo — splash → #autism 5s → #zod 5s" />
  </a>
</p>
<p align="center"><em>15s demo — splash → meth.cat#autism → IRC Fiber#zod · already logged in · <a href="https://github.com/user-attachments/assets/6720acd2-4c81-476f-ade8-c144bf9ada23">video (1920×1080)</a></em></p>

### Featured — IRC Fiber

**Problem:** Stay connected to multiple IRC networks 24/7, replay history on reconnect, manage from the browser — without dropping TCP/TLS on deploy.

**Solution:** Split `site` (gateway + Svelte 5) / `engine` (D daemon holds IRC) / `common` (shared lib). `Engine` sharded by `ServerRegistry`, `CHATHISTORY` replay, `EngineJanitor` TTL, `Redis` pub/sub, `Mongo` scrollback. Deploys via `ansible-playbook deploy-site.yml` / `deploy-engine.yml` — `site` never restarts `engine` (PID 7 stable).

* **Stack:** D LDC 1.41 / vibe.d, Svelte 5 + Vite + TypeScript, SCSS, Diet-NG, Redis 7, Mongo 7, Docker BuildKit, Ansible, SigNoz, Tailscale, Caddy
* **Ops:** `Containerfile.site` → `runtime-gateway` / `Containerfile.engine` → `runtime-engine` (never cross-compile), `1Password → Codespaces Secrets → vault`, `clean history` (`Kevin Postal <kevindpostal@gmail.com>`, `z0mgr00t`/`15.204.93.54` purged)
* **Links:** [Superproject `irc-fiber`](https://github.com/kevinpostal/irc-fiber) (1 clone via submodules) · [Site](https://github.com/kevinpostal/ircfiber-site) · [Engine](https://github.com/kevinpostal/ircfiber-engine) · [Live](https://ircfiber.com) · [Approach](https://github.com/kevinpostal/irc-fiber#architecture)

```bash
git clone --recursive https://github.com/kevinpostal/irc-fiber.git
cd irc-fiber
# Codespaces: postCreate → 1Password → vault, or:
op inject -i deploy/inventories/production/group_vars/vault.example.yml -o vault.yml
./site/scripts/generate-version.sh && docker compose -f site/docker-compose.yml -f engine/docker-compose.yml up -d
```

### Tech

`D` `vibe.d` `Svelte` `TypeScript` `Vite` `SCSS` `Docker` `Ansible` `Redis` `MongoDB` `Tailscale` `Caddy` `SigNoz` `1Password` `GitHub Actions` `Playwright`

### More

* 47 public repos — see pinned `irc-fiber`, `ircfiber-site`, `ircfiber-engine`, `ircfiber-common` below
* I ship infrastructure that survives `docker restart` / host reboot (`EngineJanitor`, `ServerRegistry` sharding, `CHATHISTORY` replay)
* Open to **Platform / Infrastructure / SRE** — Los Angeles (remote friendly) — `kevindpostal@gmail.com`

---
