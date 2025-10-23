> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# XWiki for Platform.sh

This project provides a starter kit for XWiki projects hosted on Platform.sh.  It includes and automatically configures a PostgreSQL database for storage.  XWiki itself is downloaded during the build step.  It is run using Jetty.

XWiki is a free wiki software platform written in Java with a design emphasis on extensibility. XWiki is an enterprise wiki. It includes WYSIWYG editing, OpenDocument based document import/export, semantic annotations and tagging, and advanced permissions management.

## Features

* Java 11
* PostgreSQL 11
* Automatic TLS certificates
* Maven-based build

## Customizations

* [`.platform/routes.yaml`](.platform/routes.yaml): Platform.sh allows you to define the [routes](https://docs.platform.sh/configuration/routes.html).
* [`.platform/services.yaml`](.platform/services.yaml):  Platform.sh allows you to completely define and configure the topology and [services you want to use on your project](https://docs.platform.sh/configuration/services.html).
* [`.platform.app.yaml`](.platform.app.yaml): You control your application and the way it will be built and deployed on Platform.sh [via a single configuration file](https://docs.platform.sh/configuration/app-containers.html).

> **note**
>
> This template must be initialized on a *Large* Platform.sh plan, due to XWiki's [minimum memory requirements](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Performances/#HMemory).
>
> After the project has been initialized, make sure to [increase the size of your application containers on development environments](https://platform.sh/blog/2019/supersize-app-containers-in-your-dev-environments/) as well.


## References

* [XWiki](https://www.xwiki.org/xwiki/bin/view/Main/WebHome)
* [Java at Platform.sh](https://docs.platform.sh/languages/java.html)
