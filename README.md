# Spree Starter (formerly Spark Starter Kit)

[![Circle CI](https://circleci.com/gh/spree/spree_starter.svg?style=svg)](https://circleci.com/gh/spree/spree_starter) [![Maintainability](https://api.codeclimate.com/v1/badges/d240686c99b3d35eb61b/maintainability)](https://codeclimate.com/github/spree/spree_starter/maintainability)

This a dockerized [Spree Commerce](https://spreecommerce.org) application template ready to for local development and deployment to cloud providers.

## Launch on Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Local Installation

### Install required tools and dependencies:

  * [Docker](https://www.docker.com/community-edition#/download) with docker-compose

### Run setup script

```bash
bin/setup
```

### (Optional) Import sample data such as products, categories, etc

```bash
docker-compose run web rake spree_sample:load
```

### Launching local server

```bash
docker-compose up
```

## Updating

```bash
bundle update spree
docker-compose build
```

For additional instructions please visit [Spree Upgrade Guides](https://dev-docs.spreecommerce.org/upgrades)

## Development

### Launching rails console

```bash
docker-compose run web rails c
```

### Launching bash console

```bash
docker-compose run web bash
```

## Customization
### Adding new gems

Update `Gemfile` and run

```bash
bundle install
docker-compose build
```

You will need to restart the server if running:

```bash
docker-compose restart
```

## Environment variables

| variable | description | default value |
|---|---|---|
| DEBUG_ASSETS | Enables/disables [asset debugging in development](https://guides.rubyonrails.org/asset_pipeline.html#turning-debugging-off) | false |
| DB_POOL | database connection pool | 5 |
| MEMCACHED_POOL_SIZE | memcache connection pool | 5 |
| SENDGRID_API_KEY | API key to interface Sendgrid API | |

## License

Spree Starter (formerly Spark Starter Kit) is copyright © 2015-2021
[Spark Solutions Sp. z o.o.][spark]. It is free software,
and may be redistributed under the terms specified in the
[LICENSE](LICENSE.md) file.

## About Spark Solutions

[![Spark Solutions](http://sparksolutions.co/wp-content/uploads/2015/01/logo-ss-tr-221x100.png)][spark]

Spree Starter is maintained and funded by [Spark Solutions Sp. z o.o.](http://sparksolutions.co?utm_source=github)
The names and logos are trademarks of Spark Solutions Sp. z o.o.

We are passionate about open source software.
We are [available for hire][spark].

[spark]:http://sparksolutions.co?utm_source=github
