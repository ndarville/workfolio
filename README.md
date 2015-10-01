1. Create a repo named {{ github_username }}.github.io on GitHub.
2. Copy these files to the repo, using either the browser interface or [Git][].
3. Update `links.atom`, when you create new work you want to share.

    Again, you can do so using Git or the browser interface at `https://github.com/{{ github_username }}/{{ github_username }}.github.io/edit/master/data/links.yml`.

Your site should, eventually, be updated to reflect the changes, with the feed available at `https://{{ github_username }}.github.io/links.atom`.

NB: Remember to link to the HTTPS version of you website, as GitHub Pages does not redirect automatically.

If you want, you can also set up a website that shows a list of your new work on the front page at `index.html`. For now, this is a minimal proof of concept.


[Git]: https://pages.github.com
