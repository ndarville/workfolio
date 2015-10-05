1. Create a repo named `{{ github_username }}.github.io` on GitHub.
2. Import the required code by going to

        https://import.github.com/{{ github_username }}/{{ github_username }}.github.io/import

    and entering

        https://github.com/ndarville/workfolio

3. Update `links.atom`, when you create new work you want to share.

    Again, you can do so using Git or the browser interface at

        https://github.com/{{ github_username }}/{{ github_username }}.github.io/edit/master/data/links.yml

4. Update your config in `_config.yml` as well, using Git or from

        https://github.com/{{ github_username }}/{{ github_username }}.github.io/edit/master/data/_config.yml

    You only need to update the `name` and `url` fields.

Your site should, eventually, be updated to reflect the changes, with the feed available at

    https://{{ github_username }}.github.io/links.atom

**NB:** Remember to link to the HTTPS version of you website, as GitHub Pages does not redirect from HTTP automatically. (If you forget, it’s not the end of the world.)
