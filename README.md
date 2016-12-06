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
  GithubID = "your_github"
  TwitterID = "your_twitter"
  LinkedInID = "your_linkedin"
  GoogleplusID = "your_googleplus"
  FacebookID = "your_facebook"
  Name = "your_name"
  HeaderUsername = "username"
  HeaderHostname = "hostname"
  Email = "your_email"
  About = "info_about_you"
  ProfilePicture = "profile_picture_url"
  GoogleAnalytics = "your_google_analytics_id"
```

Edit them as needed. If you don't want one of the social networks simply delete that line. `HeaderUsername` and `HeaderHostname` will be displayed in navbar on left side in the format: `HeaderUsername@HeaderHostname ~ $`

To add a menu item add `[[menu.header]]` item to `config.toml`. For example:

```
[menu]
  [[menu.header]]
    name = "posts"
    weight = 0
    url = "/posts"
```

To enable disqus comments add `disqusShortname` to your `config.toml`.

You can turn off disqus comments per page by adding `nocomments = true` to the front matter.

## License

Nix is licensed under the [MIT License](LICENSE.md) 
