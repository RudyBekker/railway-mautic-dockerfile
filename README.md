# Mautic Dockerfile for Railway

This example deploys a self-hosted version of [mautic](https://www.mautic.org/). Using apache variant.
Make sure you also setup a mysql database in Railway.

## 💁‍♀️ How to use

- On your railway dashboard, setup a MySQL database
- Deploy this `Dockerfile` using the "from Github Repo" option

## 🌐 Environment Variables

```shell
MAUTIC_ADMIN_EMAIL=<your_email>
MAUTIC_ADMIN_PASSWORD=<mautic_web_password>
MAUTIC_DB_HOST=${{mysql.MYSQLHOST}}:${{mysql.MYSQLPORT}}
MAUTIC_DB_NAME=${{mysql.MYSQLDATABASE}}
MAUTIC_DB_PASSWORD=${{mysql.MYSQLPASSWORD}}
MAUTIC_DB_USER=${{mysql.MYSQLUSER}}
MAUTIC_TRUSTED_PROXIES='E.g.: ["0.0.0.0/0"]'
MAUTIC_URL=<your_fqdn_for_mautic>
PORT=80 # Set this to 80 so railway can properly connect to Mautic
```

## 📝 Notes

- Docs: https://docs.mautic.org/en
