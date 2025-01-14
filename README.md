# Morph Docs

We use [Mintlify](https://mintlify.com/docs/quickstart) to build our [documentation](https://docs.morphdb.io/).

## Building

To build the docs, clone this repo, install the mintlify CLI, and run the development server.

### 1. Set up your environment

Install Mintlify CLI

```
npm i -g mintlify
```

### 2. Run the development server


```
mintlify dev
```

## Directory structure

- `docs/`: Markdown files for the documentation
- `asstes/`: Static files like images

If you want to create a new page group, create a directory at the root level.

This refers to the group managed by Mintlify's tabs.

## mint.json

Each page can be written in MDX, but to reflect it in the actual page, you need to edit mint.json.

See the [Mintlify documentation](https://mintlify.com/docs/settings/navigation) for more details.

### navigation

The navigation array in mint.json is an item for declaring the page group, and by setting navigation, you can use that group in the sidebar or tab. Therefore, **you must add a setting to the navigation when you add a page.**

```json
{
  "navigation": [
    {
      "group": "Get Started",
      "version": "en",
      "pages": [
        "docs/en/introduction",
        "docs/en/quickstart",
        "docs/en/development"
      ]
    }
  ]
}
```

# Contributing

If you are interested in contributing to Morph Docs, please create a branch in the local environment and create a PR towards the main branch.

The main branch is automatically deployed when a PR is merged.
