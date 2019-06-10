# Gatsby & Firebase

_This example firebase app uses the [Gatsby Starter Emma by LekoArts](https://github.com/LekoArts/gatsby-starter-portfolio-emma)_


<!-- TOC -->

- [Gatsby & Firebase](#gatsby--firebase)
  - [Firebase Project Setup](#firebase-project-setup)
  - [Preparing your Gatsby Website](#preparing-your-gatsby-website)
  - [Testing and Deployment](#testing-and-deployment)

<!-- /TOC -->


## Firebase Project Setup

1. Go to the [Firebase Website](https://firebase.google.com/products/hosting/) and sign in with your Gmail account.
2. Click on [Visit Console](https://console.firebase.google.com/project/_/hosting?pli=1) to open your project console.
3. Click on Add Project to create your new project and assign a name for it.
4. Now go to __Hosting__ in your Project Overview and click the __Get Started__ button.
5. Switch to your system console/terminal and run `npm install -g firebase-tools` (make sure that [Node.js is installed](https://nodejs.org/en/) on your system).


![Firebase Static Hosting](./screenshots/firebase_01.png)


6. Click continue on the Firebase setup wizard then go back to your console and type in `firebase login`. You will be given an URL to set up the necessary permissions for the Firebase CLI on your Gmail account.


## Preparing your Gatsby Website

1. Download a [Gatsby Starter](https://www.gatsbyjs.org/starters/?v=2).
2. Run a `npm install` and `gatsby build` inside the Starter folder (make sure that you have the [Gatsby-Cli installed](https://www.gatsbyjs.org/docs/gatsby-cli/) on your system).
3. And there run the command `firebase init` and go to __Hosting__ by using your ARROW keys and select it with SPACE and ENTER.


![Firebase Static Hosting](./screenshots/firebase_02.png)


4. You will now be asked which Firebase project this code belongs to. Select the project name that you have chosen in the [Firebase Project Setup](#firebase-project-setup).
5. Gatsby created your static site content inside the `.\public` folder - set the Firebase Project public directory to this folder.
6. Since Gatsby generates routes for each page, choose __not to rewrite__ URLs to index.html.


![Firebase Static Hosting](./screenshots/firebase_03.png)


## Testing and Deployment

1. You can test your website by running `firebase serve` - you site will be hosted on `http://localhost:5000`.
2. If everything looks fine run `firebase deploy` to upload the content of your public folder to firebase.
3. You will be able to access your website from the __Hosting URL__ or configure it from the __Project Console__.


![Firebase Static Hosting](./screenshots/firebase_04.png)










<br/><br/><br/><br/><br/><br/><br/><br/>

---

Original Starter README

![](https://i.imgur.com/M0nwIVi.png)

Gatsby Starter Portfolio: Emma

A portfolio starter for [Gatsby](https://www.gatsbyjs.org/). The target audience are designers and photographers.

[Demo Website](https://emma.lekoarts.de)

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/LekoArts/gatsby-starter-portfolio-emma) [![Edit gatsby-starter-portfolio-emma](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/github/LekoArts/gatsby-starter-portfolio-emma/tree/master/)

[![CircleCI](https://circleci.com/gh/LekoArts/gatsby-starter-portfolio-emma.svg?style=svg)](https://circleci.com/gh/LekoArts/gatsby-starter-portfolio-emma) [![Netlify Status](https://api.netlify.com/api/v1/badges/5a4f3e8c-82cb-411d-89f1-fcfde2d3cf80/deploy-status)](https://app.netlify.com/sites/portfolio-emma/deploys)

- Full-width grid-layout
- Large images
- Light theme

Why?

If you want to quickly bootstrap a design/photography portfolio or use it as a foundation for your personal site the _gatsby-starter-portfolio_ are a perfect fit for you! The project's goal is to offer minimalistic and fast websites.

I hope you like my starters and create something awesome! To see some of my work you can visit my [website](https://www.lekoarts.de) or support me on [Patreon](https://www.patreon.com/lekoarts) to get some neat rewards (4K images, project files, tutorial insights). Every pledge on Patreon helps me creating more free starters!

Also check out the other _gatsby-starter-portfolio_:

- [gatsby-starter-portfolio-emilia](https://github.com/LekoArts/gatsby-starter-portfolio-emilia)
- [gatsby-starter-portfolio-bella](https://github.com/LekoArts/gatsby-starter-portfolio-bella)
- [gatsby-starter-portfolio-cara](https://github.com/LekoArts/gatsby-starter-portfolio-cara)
- [gatsby-starter-portfolio-jodie](https://github.com/LekoArts/gatsby-starter-portfolio-jodie)

Check out the [Gatsby Starter Portfolio Overview](https://gatsby-starter-portfolio.netlify.com/)!

Features

- Configurable
  - Use the website.js to easily change the most important information
  - Easily change the font
- Choose a color for your projects highlights
- Create your subpages with MDX
- Uses styled-components for styling
- [react-spring](https://github.com/react-spring/react-spring) animations
- Projects in MDX ([gatsby-mdx](https://github.com/ChristopherBiscardi/gatsby-mdx))
- Cypress for End-to-End testing (+ CircleCI config)
- Google Analytics Support
- SEO
  - Sitemap
  - Schema.org JSONLD
  - OpenGraph Tags
  - Twitter Tags
- Offline Support
- WebApp Manifest Support
- Responsive images
  - The right image size for every screen size
  - Traced SVG loading (lazy-loading)
  - WebP support

Getting Started

Check your development environment! You'll need [Node.js](https://nodejs.org/en/), the [Gatsby CLI](https://www.gatsbyjs.org/docs/) and [node-gyp](https://github.com/nodejs/node-gyp#installation) installed. The official Gatsby website also lists two articles regarding this topic:

- [Gatsby on Windows](https://www.gatsbyjs.org/docs/gatsby-on-windows/)
- [Check your development environment](https://www.gatsbyjs.org/tutorial/part-zero/)

To copy and install this starter run this command (with "project-name" being the name of your folder you wish to install it in):

```
gatsby new project-name https://github.com/LekoArts/gatsby-starter-portfolio-emma
cd project-name
npm run dev
```

Adding a new project

- Create a new folder in `content/projects`
- Create a new markdown/mdx file, add the frontmatter (use the date format "YYYY-MM-DD")
- Add an image and reference it in your frontmatter as `cover`
- Write your content below the frontmatter

If you're still unsure have a look at the already existing examples.

Adding a new page

- Create a new folder in `src/pages`
- Create a new mdx file with the name `index.mdx` in it

Adding new features/plugins

You can add other features by having a look at the official [plugins page](https://www.gatsbyjs.org/docs/plugins/)

Building your site

```
npm run build
```

Copy the content of the `public` folder to your webhost or use a website like Netlify which automates that for you.

Configuration

You can configure your setup in `config/website.js`:

```JS
module.exports = {
  pathPrefix: '/', // Prefix for all links. If you deploy your site to example.com/portfolio your pathPrefix should be "portfolio"
  siteTitle: 'Emma', // Navigation and Site Title
  siteTitleAlt: 'Emma - Gatsby Starter Portfolio', // Alternative Site title for SEO
  siteHeadline: 'Creating marvelous art & blazginly fast websites', // Headline for schema.org JSONLD
  siteTitleShort: 'Emma', // short_name for manifest
  siteUrl: 'https://emma.lekoarts.de', // Domain of your site. No trailing slash!
  siteLanguage: 'en', // Language Tag on <html> element
  siteLogo: '/logo.png', // Used for SEO and manifest
  siteDescription: 'Minimalistic bright portfolio with full-width grid and large images',
  author: 'LekoArts', // Author for schema.org JSONLD

  // siteFBAppID: '123456789', // Facebook App ID - Optional
  userTwitter: '@emma', // Twitter Username
  ogSiteName: 'emma', // Facebook Site Name
  ogLanguage: 'en_US',
  googleAnalyticsID: 'UA-12345689-1',

  // Manifest and Progress color
  themeColor: '#3498DB',
  backgroundColor: '#2b2e3c',
}
```

You can also configure the styling of the site by editing the theme variables in `config/theme.js`.

```JS
import { darken } from 'polished'

const brand = {
  primary: '#cf1993',
  secondary: '#7b8acc',
}

const colors = {
  grey: '#6b6b6b',
  black: '#000',
  white: '#fff',
  bg_color: '#f3f3f3',
  body_color: '#444',
  link_color: brand.primary,
  link_color_hover: `${darken(0.15, brand.primary)}`,
}

const theme = {
  brand,
  colors,
  breakpoints: {
    xs: '400px',
    s: '600px',
    m: '900px',
    l: '1200px',
  },
  container: {
    base: '100rem',
    text: '55rem',
  },
  spacer: {
    horizontal: '2rem',
    vertical: '3rem',
  },
}

export default theme
```

**Attention:** You also need to edit `static/robots.txt` to include your domain!
