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
  CodepenID = "your_codepen"
  CvURL = "your_cv_url"
  Email = "your_email"
  FacebookID = "your_facebook"
  GithubID = "your_github"
  GitlabId = "your_gitlab"
  GnuPGFingerprint = "your_gpg_fingerprint"
  GoogleAnalytics = "your_google_analytics_id"
  GoogleplusID = "your_googleplus"
  InstagramID = "your_instagram"
  LinkedInID = "your_linkedin"
  MastodonURL = "your_mastodon_profile"
  Mobile = "+1-201-555-0123"
  PayPalMeID = "https://www.paypal.me/..."
  Phone = "+1-201-555-0123"
  RedditID = "your_reddit"
  SlackURL = "https://join.slack.com/..."
  StackExchangeID = "your_stackexchange_id"
  StackOverflowID = "your_stackoverflow_id"
  TelegramID = "your_telegram"
  TwitterID = "your_twitter"
  XingURL = "https://www.xing.com/profile/..."
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

## License

Nix is licensed under the [MIT License](LICENSE.md)
