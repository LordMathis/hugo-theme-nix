# Nix

Nix is a simple, minimal theme for Hugo

![Hugo Theme Nix](https://raw.githubusercontent.com/LordMathis/hugo-theme-nix/master/images/screenshot.png)

## Usage

Clone the repository to your hugo theme directory

```
mkdir themes
cd themes
git clone https://github.com/LordMathis/hugo-theme-nix
```

## Configuration

Add these parameters to your `config.toml`:

```
[params]
  Name = "your_name"
  HeaderUsername = "username"
  HeaderHostname = "hostname"
  About = "info_about_you"
  ProfilePicture = "profile_picture_url"
```

`HeaderUsername` and `HeaderHostname` will be displayed in navbar on left side in the format: `HeaderUsername@HeaderHostname ~ $`.  

Optionaly you can add any of these social networks to the \[params\] section.

```
  BitbucketID = "your_bitbucket_id"
  BlueskyID = "your_bluesky_id"
  CodepenID = "your_codepen"
  CvURL = "your_cv_url"
  Email = "your_email"
  FacebookID = "your_facebook"
  GithubID = "your_github"
  GitlabId = "your_gitlab"
  # Uses keys.openpgp.org keyserver to search your fingerprint
  # https://keys.openpgp.org/search?q=your_gpg_fingerprint
  GnuPGFingerprint = "your_gpg_fingerprint"
  GoogleAnalytics = "your_google_analytics_id"
  GoogleplusID = "your_googleplus"
  InstagramID = "your_instagram"
  LinkedInID = "your_linkedin"
  MastodonURL = "your_mastodon_profile"
  MediumID = "your_medium_id"
  Mobile = "+1-201-555-0123"
  PayPalMeID = "https://www.paypal.me/..."
  Phone = "+1-201-555-0123"
  RedditID = "your_reddit"
  RSSURL = "\path-to-xml" ( default hugo generates from pages at "/index.xml" )
  SlackURL = "https://join.slack.com/..."
  SpotifyID = "your_spotify_id"
  SoundcloudID = "your_soundcloud_id"
  StackExchangeID = "your_stackexchange_id"
  StackOverflowID = "your_stackoverflow_id"
  TelegramID = "your_telegram"
  TwitterID = "your_twitter"
  TwitchID = "your_twitch_username"
  XingURL = "https://www.xing.com/profile/..."
  # For youtube, since there are multiple path urls please add everything after https://youtube.com/ in channel url
  YoutubeID = "c/your_youtube_id"
```

To add a menu item add `[[menu.header]]` item to `config.toml`. For example:

```
[menu]
  [[menu.header]]
    name = "posts"
    weight = 0
    url = "/posts"
```

To add a submenu item add `[[menu.header]]` item with a parent parameter to `config.toml`. For example:

```
[menu]
  [[menu.header]]
    identifier = "post"
    name = "posts"
    weight = 0
  [[menu.header]]
    parent = "post"
    name = "All Posts"
    url = "/posts"
  [[menu.header]]
    parent = "post"
    name = "categories"
    url = "/categories"
  [[menu.header]]
    parent = "post"
    name = "tags"
    url = "/tags"
```

To enable disqus comments add `disqusShortname` to your `config.toml`.

You can turn off disqus comments per page by adding `nocomments = true` to the front matter.

To disable the post date from a specific page add `showpostdate = false` to your relevant `.md` file.

Pages now also support ![Lastmod](https://gohugo.io/methods/page/lastmod/). This will not appear until you populate `lastmod:` in the page's frontmatter, unless you have `enableGitInfo` set to `true` in your site's config file, in which case it will use the date of the last git commit containing that page.

## License

Nix is licensed under the [MIT License](LICENSE.md)
