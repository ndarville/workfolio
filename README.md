Workfolio
=========
With Workfolio, you can create a

* hosted RSS feed for your work
* well-designed overview of all your work, or a featured list

The site will be available at `github_username.github.io`.

How-To
------
1. Create a GitHub user, if you don’t already have one. Here is the [registration page][].

    Make **sure** to choose a username that easily identifies you, eg

    * `firstname|lastname`
    * `firstnameInitial|lastname`

    as the username will be a part of the website URL.

2. [Create a repo][] named `{{ github_username }}.github.io` on GitHub.
3. Import the required code by going to

        https://import.github.com/{{ github_username }}/{{ github_username }}.github.io/import

    and entering

        https://github.com/ndarville/workfolio

4. Update `links.atom`, when you create new work you want to share.

    You can do this with Git or the browser interface at

        https://github.com/{{ github_username }}/{{ github_username }}.github.io/edit/master/data/links.yml

5. Update your config in `_config.yml` as well, using Git or the browser interface at

        https://github.com/{{ github_username }}/{{ github_username }}.github.io/edit/master/data/_config.yml

    You only need to update the `name` and `url` fields under `Required settings`.

Your site should, eventually, be updated to reflect the changes, with the feed available at

    https://{{ github_username }}.github.io/links.atom

Congrats on your new site!

**NB:** Remember to link to the HTTPS version of you website, as GitHub Pages does not redirect from HTTP automatically. (If you forget, it’s not the end of the world.)

Can I Use a Custom Domain Name?
-------------------------------
[You sure can][custom-github-pages], but this is for what you might call intermediate technical users. I use it myself for [some of my projects][hafnia-times].

I Can’t Get It to Work :(
-------------------------
You’re welcome to contact me about this as well. We’ll figure it out.


[registration page]: https://github.com/join
[create a repo]: https://github.com/new
[custom-github-pages]: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/
[hafnia-times]: https://github.com/hafniatimes/hafniatimes.github.io
