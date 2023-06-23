# EMAIL Setup

After `mix phx.gen.auth Accounts User users --web Accounts`

```elixir
if config_env() == :prod or config_env() == :dev do
  # Configuring the mailer
  config :templatephx, Socrates.Mailer,
    adapter: Swoosh.Adapters.Sendgrid,
    api_key: System.get_env("SENDGRID_API_KEY")
  config :swoosh, :api_client, Swoosh.ApiClient.Finch
end
```