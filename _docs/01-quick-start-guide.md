---
title: "Quick-Start Guide"
permalink: /docs/quick-start-guide/
excerpt: "How to quickly install and setup Minimal Mistakes for use with GitHub Pages."
last_modified_at: 2020-07-27
redirect_from:
  - /theme-setup/
toc: true
---

Alchemy has been developed as a _codeless_ data warehouse designing tool for Azure.
It's 100% compatible with your own Azure subscriptions and does not require any expensive proprietary software.

Alchemy automates your daily data warehouse development tasks with simple wizards and populates new entities as if you built it all manually by yourself.

**If you enjoy this project, please consider [supporting me](https://www.paypal.me/alchemy.io) for developing and maintaining it.**

[![Support via PayPal](https://cdn.jsdelivr.net/gh/twolfson/paypal-github-button@1.0.0/dist/button.svg)](https://www.paypal.me/mmistakes)

## Installing Alchemy CLI

If you have [NodeJS](https://nodejs.org/en/) 12.19+ installed on your machine you can quickly install Alchemy as npm package.

```bash
npm i -g @alchemy/cli
```

### Spells

Spells extract new elements and cast magic. Read more about spells here[^spells].

Let's see in practice what spells can do. First, let's extract a couple table definitions from the source database.

[^spells]: See [**Spells** page]({{ "/spells/" | relative_url }}) for a list of Alchemy spells and what they do.

<figure><img src="{{ '/assets/images/animated/alchemy-extract.gif' | relative_url }}" alt="creating a table extract with Alchemy"></figure>

This command extracts tables metadata into local YAML file that Alchemy uses to cast new elements.

Now, let's do some magic!

```bash
alchemy cast 'meta\demo\dbo\employee.yml'
```

You are free to decide what new elements you want to cast.

The result of cast command can be a new Data Factory pipeline with all required objects and parameters, or it can be the new transformation or data warehouse dimension table.

For example, the created Data Factory pipeline will connect to your source database and periodically copy defined tables, views, or dynamic queries as;

- parquet/csv files in your Azure Data Lake
- raw tables in your Azure SQL database
- data store tables in your Azure SQL database
- external tables or views in your Azure SQL database

## Features

Want to pull data into Synapse Analytics? Alchemy will cast elements in Synapse format for you.

Want to keep all changes in your history tables as SCD2? Alchemy can cast stored procedures, and update Data Factory pipelines to run them.

Alchemy follows best practices on each step of ETL development process. It creates automated tests, validations, and generates detailed documentation.

Dynamic pipelines are simple and easy to maintain. For example, administrator can run pipeline multiple times if it fails and it will continue to run from the last failed step.

Alchemy keeps all your connection details and all secrets in your Azure Key Vault. All your private data remains secured inside your cloud.

All these and many other features make Alchemy very convenient and secure tool for your daily data warehouse projects.

These are the next steps you should browse to know more:

- [Design Architecture](/docs/02-design-architecture)
- [Project Structure](/docs/03-project-structure)
- [Installation](/docs/04-installation)
