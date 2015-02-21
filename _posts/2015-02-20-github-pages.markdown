---
layout:   post
title:    "Hosting a Static Site on GitHub Pages"
category: Web-Development 
---

I believe in solutions that are tailored to a client's needs, and since small businesses often do not need a blog, process data or update content regularly, a brochure site or a landing page is sufficent to meet a marketing requirement. In short, not every small business needs a WordPress site or a CMS for that matter.

Below I explain in 8 steps how to host a static website on [GitHub Pages](https://pages.github.com/) using a custom domain name. Did I mention it's free of charge?

1. ###Create a static website locally
Build a [Bootstrap](http://getbootstrap.com) site or hand code a site from scratch on your computer.

2. ###Create a GitHub account
Go to [GitHub.com](http://github.com) and create an account


3. ###Create an Organization (optional)
While this step is not required, if you're going to delegate the site maintenance to an employee or a freelancer, it is recommended to create an Organization with your company's name. This is to avoid sharing your GitHub credentials with other people.

4. ###Create a repository
Create a repository with your GitHub account and name it [account-name].github.io. If you created an Organization, name the account [organization-name.github.io]. You can also create a team and grant this team write-access to your new repository. This will allow you to add other people to this team, who will be able to update your site.

5. ###Commit and push your website files to the organization's repository
Download the GitHub app or use the command line to push your website files to your GitHub repository.

6. ###Add CNAME file to repository
Additionally, create a file that includes your custom domain name prefixed with 'www.' (i.e. www.example.com). Name this file 'CNAME' and push to repository.

7. ###Configure custom domain's DNS settings to point to GitHub servers
Go to your domain name provider's control panel and open the DNS configuration page for your custom domain. Add a CNAME record for a 'wwww' subdomain and 2 A records pointing at 192.30.252.153 and 192.30.252.154 respectivelly.

8. ###Visit your new site.
It may take a few hours for the DNS configuration changes to propagate, but soon you will be able to see your static site on your custom domain. Below is an example of DNS configuration for GitHub Pages using [Google Domains](http://domains.google.com).

![DNS sample settings](http://googledrive.com/host/0B7JXcWvuAx6QfjMzdTFndVVXaXRFUHVuS3BNcVViN3RCSjQ5b1FNOTNCa19LVHBwYXVLaTA/Google_domains.jpg)

**Note:** Following the configuration above will make your bare domain (i.e. example.com) redirecit to your www domain (www.example.com).

If you live in Phoenix, Arizona, and you're interested in learning more about hosting your site on GitHub Pages, check out the [Phoenix GitHub Pages Meetup](http://www.meetup.com/Phoenix-GitHub-Pages-Meetup).
