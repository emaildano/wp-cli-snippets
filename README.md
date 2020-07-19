# WP CLI Snippets

### Set all draft posts to publish.

Change post type by updating the `--post_type` flag.

```
wp post list --skip-plugins --skip-themes --post-status=draft --post_type=post --format=ids | xargs -d ' ' -I % wp post update % --post_status=publish
```