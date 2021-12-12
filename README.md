# Railway Ghost Starter

[![Deploy on Railway](https://img.shields.io/badge/Deploy%20on-Railway-b33acd)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2FStefanZoneExamples%2Frailway-ghost&envs=CLOUDINARY_URL%2CMYSQLHOST%2CMYSQLPORT%2CMYSQLUSER%2CMYSQLPASSWORD%2CMYSQLDATABASE%2CMYSQL_URL%2CCUSTOM_DOMAIN&optionalEnvs=CLOUDINARY_URL%2CCUSTOM_DOMAIN&CLOUDINARY_URLDesc=For+file+storage.+If+you+do+not+add+this%2C+your+images+won%27t+persist+between+deploys.&MYSQLHOSTDesc=Host+of+the+MySQL+database.&MYSQLPORTDesc=Port+of+the+MySQL+database.&MYSQLUSERDesc=User+of+the+MySQL+database.&MYSQLPASSWORDDesc=Password+of+the+MySQL+database.&MYSQLDATABASEDesc=Name+of+the+MySQL+database.&MYSQL_URLDesc=Connection+Url+of+the+MySQL+database.&CUSTOM_DOMAINDesc=Domain%2C+which+replaces+the+domain+with+the+%60*.up.railway.app%60+suffix.&MYSQL_URLDefault=mysql%3A%2F%2F%24%7B%7B+MYSQLUSER+%7D%7D%3A%24%7B%7B+MYSQLPASSWORD+%7D%7D%40%24%7B%7B+MYSQLHOST+%7D%7D%3A%24%7B%7B+MYSQLPORT+%7D%7D%2F%24%7B%7B+MYSQLDATABASE+%7D%7D&referralCode=stefankuehnel)

The [Ghost](https://ghost.org) configuration for a blog hosted on [Railway](https://railway.app) with an external MySQL database.

## Found a bug? 💁‍♀️

Thanks for letting me know! Please [file an issue](../../issues/new?assignees=&labels=&template=bug_report.md&title=) and I should reply shortly.

## Configuration 📝

Railway's filesystem is ephemeral which is why any changes to the filesystem are not persisted between deploys.

### Environment Variables

- `CUSTOM_DOMAIN`: Domain, which replaces the domain with the `*.up.railway.app` suffix. (**optional**)
- `CLOUDINARY_URL`: For file storage. If you do not add this, your images won't persist between deploys. (**recommended**)
- `MYSQLHOST`: Host of the MySQL database. (**required**)
- `MYSQLPORT`: Port of the MySQL database. (**required**)
- `MYSQLUSER`: User of the MySQL database. (**required**)
- `MYSQLPASSWORD`: Password of the MySQL database. (**required**)
- `MYSQLDATABASE`: Name of the MySQL database. (**required**)
- `MYSQL_URL`: Connection Url of the MySQL database. `mysql://user:password@host:port/database` (**required**)

### Themes

To add a theme, first add the package as a dependency to the `package.json` file, then add it to the list of themes in the `bin/themes.sh` file.

**Note**: Do NOT add a theme directly using the Ghost UI, it will look like it worked but will break whenever the app is deployed again.

## Deploying the site 🚀

The site will build and deploy the `main` branch automatically after every `git push origin main` via [Railway](https://railway.app).
