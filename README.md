# freebox
Better HomeAssistant freebox integration

Forked from the [official Freebox Integration](https://www.home-assistant.io/integrations/freebox/), but due to the lack of maintainment and pull request validation, I've decided to fork it and do my own modifications, specific to my need.

## Fix
- Fix non reuse of service name

When running HomeAssistant in a docker container, when the container is beeing recreated after an update, the integration fails because it uses `gethostname()`, which changes after each creation.

## Features
- Specify custom service name

Instead of using `gethostname()`, add the possibility to specify a user service name. That same name will be displayed on the freebox's web interface

- Change polling rate

30s by default. Can be changed

