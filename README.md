# Kevin Postal — Senior Full Stack Engineer

**Los Angeles, CA · [kevinpostal@gmail.com](mailto:kevindpostal@gmail.com) · [linkedin.com/in/kevinpostal](https://linkedin.com/in/kevinpostal) · [github.com/kevinpostal](https://github.com/kevinpostal) · [ircfiber.com](https://ircfiber.com)**

> Senior Full Stack Engineer — 19 years scaling Python systems to millions of users. Django · React · AWS/GCP · Docker/Kubernetes. I turn legacy monoliths into resilient microservices and ship CI/CD that cuts release cycles from weeks to hours. Seeking Senior/Lead Platform & Infrastructure — Remote (Los Angeles).

<p align="center">
  <a href="https://github.com/kevinpostal/irc-fiber">
    <img src="https://github.com/kevinpostal/irc-fiber/releases/download/v0.3.0-demo/irc-fiber-final-minimal.gif" width="800" alt="IRC Fiber demo — splash → meth.cat#autism 5s → IRC Fiber#zod 5s" />
  </a>
</p>
<p align="center"><em>Featured: IRC Fiber — 15s demo (already logged in via <code>.env</code>) — <a href="https://github.com/user-attachments/assets/6720acd2-4c81-476f-ade8-c144bf9ada23">video 1920×1080</a> · <a href="https://github.com/kevinpostal/irc-fiber">superproject</a> · <a href="https://ircfiber.com">live</a></em></p>

<p align="center">
  <a href="https://github.com/stats-organization/github-stats-extended"><img src="https://github-stats-extended.vercel.app/api?username=kevinpostal&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" alt="Kevin's GitHub stats" /></a>
  <a href="https://github.com/stats-organization/github-stats-extended"><img src="https://github-stats-extended.vercel.app/api/top-langs/?username=kevinpostal&layout=compact&langs_count=8&theme=tokyonight&hide_border=true" alt="Top Langs" /></a>
</p>

### Why IRC Fiber for your team

I built it to demo what I do in your stack — not because you need an IRC bouncer:

* **Python/Django parallel:** `site/backend` is a `vibe.d` gateway (HTTP/WS, auth, sessions) — same patterns as `Django`/`DRF` + `Celery` + `Redis` + `Mongo` I used at **National Services Group** (6 brands, 50K+ users, Zope→Django/Flask) and **Walmart OPUS** (millions of users). Swap the language, keep the contract (`RedisKeys`, `NetworkStateSnapshot`).
* **React parallel:** `site/frontend` is `Svelte 5` + `Vite` + `TypeScript` (IRCCloud-inspired) — same component/store/WebSocket work as `React`/`Angular`/`Vue` at **AMP Agency** (LinkedIn, Amazon, FX), **Keypr**, **Woven** (85M+ monthly). Svelte 5 runes map directly to React hooks.
* **Cloud/DevOps parallel:** `Docker BuildKit` (`Containerfile.site`/`engine` never cross-compile), `Ansible` (`deploy-site.yml`/`deploy-engine.yml` — site never restarts engine `PID 7`), `1Password → Codespaces Secrets → vault`, `clean history` (`Kevin Postal <kevindpostal@gmail.com>`), `EngineJanitor` TTL + `ServerRegistry` sharding + `CHATHISTORY` replay that survives `docker restart`.

```bash
git clone --recursive https://github.com/kevinpostal/irc-fiber.git
cd irc-fiber
op inject -i deploy/inventories/production/group_vars/vault.example.yml -o vault.yml
./site/scripts/generate-version.sh && docker compose -f site/docker-compose.yml -f engine/docker-compose.yml up -d
# → http://localhost:8090 — admin / z0mgr00t (via .env, gitignored)
```

### Technical Skills

**Languages:** Python, JavaScript (ES6+), Go, TypeScript, D, HTML5, CSS3
**Frameworks:** Django, Django REST Framework, Flask, FastAPI, Celery, React, Angular, Vue.js, Svelte 5, vibe.d
**Cloud & DevOps:** AWS (EC2, Lambda, S3, RDS, ECS/EKS, CodeBuild/CodePipeline), GCP (Cloud Functions, Cloud Run, BigQuery), Docker, Kubernetes, Terraform, CI/CD, Ansible, Tailscale, Caddy
**Databases & Caching:** PostgreSQL, MySQL, MongoDB, Redis, Elasticsearch, Snowflake
**Tools:** Git, REST API design, Microservices, Jira, pytest, Selenium, Playwright, SigNoz, 1Password

### Experience Highlights

* **National Services Group** `May 2024–Mar 2025` — Led Zope→Django/Flask for 6 brands, 50K+ users; AWS serverless + CI/CD; profiling + caching for memory leaks; 2-week sprints, mentoring.
* **Walmart / Sam’s Club** `Apr 2022–Aug 2023` — OPUS (Django microservice, millions of users); DRF APIs for search/inventory; Docker parity; query bottlenecks at peak.
* **AMP Agency** `Nov 2018–Dec 2019` — Python/Django for LinkedIn/Amazon/Facebook/FX; AWS (EC2/RDS/ECS/Lambda); cleared 6-month backlog in 8 weeks.
* **Freelance AI & Python** `Mar 2025–Present` — RAG + LLM APIs (OpenAI/Anthropic), AWS serverless (Lambda/API Gateway/DynamoDB/S3).

*Full history → [Resume (Bauhaus, PDF)](https://github.com/kevinpostal/kevinpostal/blob/main/Resume-Bauhaus.pdf) or [LinkedIn](https://linkedin.com/in/kevinpostal)*

### More

* 47 public repos — pinned `irc-fiber` (superproject, 1 clone) + `ircfiber-site` + `ircfiber-engine` + `ircfiber-common` below
* I ship infrastructure that survives host reboot — see `irc-fiber` `EngineJanitor` + `ServerRegistry`
* **Open to Senior/Lead — Platform / Infrastructure / SRE — Los Angeles (remote) — [kevinpostal@gmail.com](mailto:kevindpostal@gmail.com)**

---

> Profile inspired by [From Meh to Marvelous — Crafting a Killer GitHub Profile](https://medium.com/@chijiokeokorji/from-meh-to-marvelous-the-ultimate-guide-to-crafting-a-killer-github-profile-8dd3f6c6d602): demo GIF above the fold, pinned repos, topics, clean history, one-click Codespaces, 1Password.
