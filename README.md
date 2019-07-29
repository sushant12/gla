# Gla (jii-laa)

A bash script that mimics version control for your database. (sort of !!)

## Getting Started

[NOTE: This script only supports postgresl. Feel free to send PR for other adapters]

### Prerequisites

This bash script will only work on unix based os.

### Installing

Clone/Download the repo and copy `post-checkout` file to your project's `.git/hooks` folder.

```
git clone git@github.com:sushant12/gla.git
cd gla && cp post-checkout <project root .git/hooks folder>
```

You need to create a `gla.yml` file in your project's root directory. Without this file, the script will fail.

For eg, we support the following keys in the yml file

```
adapter: psql
encoding: utf8
database: <db name>
host: <db host>
port: <db port>
username: <your database username>
password: <your database password>
```

Finally, you need to locate your `.pgpass` file which will prolly be in your home directory. If it does not exist create one.

`.pgpass` will allow you to run `psql` command without the need to re-enter the password.

Lear more about (pgpass file here)[https://www.postgresql.org/docs/9.3/libpq-pgpass.html]

In your `.pgpass` file, add your database like this

```
localhost:5432:<your db name>:<your db username>:<your db password>
```


## Authors

* **Sushant Bajracharya** 
