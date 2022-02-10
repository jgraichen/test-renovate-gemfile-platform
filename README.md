# Test Renovate with Platforms in Gemfile.lock

Rubygems/Bundler support multiple platforms for choosing native gems to install. Such platforms can be added using `bundle lock --add-platform`.

```
bundle lock --add-platform ruby
bundle lock --add-platform x86_64-darwin-19
bundle lock --add-platform x86_64-darwin-20
bundle lock --add-platform x86_64-darwin-21
```

## Issue description

It appears that Renovatebot removes all platforms except x86-64-linux when doing lockfile maintenance.