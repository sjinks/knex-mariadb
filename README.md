# knex-mariadb

[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg?style=flat-square)](https://github.com/Flet/semistandard)

MariaDB Client for Knex.js

# Install

```bash
npm i --save-dev knex-mariadb
```

`knex-mariadb` has peer dependencies on [`knex`](https://www.npmjs.com/package/knex) and [`mariadb`](https://www.npmjs.com/package/mariadb), please make sure that they are installed as well.

# Usage

`knex-mariadb` should be compatible with `mysql` and `mysql2` knex clients, see [this page](https://knexjs.org/#Installation-client) for connection options.

Note that you cannot pass `client: 'mariadb'` to Knex because this method can be used only with the "official" clients.

You should use something like this instead:

```js
const mdb = require('knex-mariadb');
const knex = require('knex')({
  client: mdb,
  // Other options go here
});
```
