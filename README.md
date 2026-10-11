# AustinProps.city

A simple site about Austin city propositions on the ballot.

## Running locally

1. Clone the repo
1. Install Ruby 3.3+: `brew install ruby`
1. Install bundler: `gem install bundler`
1. Install the gems from this repo’s bundle: `cd austinprops.city && bundle`
1. Make changes to the site and run the site locally: `bundle exec jekyll serve`
1. Visit `localhost:4000` to see the site


## Running with Docker

1. Clone the repo
1. Install Docker
1. Make changes to the site and run the site locally: `cd austinprops.city && docker compose up`
1. Visit `localhost` to see the site

## Deploying

Pushes to `master` build with the Gemfile's Jekyll and deploy via the GitHub
Actions workflow in `.github/workflows/pages.yml`. In the repository's
Settings → Pages, the source must be set to “GitHub Actions”.

## A new election

1. Set `current_ballot` and `election_date` in `_config.yml`. Earlier ballots
   move to `/archive` automatically.
1. Add one post per proposition with `ballot`, `jurisdiction`, `order`, `tags`,
   and `recommendation` in the front matter.
