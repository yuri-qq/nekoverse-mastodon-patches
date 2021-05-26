# nekoverse-mastodon-patches
Mastodon currently overwhelmingly fails vibe check.
These patches try to correct that.

They are applied on my Mastodon instance [social.nekover.se](https://social.nekover.se).

## Applying the patches

To apply a patch run:
```shell
$ git apply 000_placeholder.patch
```

After the desired patches are applied, run the following commands to rebuild the Mastodon assets:
```
$ npm run build:production
$ RAILS_ENV=production bundle exec rails assets:precompile
$ RAILS_ENV=production bin/tootctl cache clear
```
