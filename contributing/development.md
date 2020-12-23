## Imprint App Flame
Required disclosures as per § 5 of the German Telemedia Act
justDice GmbH
An der Alster 42
20099 Hamburg

Commercial Register Number: HRB 141399

App Flame is part of justDice GmbH

Authorised representatives:
Arne Wolter, Jonas Thiemann, Carlo Szelinsky

justDice GmbH holds a valid account with Deutsche Bank AG.
For further information, please reach out to contact@appflame.online.

Contact:
eMail: contact@appflame.online

VAT ID No.:
Dr officer
Stephan Krämer, LL.M., Attorney at Law (Germany)
Kinast & Partner Rechtsanwälte
Disclaimer

As a service provider, we are responsible for our own content on these Internet pages under § 7 (1) TMG and according to the general laws. According to §§ 8 to 10 TMG, however, we as service providers are not obliged to monitor transmitted or stored third-party information or investigate circumstances which indicate an illicit activity. Obligations to remove or block the use of information in accordance with the general laws remain unaffected. Any liability in this respect is, however, only incurred from the moment that knowledge of the specific breach of law is obtained. If we become aware of any legal infringements, we will remove these contents immediately.

Liability for Links

Our offer contains links to external websites of third parties on whose contents we have no influence. Therefore, we can not assume any liability for these third-party contents. The respective provider or operator of the pages is always responsible for the contents of the linked pages. The linked pages were checked for possible legal violations at the time of linking. Illegal contents were not recognizable at the time of linking. However, a permanent control of the content of the linked pages is not reasonable without specific indications of an infringement. We will remove such links immediately, if we become aware of any legal infringements. Development

This document describes the process for running this application on your local computer.

## Getting started

This site is powered by Node.js! :sparkles: :turtle: :rocket: :sparkles:

It runs on macOS, Windows, and Linux environments.

You'll need Node.js version 12 or 14 to run the site. To install Node.js, [download the "LTS" installer from nodejs.org](https://nodejs.org). If you're using [`nodenv`](https://github.com/nodenv/nodenv), read the [`nodenv` docs](#nodenv) for instructions on switching Node.js versions.

Once you've installed Node.js (which includes the popular `npm` package manager), open Terminal and run the following:

```sh
git clone https://github.com/github/docs
cd docs
npm install
npm run build
npm start
```

You should now have a running server! Visit [localhost:4000](http://localhost:4000) in your browser. It will automatically restart as you make changes to site content.

When you're ready to stop your local server, type <kbd>CTRL</kbd><kbd>c</kbd> in your terminal window.

Note that `npm run build` is a one-time step that create static assets.

### Using GitHub Codespaces

As an alternative, you can simply use [GitHub Codespaces](https://github.com/features/codespaces).

In a matter of minutes, you will be ready to edit, preview and test your changes directly from the comfort of your browser.

### Debugging with VS Code

This repo has configuration for debugging with VS Code's built-in Node Debugger.

1. After running the build steps, start the app by running `npm run debug`.
2. In VS Code, click on the Debugging icon in the Activity Bar to bring up the Debug view.
3. In the Debug View, select the **'Node: Nodemon'** configuration, then press F5 or click the green play button. You should see all of your running node processes.
4. Select the node process that's started with the `--inspect` flag.
5. Debugger has now been attached. Enjoy!

For more detailed instructions, please see this [VS Code recipe](https://github.com/Microsoft/vscode-recipes/tree/master/nodemon). You can also learn more about debugging using VS Code [here](https://code.visualstudio.com/docs/editor/debugging).

### Viewing a top-level table of contents

While running the local server, you can visit [localhost:4000/dev-toc](http://localhost:4000/dev-toc) to view a top-level TOC of all the content in the site. This page is not available on https://docs.github.com. It was created for internal GitHub writers' use.

At the `/dev-toc` path, you'll see a list of available versions. Click a version, and a list of products will appear. Note that the TOC content is versioned. If you are viewing `free-pro-team@latest` and you click the `Enterprise Admin` product, it will be empty, because there isn't any Admin content available on that version.

## Site structure

This site was originally a Ruby on Rails web application. Some time later it was converted into a static site powered by [Jekyll](https://jekyllrb.com/). A few years after that it was migrated to [Nanoc](https://nanoc.ws/), another Ruby static site generator.

Today it's a dynamic Node.js webserver powered by Express, using [middleware](../middleware/README.md) to support proper HTTP redirects, language header detection, and dynamic content generation to support the various flavors of GitHub's product documentation, like GitHub.com and GitHub Enterprise Server.

The tooling for this site has changed over the years, but many of the tried-and-true authoring conventions of the original Jekyll site have been preserved:

- Content is written in Markdown files, which live in the `content` directory.
- Content can use the [Liquid templating language](liquid-helpers.md).
- Files in the `data` directory are available to templates via the `{% data %}` tag.
- Markdown files can contain [frontmatter](https://jekyllrb.com/docs/front-matter).
- The [`redirect_from`](https://github.com/jekyll/jekyll-redirect-from) Jekyll plugin behavior is supported.

For more info about working with this site, check out these READMEs:

- [content/README.md](../content/README.md)
- [contributing/README.md](../contributing/README.md)
- [data/README.md](../data/README.md)
- [data/reusables/README.md](../data/reusables/README.md)
- [data/variables/README.md](../data/variables/README.md)
- [includes/liquid-tags/README.md](../includes/liquid-tags/README.md)
- [includes/README.md](../includes/README.md)
- [javascripts/README.md](../javascripts/README.md)
- [layouts/README.md](../layouts/README.md)
- [lib/liquid-tags/README.md](../lib/liquid-tags/README.md)
- [middleware/README.md](../middleware/README.md)
- [script/README.md](../script/README.md)
- [stylesheets/README.md](../stylesheets/README.md)
- [tests/README.md](../tests/README.md)
