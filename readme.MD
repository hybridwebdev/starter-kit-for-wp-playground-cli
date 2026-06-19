# Starter Kit for WP Playground CLI

A quick-start template for setting up and running WordPress locally using the [WP Playground CLI](https://github.com/WordPress/wordpress-playground).

## What is This?

This starter kit provides a simple, automated way to:
- Initialize a WordPress environment locally
- Install themes and plugins (configured in `blueprint.json`)
- Run a local development server with WP Playground

Perfect for rapid WordPress development, theme testing, plugin development, and learning.

## Prerequisites

- **Node.js** (v14 or higher)
- **npm** (comes with Node.js)

## Quick Start

### 1. Clone or Use This Template
```bash
git clone https://github.com/hybridwebdev/starter-kit-for-wp-playground-cli.git
cd starter-kit-for-wp-playground-cli
```

### 2. Initialize WordPress Directory
```bash
npm run wp:init
```
This creates an `htdocs` directory where WordPress will be installed.

### 3. Install WordPress with Blueprint
```bash
npm run wp:install
```
This runs the blueprint configuration (installs themes, plugins, etc.) and sets up WordPress.

### 4. Start the Development Server
```bash
npm run wp:serve
```
The WordPress site will be available locally. Check the CLI output for the access URL.

## Configuration

### Customize Your WordPress Setup

Edit `install.json` to modify what gets installed:

```json
{
  "steps": [
    {
      "step": "installTheme",
      "themeData": {
        "resource": "wordpress.org/themes",
        "slug": "twentytwentyfive"
      }
    },
    {
      "step": "installPlugin",
      "pluginData": {
        "resource": "wordpress.org/plugins",
        "slug": "woocommerce"
      }
    }
  ]
}
```

You can Edit `serve.json` to modify settings used when ```run wp:serve``` is called:

```json
{
  "steps": [
    {
      "step": "defineWpConfigConsts",
      "consts": {
        "WP_DEBUG": true,
        "WP_DEBUG_LOG": true,
        "WP_DEBUG_DISPLAY": true,
        "WP_DISABLE_FATAL_ERROR_HANDLER": true
      }
    }
  ]
}
```

You can add or remove theme and plugin installation steps. See the [WP Playground Blueprint Documentation](https://developer.wordpress.org/playground/blueprints/) for more advanced configuration options.

## Scripts

- **`npm run wp:init`** – Creates the `htdocs` directory
- **`npm run wp:install`** – Installs WordPress and runs the blueprint
- **`npm run wp:serve`** – Starts the local development server

## Resources

- **[WP Playground Documentation](https://developer.wordpress.org/playground/)** – Official docs and API reference
- **[WP Playground CLI GitHub](https://github.com/WordPress/wordpress-playground)** – Source code and issues
- **[WordPress.org](https://wordpress.org/)** – Official WordPress site
- **[WordPress Developer Resources](https://developer.wordpress.org/)** – Developer documentation and plugins/themes directory

## Learn More

- [WP Playground Blueprints](https://developer.wordpress.org/playground/blueprints/) – Advanced configuration
- [WordPress Plugin Development](https://developer.wordpress.org/plugins/)
- [WordPress Theme Development](https://developer.wordpress.org/themes/)

## License

This starter kit is provided as-is. WordPress is GPL v2 or later.

## Contributing

Have suggestions or improvements? Feel free to open an issue or submit a pull request!
