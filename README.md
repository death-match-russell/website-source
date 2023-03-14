# Death Match Russell Podcast - Static Site Generator

## Jekyll
This repository contains the necessary files to generate a [Jekyll](https://jekyllrb.com/) website for Death Match Russell Podcast.

The site uses Jekyll's _posts folder to organise posts, this includes all podcast episode posts. If you want to make a manual post, you can simply create a markdown file in the _posts folder. [here](https://gist.github.com/roachhd/779fa77e9b90fe945b0c) is a quick reference for how markdown files can be written.

Further, if you want to build the files manually on your machine (you may only need to do this if making modifications to the site) you'll need to:
* Clone the repository on your machine using [git](https://github.com/git-guides/install-git) `git clone git@github.com:death-match-russell/website-source.git`.
* Install Jekyll using the instructions [here](https://jekyllrb.com/docs/installation/).
* Build the site by running `bundle exec jekyll build` in the root folder of the project which will produce the files in the `_site` folder.
You can also check the site's working locally using `bundle exec jekyll server` which should allow you to see the site running locally at [http://127.0.0.1:4000/](http://127.0.0.1:4000/).

If you want to add more images to the site's photos page you can easily just drop a photo into the `/assets/images/photos` folder. If you have the GitHub page open to that [folder](https://github.com/death-match-russell/website-source/tree/main/assets/images/photos) you should be able to just drag and drop from your machine to the page.

After making changes the GitHub Actions Workflows should automatically begin the process of building the site and publishing changes. This can take a few minutes.

## GitHub Actions Workflows
It includes 2 a GitHub Actions Workflows that:
* Generates/Updates podcast posts for Apple and Youtube (with support for Spotify too if that's ever needed).
* Publishes the site to the official GitHub Pages repository.

The site should use these 2 Workflows to manage updates itself with no input required from the site owner/administrators. However, if needed the Workflows can be manually triggered by going to this repository's Actions tab, clicking the required Action, and then clicking Run Workflow (twice).
![Step 1](/readme/step-1.png)
![Step 2](/readme/step-2.png)
![Step 3](/readme/step-3.png)
![Step 4](/readme/step-4.png)

## External Services

The site is Hosted by GitHub, meaning that the files that you access in a browser eventually come from GitHub. However, the site is setup with a couple of other services to manage the Contact form, Domain, and DNS.

### Contact Form
The Contact form is setup using a [Formspree](https://formspree.io/) account. This allows people to contact the site with questions from the site's Contact page.

### Domain
The Domain is registered with [Google Domains](https://domains.google.com/registrar/). This allows people to access the site from the url [https://deathmatchrussellpod.com/](https://deathmatchrussellpod.com/).

###  DNS
The DNS service is [Cloudflare](https://www.cloudflare.com/). This also plays into accessing the site via the url however, it also provides a few nice features like edge caching which speeds up content delivery.
