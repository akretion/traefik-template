# traefik-template

Traefik template example for docker-compose to be used with docky / ak / odoo.

How to use it:

```sh
git clone https://github.com/akretion/traefik-template.git traefik
cd traefik
docker-compose up -d
```

Make sure ports 80, 8080 and 443 are available.

Traefik dashboard is available at http://localhost:8080

---

This version also includes:

- **kwkhtmltopdf**: a shared `wkhtmltopdf` service for all local instances.
- **mailpit**: a shared mail catcher available at http://mail.localhost.

The Mailpit SMTP server listens on port 1025.

To use Mailpit with your local Odoo (ENV=dev), you can create a `server_environment_files` module with the following minimal configuration in `server_environment_files/dev/base.conf`:

```ini
[outgoing_mail]
smtp_host = mailpit
smtp_port = 1025
smtp_encryption = none
```

More info at:
- https://github.com/OCA/server-env/tree/18.0/server_environment
- https://github.com/OCA/server-env/tree/18.0/mail_environment