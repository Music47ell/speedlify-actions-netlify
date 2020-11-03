# Speedlify + GitHub Actions + Netlify

This repository demonstrates how you can configure GitHub Actions `workflow` to **continuously measure your website Lighthouse score** by using Speedlify + GitHub Actions for free. Then deploy the dashboard to [Netlify](https://www.netlify.com/).
This repository is based on the workflow in [ThewApp/speedlify-actions](https://github.com/ThewApp/speedlify-actions) and [ThewApp/speedlify-actions-vercel](https://github.com/ThewApp/speedlify-actions-vercel).

By using the [workflow](.github/workflows/test-pages.yml) in this repository, you will have an **unlimited** build time in public repositories or a **2000**
minutes build time per month in private repositories for free. Thanks to [GitHub Actions](https://github.com/features/actions).

## Usage
1. Get this workflow by either:
   * Cloning this repository
   * [Importing the repository](https://github.com/new/import) to your account by entering `https://github.com/Music47ell/speedlify-actions-netlify`
   * [Using this repository as a template](https://github.com/Music47ell/speedlify-actions-netlify/generate)
   * Putting the [workflow file](.github/workflows/test-and-deploy.yml) in your existing Speedlify repository.
   Do **not** fork as GitHub Actions will not run on a forked repository.
2. Delete or skip the initial `_data/sites/*.js` files
3. Create your file with a list of your site URLs
4. [Add the following secrets](https://docs.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets#creating-encrypted-secrets-for-a-repository) to your repository:
    * `NETLIFY_AUTH_TOKEN`: Your Netlify Personal access tokens can be obtained from https://app.netlify.com/user/applications#personal-access-tokens
    * `NETLIFY_SITE_ID`: Go to **Site settings > General > Site details > Site information, and copy the value for API ID**
5. Commit and push to your repository.

---

**NOTE**

By default, the workflow runs daily at 06:00. You can change by editing [line 7](.github/workflows/test-and-deploy.yml#L7).

Here's a [list of cron examples](https://crontab.guru/examples.html)

---
