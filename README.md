# RESTKit-Dubbo

[简体中文](./README.zh_CN.md)

[RESTKit-Dubbo](https://plugins.jetbrains.com/plugin/18828-restkit-dubbo) is a plugin that support Dubbo scanning and request for [RESTKit](https://plugins.jetbrains.com/plugin/14723-restkit) plugin from version 2.0.0.


> Note  
> RESTKit plugin has provided extension point from version 2.0.0. You can also support your web framework restful apis like this plugin.

If this plugin helps, please **🌟Star**! If you have any good idea, please let me know.

## Features
- Support most RESTKit features.
- Support scanning dubbo services in java project.
- Support sending dubbo request.
- Support jumping to tree in the dubbo method from service impl.

## Install
- **Using IDE plugin system**

Recommended <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Browse repositories...</kbd> > <kbd>find "RESTKit-Dubbo"</kbd> > <kbd>Install Plugin</kbd>

- **Local Install**

Download plugin form <kbd>distributions/RESTKit-Dubbo-x.x.x.zip</kbd>, then <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Install Plugin from Disk...</kbd>

## Usage
After installed this plugin, you should enable it in `RESTKit` setting. Refresh in `RESTKit` window.

![enable](./.images/setting.png)

You will see.

![plugin](./.images/plugin.png)

UI introduction:

- Config: request config for dubbo, can use environment variable. Content:
  - registry: registry address, support zookeeper only. The default is `{{registry}}`. Without this pair or env variable, will use`zookeeper://127.0.0.1:2181`.
  - url: dubbo direct url like `dubbo://127.0.0.1:20880`. The default is `{{url}}`. Without this pair or env variable, will not use.
  - timeout: request timeout, the default is 2000ms. Without this pair, will use 5000ms.
  - applicationName: the default is RESTKit-Dubbo-proxy.
  - retries: the default is 0.
  - check: the default is false.
  - loadbalance: no default.
- Headers: use as dubbo attachments.
- Params: useless, just ignore.
- Body: dubbo generic request content, can't use env variable.
- Response：response content.
- Info：request and response info.