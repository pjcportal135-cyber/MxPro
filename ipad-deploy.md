# iPad deployment workflow

## Best workflow for you

Because you're using an iPad, use this setup:

- GitHub for code storage
- VPS for running the API and database
- Safari for testing the app
- Termius for SSH access

## On the VPS

Install these:

```bash
sudo apt update
sudo apt install -y git curl docker.io docker-compose-plugin
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

## Deploy steps

```bash
git clone https://github.com/YOUR-USERNAME/aeromaint-pro-saas.git
cd aeromaint-pro-saas
docker compose up -d
```

Then:

```bash
cd apps/api
cp .env.example .env
npm install
npm run seed
npm run build
npm start
```

And in a second shell:

```bash
cd apps/web
cp .env.example .env
npm install
npm run build
npm run dev -- --host 0.0.0.0
```

## Open from iPad

In Safari:

```text
http://YOUR-SERVER-IP:5173
```

For production later, put the web app behind a domain and reverse proxy.
