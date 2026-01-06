Below is the **recommended, official method** to install **Caddy v2** on **Ubuntu** using Caddy’s maintained APT repository. This avoids outdated packages and ensures proper automatic updates.

---

## 1. Prerequisites

Ensure you are running Ubuntu 20.04 / 22.04 / 24.04 and have sudo access.

```bash
sudo apt update
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https curl
```

---

## 2. Add Caddy’s Official GPG Key

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' \
  | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg
```

---

## 3. Add the Official Caddy APT Repository

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' \
  | sudo tee /etc/apt/sources.list.d/caddy-stable.list
```

---

## 4. Install Caddy

```bash
sudo apt update
sudo apt install -y caddy
```

---

## 5. Verify Installation

```bash
caddy version
```

You should see output similar to:

```
v2.x.x h1:...
```

---

## 6. Check Service Status

Caddy installs as a **systemd service** by default.

```bash
sudo systemctl status caddy
```

Enable on boot (usually already enabled):

```bash
sudo systemctl enable caddy
```

---

## 7. Default Paths (Important)

| Purpose   | Path                   |
| --------- | ---------------------- |
| Caddyfile | `/etc/caddy/Caddyfile` |
| Web root  | `/var/www/html`        |
| Logs      | `journalctl -u caddy`  |
| Binary    | `/usr/bin/caddy`       |

---

## 8. Test with a Simple Site

Edit the Caddyfile:

```bash
sudo nano /etc/caddy/Caddyfile
```

Example:

```caddyfile
:80 {
    respond "Caddy is working"
}
```

Reload Caddy (no downtime):

```bash
sudo caddy reload --config /etc/caddy/Caddyfile
```

Then test:

```bash
curl http://localhost
```

---

## 9. Common Commands You’ll Use Often

```bash
sudo caddy reload
sudo caddy validate
sudo journalctl -u caddy -f
sudo systemctl restart caddy
```

---

## 10. Notes Specific to Your Use Case (PM2 / Next.js / APIs)

Since you frequently proxy **Next.js**, **Node**, and **PM2** services:

* **Do NOT** run Node on ports 80/443
* Run Node on ports like `3000–3999`
* Let **Caddy terminate TLS and reverse proxy**

Example:

```caddyfile
example.com {
    reverse_proxy localhost:3003
}
```

---

If you want, I can:

* Fix a **broken Caddyfile** (you had a `tls` global issue earlier)
* Provide a **production Next.js + PM2 + Caddy config**
* Help you set up **Cloudflare + Caddy**
* Debug **HTTPS / ACME / certificate failures**

Tell me what you want next.
