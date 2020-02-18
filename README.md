# Peach CLI

Command line tool to migrate wordpress databases between domains.

This is a command line version of [Peach](http://psaia.github.com/Peach/),
great work of my good friend [Pete Saia](https://github.com/psaia).

## The problem

- You are developing a [Wordpress](https://wordpress.org) website locally.
- You setup a dummy domain, like `http://localhost` or `http://localhost:8000`
  or even `http://mysite.local`
- The site is ready to go staging/production (like `http://mycoolsite.com`)
- You make a database dump from your local
- You restore the dump on staging/production
- ... and all links a broken because the old domain (`http://mysite.local` is not cool on production)

## The solution

Use [Peach](http://psaia.github.com/Peach/), online version! Drag and drop your sql dump, inform your new domain, run it, everything on the browser, no tracking.

But, if you like a little more automation, use **Peach command**. Yeah, this tool.

## Install

```bash
npm install -g @rafaelgou/peach-cli
```

or

```bash
yarn global @rafaelgou/peach-cli
```

to install the command line globally.

Run it:

```bash
peach-cli <PATH_TO_YOUR_SQL_FILE> <NEW_DOMAIN>
```

You get a new file converted with `-migrated.sql` suffix/extension
