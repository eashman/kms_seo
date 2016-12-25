## KMS SEO

Adds SEO support to KMS: meta tags fields, sitemap.xml generating, redirects, special {{ seo }} variable.

Use "seo" object for accessing SEO settings for page or object.

        <title>{{ seo.title }}</title>
        <meta name="keywords" content="{{ seo.keywords }}">
        <meta name="description" content="{{ seo.description }}">

Also, this adds sitemap generation support (at /sitemap.xml)

## Installation

1. Add to Gemfile

        gem "kms_seo"
        # or for edge version:
        gem "kms_seo", github: "webgradus/kms_seo"

2. Run generator:

        bundle exec rails g kms_seo:install

3. Copy migrations:

        bundle exec rails kms_seo:install:migrations

4. Migrate:

        bundle exec rails db:migrate

5. Recompile assets (if on production):

        bundle exec rails assets:precompile

6. Restart KMS instance

## Contributing

Please follow [CONTRIBUTING.md](CONTRIBUTING.md).
