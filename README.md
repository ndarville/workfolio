Workfolio
=========
With Workfolio, you can create a

* hosted RSS and JSON feed for your work
* well-designed overview of your work

(Or just a featured list of your work.)

The site will be available at `github_username.github.io`.

If you know your way around Jekyll, GitHub, or static pages, you’ll also know how to host this elsewhere.

Demo
----
As of this writing, you can check out the [live version][] of this repo.

How-To
------
1. Create a GitHub user, if you don’t already have one. Here is the [registration page][].

    Make **sure** to choose a username that easily identifies you, eg

    * `firstname|lastname`
    * `firstnameInitial|lastname`

    as the username will be a part of the website URL.

2. Go to your [e-mail settings][] and make sure you’ve checked the box “Keep my email address private”.
3. [Create a repo][] named `{{ github_username }}.github.io` on GitHub.
4. Import the required code by going to

        https://import.github.com/{{ github_username }}/{{ github_username }}.github.io/import

    and entering

        https://github.com/ndarville/workfolio

5. Update `links.yml`, when you create new work you want to share.

    You can do this with Git or the browser interface at

        https://github.com/{{ github_username }}/{{ github_repo }}/edit/master/data/links.yml

6. Update your config in `_config.yml` as well with Git or the browser interface at

        https://github.com/{{ github_username }}/{{ github_repo }}/edit/master/data/_config.yml

    You only need to update the `name` and `url` fields under `Required settings`.

    However, I’ve built in support for `archive` since a big issue with workfolios is your older work disappearing. [archive.is][] is great to make back up your work without too much effort. If no archive link is found, a query link for Internet Archive will be used instead&mdash;regardless of whether your article is archived. I also heartily endorse the [Wayback Machine extension][wayback].

    **NB:** If you are using a private repository for this project, and you don’t want people to see your `links.yml` file, you must also delete this line in `_config.yml`:

        data_dir: data

7. Go to the settings of your repo, `github.com/{{ github_username }}/your_repo/settings` under Options

8. Under GitHub Pages:

    * Under **Source**, click the drop-down and select “master branch” at the top.
    * Check **Enforce HTTPS**.
    * You can also set the custom domain here, which is handled by the `CNAME` file in your repo.

Your site should eventually be updated to reflect the changes with the feed available at

    https://{{ github_username }}.github.io

Congrats on your new site!

Can I use a custom domain name?
-------------------------------
[You sure can][custom-github-pages], but this is for what you might call technical people.

I use it myself for [some of my projects][hafnia-times].

I can’t get it to work :(
-------------------------
You’re welcome to contact me about this as well. We’ll figure it out.

Will my site automatically be updated with new features?
--------------------------------------------------------
Nope. You’ll basically have to follow the so-called [commit history][] for updates that sound important to you and copy-paste them yourself.

It is unlikely that there’ll be significant updates, but it is possible that changes will be made to `index.html` and `links.atom`, and perhaps `_config.yml`.

Should this happen, and you *really* want to update your site, I recommend you just copy-paste the code to your current files and save the changes. I *do not* recommend you delete your site, re-create it, and then re-import this repo, as you will lose the information your entered in `data/links.yml` and `_config.yml`.

For this reason, it never hurts to have a backup of `links.yml` somewhere else, should you manage to pull what I just described.

Never underestimate your ability to do something obscenely dumb, especially when the hour’s late or alcohol is involved.

Can I set up automated tweets about new articles?
-------------------------------------------------
With [IFTTT][], yes.

1. [Create an IFTTT user][ifttt-create]
2. Use this [IFTTT recipe][] and replace the field `Field URL`

        https://ndarville.github.io/feed.atom

    with

        https://{{ github_username }}.github.io/links.atom

    Remember to change `feed.atom` to `links.atom` in the URL—not just the username.

3. [Connect your Twitter account][] to IFTTT for the recipe to work.

You can change the recipe description, too, if you want, but it’s not required.

Be aware that IFTTT can take around one hour to react to triggers.

**NB:** Do keep your wits about you and fill your backlog of articles, *before* enabling this Twitter script, as you’ll subject your followers to a deluge of “new” RSS updates otherwise.

Boom. You’re now set to share your articles through both a website, an RSS feed, and now your Twitter account!

You can also use your RSS feed to trigger other events, be it with [IFTTT channels][IFTTT channels] or [Slack integrations][], or something else.

Related projects
----------------
* [Goal Tracker][]
* [Wishlist][]

Credits
-------
* [skeleton.css][], the CSS framework for this project


[live version]: https://ndarville.github.io/workfolio/
[registration page]: https://github.com/join
[e-mail settings]: https://github.com/settings/emails
[create a repo]: https://github.com/new
[archive.is]: https://archive.is
[wayback]: https://blog.archive.org/2017/01/13/wayback-machine-chrome-extension-now-available/
[custom-github-pages]: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/
[hafnia-times]: https://github.com/hafniatimes/hafniatimes.github.io
[commit history]: https://github.com/ndarville/workfolio/commits/master
[IFTTT]: https://ifttt.com
[ifttt-create]: https://ifttt.com/join
[IFTTT recipe]: https://ifttt.com/myrecipes/personal/28755829
[Connect your Twitter account]: https://ifttt.com/channels/twitter/activate
[IFTTT channels]: https://ifttt.com/channels
[Slack integrations]: https://ndarville.com/projects/slack/
[goal tracker]: https://github.com/ndarville/goal-tracker
[wishlist]: https://github.com/ndarville/wishlist
[skeleton.css]: http://getskeleton.com
