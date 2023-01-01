<h1 align="center">Convention</h1>

Trip Teknologi's Continuous Integration.

- A sample of workflow as `.github/workflows/php.yml`.

    ```
    name: Continuous Integration

    on: push

    jobs:
        ci_php:
            runs-on: ubuntu-latest
            steps:
                - uses: actions/checkout@v3
                  with:
                    fetch-depth: 0
                - uses: shivammathur/setup-php@v2
                  with:
                    php-version: "8.0"
                    extensions: ctype, fileinfo, mbstring, zip, gd, curl, bcmath, pcntl, sockets, session, tokenizer, json,xml, pdo, pdo_mysql, pdo_sqlite, mysqlnd, mysqli, xdebug, swoole, amqp, rdkafka, redis
                - run: php -v
    ```

- A sample of workflow as `.github/workflows/nodejs.yml`.

    ```
    name: Continuous Integration

    on: push

    jobs:
        ci_nodejs:
            runs-on: ubuntu-latest
            steps:
                - uses: actions/checkout@v3
                  with:
                    fetch-depth: 0
                - uses: actions/setup-node@v3
                  with:
                    node-version: "19"
                - run: node -v
    ```

- A sample of workflow as `.github/workflows/python.yml`.

    ```
    name: Continuous Integration

    on: push

    jobs:
        ci_python:
            runs-on: ubuntu-latest
            steps:
                - uses: actions/checkout@v3
                  with:
                    fetch-depth: 0
                - uses: actions/setup-python@v4
                  with:
                    python-version: "3.10"
                - run: python3 -V
    ```

Author
---

- Trip Teknologi ([@tripteki](https://linkedin.com/company/tripteki))
- Hasby Maulana ([@hsbmaulana](https://linkedin.com/in/hsbmaulana))
