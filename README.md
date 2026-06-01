# bsp-stm32mp25-dk

Board support for the STM32MP25 Discovery Kit (STM32MP257F-DK)

## Using this extension

`bsp-stm32mp25-dk` is an [Avocado](https://avocadolinux.org) extension — a reusable fragment of
build- and runtime-configuration that you compose into your own Avocado project. To use it,
declare it as a package-sourced extension in your `avocado.yaml` and add it to a runtime:

```yaml
extensions:
  avocado-bsp-stm32mp25-dk:
    source:
      type: package
      version: "*"        # or pin an exact version

runtimes:
  my-runtime:
    extensions:
      - avocado-bsp-stm32mp25-dk
```

Then `avocado build`. The extension's config is fetched from your target's package feed
and merged into your project at build time.
