# traefik-template

Traefik template example for docker-compose to be used with docky / ak / odoo

How to use it:

```sh
git clone https://github.com/akretion/traefik-template.git traefik
cd traefik
docker-compose up -d
```

Make sure port 80, 8080 and 443 are available.

Dashboard is available on http://localhost:8080


Now this version include also

- mailpit: available on http://localhost:8025
in your server_environnment_files module
you have to set in your `dev` env for every project
`mailpit` as host and `1025` as port


- kwkhtmltopdf
