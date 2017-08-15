<div align="center">
    <img src="static/logos/logo-1024.png" alt="Logo" width='200px' height='200px'/>
</div>

# Gatsby Foundation Starter with Foundation

A blog starter with advanced features and Foundation Sites for [Gatsby](https://github.com/gatsbyjs/gatsby/).

This project extends the [Gatsby Foundation Starter](https://github.com/cherihung/gatsby-foundation-starter) with added [Foundation 6](http://foundation.zurb.com/) support.

[Demo website.](...)

## Features

* Blazing fast loading times thanks to pre-rendered HTML and automatic chunk loading of JS files
* Separate components for everything
* High configurability:
  * User information
  * User social profiles
  * Copyright information
  * More!
* Author segment
  * Name
  * Location
  * Description
  * Links
  * Follow Me button
* Posts in Markdown
  * Code syntax highlighting
  * Embed YouTube videos
  * Embed Tweets
* Tags
  * Separate page for posts under each tag
* Categories
  * Separate page for posts under each category
* Disqus support
  * Notifications about new disqus comments
* Google Analytics support
* NPM scripts for GitHub Pages deployment
* Social features
  * Twitter tweet button
  * Facebook share/share count
  * Reddit share/share count
  * Google+ share button
  * LinkedIn share button
  * Telegram share button
* SEO
  * Sitemap generation
  * robots.txt
  * General description tags
  * Schema.org JSONLD (Google Rich Snippets)
  * OpenGraph Tags (Facebook/Google+/Pinterest)
  * Twitter Tags (Twitter Cards)
* RSS feeds
* Loading progress for slow networks
* Offline support
* Web App Manifest support
* Development tools
  * ESLint for linting
  * Prettier for code style
  * Remark-Lint for linting Markdown
  * write-good for linting English prose
  * gh-pages for deploying to GitHub pages
  * CodeClimate configuration file and badge

## Getting Started

Install this starter (assuming [Gatsby](https://github.com/gatsbyjs/gatsby/) is installed) by running from your CLI:

```sh
gatsby new ProjectName https://github.com/cherihung/gatsby-foundation-starter
npm run serve
```

## Configuration

 Edit the export object in `data/SiteConfig`:

 ```js
module.exports = {
  blogPostDir: 'sample-posts', // The name of directory that contains your posts.
  siteTitle: 'Gatsby Foundation Starter', // Site title.
  siteTitleAlt: 'GatsbyJS Foundation Starter', // Alternative site title for SEO.
  siteLogo: '/logos/logo-1024.png', // Logo used for SEO and manifest.
  siteUrl: 'https://cherihung.github.io', // Domain of your website without pathPrefix.
  pathPrefix: '/gatsby-foundation-starter', // Prefixes all links. For cases when deployed to example.github.io/gatsby-foundation-starter/.
  siteDescription: 'A blog starter with advanced features and Foundation 6 for GatsbyJS', // Website description used for RSS feeds/meta description tag.
  siteRss: '/rss.xml', // Path to the RSS file.
  siteFBAppID: '', // FB Application ID for using app insights
  disqusShortname: '', // Disqus shortname.
  postDefaultCategoryID: 'Tech', // Default category for posts.
  userName: 'Cheri Hung', // Username to display in the author segment.
  userTwitter: 'cyhung', // Optionally renders "Follow Me" in the UserInfo segment.
  userLocation: 'North Pole, Earth', // User location to display in the author segment.
  userAvatar: '', // User avatar to display in the author segment.
  userDescription: "Yeah, I like animals better than people sometimes... Especially dogs. Dogs are the best. Every time you come home, they act like they haven't seen you in a year. And the good thing about dogs... is they got different dogs for different people.", // User description to display in the author segment.
  // Links to social profiles/projects you want to display in the author segment/navigation bar.
  userLinks: [
    {
      label: 'GitHub',
      url: 'https://github.com/cherihung/gatsby-foundation-starter',
      iconClassName: 'fa fa-github',
    },
    {
      label: 'Twitter',
      url: 'https://twitter.com/cherihung',
      iconClassName: 'fa fa-twitter',
    },
    {
      label: 'Email',
      url: 'mailto:cherihung@gmail.com',
      iconClassName: 'fa fa-envelope',
    },
  ],
  copyright: 'Copyright © 2017. Cheri Hung', // Copyright string for the footer of the website and RSS feed.

};
 ```

 You can also optionally set `pathPrefix`:
 ```js
 module.exports = {
  // Note: it must *not* have a trailing slash.
       pathPrefix: '/gatsby-foundation-starter', // Prefixes all links. For cases when deployed to example.github.io/gatsby-foundation-starter/.
}

 ```

 WARNING: Make sure to edit `static/robots.txt` to include your domain for the sitemap!
