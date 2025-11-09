# Welcome to Quarkiverse Hub!

* Quarkiverse GitHub organization
  * provides, 
    * about Quarkus extension projects,
      * build,
      * CI
      * release publishing

## documentation
* [docs](docs)

## Onboarding an extension 

* TODO: Looking to onboard an extension? Here's the [quick link](https://github.com/quarkiverse/quarkiverse/wiki#getting-an-extension-onboarded). 

## Updating the docs 

The content for the Quarkiverse Hub site lives in [the docs folder](https://github.com/quarkiverse/quarkiverse/tree/main/docs). 
It is [mirrored](https://github.com/quarkiverse/quarkiverse/blob/main/.github/workflows/wikisync.yml) to [the GitHub wiki](https://github.com/quarkiverse/quarkiverse/wiki), and also [published externally](https://hub.quarkiverse.io) as a Gatsby site. This allows the content to be indexed by search engines, and also enables richer formatting and styling.

### Run project locally

To stand up the Gatsby site locally, work in the `site` directory. First, install the required dependencies:

```
npm install
```

Then, to start development:

```
npm run develop
```
Gatsby will start a hot-reloading development environment at [localhost:8000](http://localhost:8000)
