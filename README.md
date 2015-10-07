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

Can I use a custom domain name?
-------------------------------
[You sure can][custom-github-pages], but this is for what you might call intermediate technical users. I use it myself for [some of my projects][hafnia-times].

I can’t get it to work :(
-------------------------
You’re welcome to contact me about this as well. We’ll figure it out.

Can I set up an automated tweet about new articles?
---------------------------------------------------
With [IFTTT][], yes.

1. Create an IFTTT user
2. Use this [IFTTT recipe][] and replace the field `Field URL`

        https://ndarville.github.io/feed.atom

    with

        https://{{ github_username }}.github.io/links.atom

    Remember to change `feed.atom` to `links.atom` in the URL—not just the username.

3. [Connect your Twitter account][] to IFTTT for the recipe to work.

You can change the recipe description too, if you want, but it’s not required.

**NB:**Do keep your wits about you and fill your backlog of articles *before* enabling this Twitter script, as you’ll subject your followers to a deluge of “new” RSS updates otherwise.

Boom. You are now set to share your articles through both a website, an RSS feed, and now your Twitter account!

You can also use your RSS feed to trigger other events, be it with [IFTTT channels][IFTTT channels] or [Slack integrations][], or something else.


[registration page]: https://github.com/join
[create a repo]: https://github.com/new
[custom-github-pages]: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/
[hafnia-times]: https://github.com/hafniatimes/hafniatimes.github.io
[IFTTT]: https://ifttt.com
[IFTTT recipe]: https://ifttt.com/myrecipes/personal/28755829
[Connect your Twitter account]: https://ifttt.com/channels/twitter/activate
[IFTTT channels]: https://ifttt.com/channels
[Slack integrations]: https://ndarville.com/projects/slack/
