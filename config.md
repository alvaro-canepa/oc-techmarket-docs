![TechMarket](https://i.imgur.com/2pNzJ6e.png)

## Theme Settings

Go to `Settings` > `CMS` > `Front-end-theme`   
Click on `Customize` button, from `TechMarket` theme.

### Styles & Assets

#### Color Style
You can choose a base color for header, buttons, and other widgets.
Select from **Blue**, **Green**, **Flat Green**, **Orange**, **Red** or **Yellow**

#### Home Layout
Select the home/shop layout. 

**8 different homes**
![Homes v1 - v4](https://i.imgur.com/B5XDs6v.png)
![Homes v5 - v8](https://i.imgur.com/ikCq4nb.png)

**6 different markets**   
![Thumb - Electronic Market](https://i.imgur.com/3KVXVgi.png)
![Thumb - Garden Market](https://i.imgur.com/B5f0ZKi.png)
![Thumb - Shoes Market](https://i.imgur.com/aoWjbjZ.png)
![Thumb - Sports Market](https://i.imgur.com/3ghOWwZ.png)
![Thumb - Organic Market](https://i.imgur.com/2RkrbPB.png)
![Thumb - Multi Market](https://i.imgur.com/UmY4rH8.png)

#### Other options

- **Load OctoberCMS Front-end Javascript Framework**   
    If checked, load `framework extras` script.
```twig
    {% framework extras %}
```
- **Show Primary Menu**   
    Force to load primary menu. Only affect to "Home 5", "Home 6" and "Home 14".  
    **Important**: Require `StaticPage` Menu component with "primaryMenu" alias.
- **Animate CSS**   
    Load [`Animate.css`](https://daneden.github.io/animate.css/) library
- **Will load js and css using the .min. prefix on layout**   
    If checked, load all js and css libraries minified. Use it on production.


----------


### Contact Us Page
Select one of two different layouts
![Contact v1 and v2](https://i.imgur.com/ELZlA3q.png)

Write all fields below. 

**Note**: for use google maps, you need to setup your `Google API key` in `PlanetaDelEste.Widgets` plugin.


----------


### About Us Page
![About Us](https://s.nimbusweb.me/attachment/3194120/vmsenzd4rrikwpx3rr4v/cDazhABgTSaA2WS6/screenshot-shop.teros.uy-2019.08.14-03_26_22.png)
- Upload header image
- Add features (Title, Description and Image)
- Add Team Members (Name, Description and Image)
- Add Text boxes (Title and Description)
- Accordion Title
- Add Accordion boxes (Title and Description)


----------


### Landing Page
You  have an option to use landing pages or not.   
If choose to use landing pages,  there are two different options for design.
![Landing v1 and v2](https://i.imgur.com/cO66uy8.png)


----------


### Product Page
Choose the product page layout:

**Full Width**
![Fullwidth](https://i.imgur.com/AjPHUC2.png)

**Extended**
![Extended](https://i.imgur.com/2xHZzIa.png)

**Sidebar**
![Sidebar](https://i.imgur.com/NIJXwpB.png)


----------


### Shop/Catalog Page
**Use as catalog only**   
You have the option to switch to catalog mode. By doing this you hide the prices, add to cart buttons and minicart element and turn your solution into a shop for showcasing your products. You don’t have to alter any html or remove any components to do this.

**Shop/Catalog Layouts**   
Choose one of four shop layouts
![Shop Listing](https://i.imgur.com/f4CgfJ4.png)

**Default listing view**   
Select between five listing view layouts. Users can change listing layout by click on navigation icons.

**Grid**   
![Thumb - Grid](https://i.imgur.com/PdK0xP3.png)

**Grid Extended**   
![Thumb - Grid Extended](https://i.imgur.com/94yLnc4.png)

**List View**   
![Thumb - List View](https://i.imgur.com/bB1oWn9.png)

**List View Large**   
![Thumb - List View Large](https://i.imgur.com/mcDrt1A.png)

**List View Small**   
![Thumb - List View Small](https://i.imgur.com/lC0BMjt.png)


----------


## Assets

Custom sass/scss and javascript files can be easily compiled with ![Prepros](https://prepros.io/img/icon.png) [Prepros](https://prepros.io/)

### Sass/Scss
Css is based on Bootstrap 4  
You can customize the entire site, changing scss files, from `assets/sass` directory.

Change base colors from `_variables.scss`

```sass
// base color scheme
$body-background: #ffffff;
$primary-color: #0063d1;
$secondary-btn-color: #444444;
$color_body: #43454b;
$color_links: #2c2d33;
$color_border: rgba(0, 0, 0, 0.05);
$color_woocommerce: #fed700;
$error: #e2401c;
$success: #0f834d;
$info: #3d9cd2;
```

Selecting color from `CMS` settings, use one of `assets/css/color/` files

```twig
{# partials/common/head.htm #}
{% set cssFiles = cssFiles|merge(['assets/css/style.css', 'assets/css/colors/'~ this.theme.primary_color|default('blue') ~'.css']) %}
```

```sass
// assets/sass/colors/blue.scss

/*==============================*/
/*  Blue Color
/*==============================*/
@import '../bs-variables';
@import '../variables';
@import '../mixins';

$primary-color: #0063d1;

@import 'color';
```

All css files are added to theme in `partials/common/head.htm`

```twig
{% set cssFiles = [
    'assets/vendor/bootstrap/css/bootstrap.min.css',
    'assets/vendor/bootstrap/css/bootstrap-grid.min.css',
    'assets/vendor/bootstrap/css/bootstrap-reboot.min.css',
    'assets/css/font-awesome.min.css',
    'assets/css/font-techmarket.css',
    'assets/css/slick.css',
    'assets/css/techmarket-font-awesome.css',
    'assets/css/slick-style.css',
    'assets/vendor/lity/lity.min.css',
    'assets/vendor/hover/hover.min.css',
    'assets/vendor/flag-icon-css/css/flag-icon.min.css'
] %}
```

### Javascript

Javascript files are separated by module, to be edited more easily.   
There are located in `assets/js/techmarket/includes`.   
I use *Prepros* to join files and make `assets/js/techmarket.js` and `assets/js/techmarket.min.js`

```js
//  assets/js/techmarket/techmarket.js
//@prepros-prepend includes/_functions.js
//@prepros-prepend includes/_blockui.js
//@prepros-prepend includes/_wc_tabs.js
//@prepros-prepend includes/_yt_videos.js
//@prepros-prepend includes/_add_to_cart.js
//@prepros-prepend includes/_control_bar.js
//@prepros-prepend includes/_availability.js
//@prepros-prepend includes/_countdown.js
//@prepros-prepend includes/_category_filter.js
//@prepros-prepend includes/_filters.js
//@prepros-prepend includes/_global_window_events.js
//@prepros-prepend includes/_price_filter.js
//@prepros-prepend includes/_flex_menu.js
//@prepros-prepend includes/_product_category_toggle.js
//@prepros-prepend includes/_add_to_wishlist.js
//@prepros-prepend includes/_slick_carousel.js
//@prepros-prepend includes/_sticky_header.js
//@prepros-prepend includes/_departments_menu.js
//@prepros-prepend includes/_home_slider.js
//@prepros-prepend includes/_reviews.js
//@prepros-prepend includes/_account.js
//@prepros-prepend includes/_handheld_menu.js
//@prepros-prepend includes/_login.js
```

All js files are added to theme in `partials/common/scripts.htm`

```twig
{# partials/common/scripts.htm #}

{% set jsMin = this.theme.use_minified ? '.min' : '' %}
{% set jsFiles = [
    'assets/js/tether'~ jsMin ~'.js',
    'assets/vendor/bootstrap/js/bootstrap.bundle'~ jsMin ~'.js',
    'assets/js/jquery-migrate.min.js',
    'assets/js/hidemaxlistitem.min.js',
    'assets/js/jquery-ui.min.js',
    'assets/js/hidemaxlistitem.min.js',
    'assets/js/jquery.easing.min.js',
    'assets/js/scrollup.min.js',
    'assets/js/jquery.waypoints.min.js',
    'assets/js/waypoints-sticky.min.js',
    'assets/js/pace.min.js',
    'assets/js/slick.min.js',
    'assets/js/jquery.blockUI.js',
    'assets/vendor/lity/lity'~ jsMin ~'.js',
    'assets/js/techmarket'~ jsMin ~'.js'
] %}
```