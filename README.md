# Blade Feather Icons

<a href="https://packagist.org/packages/outhebox/blade-feather-icons">
    <img src="https://poser.pugx.org/outhebox/blade-feather-icons/v/stable.svg" alt="Latest Stable Version">
</a>
<a href="https://packagist.org/packages/outhebox/blade-feather-icons">
    <img src="https://poser.pugx.org/outhebox/blade-feather-icons/d/total.svg" alt="Total Downloads">
</a>

A package to easily make use of [Feather Icons](https://github.com/feathericons/feather) in your Laravel Blade views.

For a full list of available icons see [the SVG directory](resources/svg) or preview them at [feathericons.com](https://feathericons.com/).

## Requirements

- PHP 7.2 or higher
- Laravel 7.14 or higher

## Installation

```bash
composer require outhebox/blade-feather-icons
```

## Usage

Icons can be used a self-closing Blade components which will be compiled to SVG icons:

```blade
<x-feather-alert-triangle/>
```

You can also pass classes to your icon components:

```blade
<x-feather-alert-triangle class="text-primary"/>
```

And even use inline styles:

```blade
<x-feather-alert-triangle style="color: #555"/>
```

### Raw SVG Icons

If you want to use the raw SVG icons as assets, you can publish them using:

```bash
php artisan vendor:publish --tag=blade-feather-icons --force
```

Then use them in your views like:

```blade
<img src="{{ asset('vendor/blade-feather-icons/alert-triangle.svg') }}" width="25" height="25"/>
```

### Update your Feather icons to the latest version

Install the feather icons npm library
```
npm install feather-icons --save
```

Then copy this line to your webpack.mix file
```
mix.copy('node_modules/feather-icons/dist/icons', 'public/vendor/feather-icons');
```

### Blade Icons

Blade Feather Icons uses Blade Icons under the hood. Please refer to [the Blade Icons readme](https://github.com/blade-ui-kit/blade-icons) for additional functionality.

## Credits

- [Dries Vints](https://driesvints.com)
- [Bruno Falcão](https://github.com/brunocfalcao)
- [Mohamed Ashraf](https://github.com/MohmmedAshraf)
- [All contributors](https://github.com/MohmmedAshraf/blade-feather-icons/contributors)

## License

Blade Feather Icons is open-sourced software licensed under [the MIT license](LICENSE.md).
