# How to use this project

```hcl-terraform
provider discord {
  token = var.discord_token
}

data discord_local_image logo {
  file = "logo.png"
}

resource discord_server my_server {
  name = "My Awesome Server"
  region = "us-west"
  default_message_notifications = 0
  icon_data_uri = data.discord_local_image.logo.data_uri
}
```

## Argument Reference

The Discord provider supports the following arguments:

- `token` - The token of the bot that will be accessing the API
- `client_id` - Currently unused
- `secret` - Currently unused
