
## New Relic Sidekiq Plugin

Monitors Sidekiq, a library for processing background jobs.

  - Pending jobs number
  - Total failed jobs number
  - Number of processed jobs

### Requirements

In order to use this plugin, you must have an active New Relic account.
Also, you should be able to use **json-1.8.0**, since it is required by **newrelic_plugin** gem.

  - Ruby (>= 1.8.7)
  - Bundler
  - Sidekiq
  - Json (= 1.8.0)


### Installation

1. Run `bundle install` to install required gems
2. Copy `config/newrelic_plugin.yml.example` to `config/newrelic_plugin.yml`
3. Edit `config/newrelic_plugin.yml` and replace "YOUR_LICENSE_KEY_HERE" with your New Relic license key

### Running 

In order to check your configuration, you can launch the plugin
in foreground mode, with all output going to stdout:

    ./newrelic_sidekiq_agent

Carefully check plugin's output for any possible error messages.
In case of success, collected data should appear in the New Relic
user interface shortly after starting.

Plugin can also be started as a daemon using the following command:

    ./newrelic_sidekiq_agent.daemon start

In this case you can check its status by running

    ./newrelic_sidekiq_agent.daemon status

and stop it with

    ./newrelic_sidekiq_agent.daemon stop

### Licensing

This project was **forked** from [mscifo/newrelic_sidekiq_agent](https://github.com/mscifo/newrelic_sidekiq_agent) and it is under the *MIT License*. 

