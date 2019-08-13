![TechMarket](https://i.imgur.com/2pNzJ6e.png)

## Fields
![Preview](https://s.nimbusweb.me/attachment/3179291/vtp462itv1xtxi6sud6i/muTDVTnKpDRfn2Sz/screenshot-shop.teros.uy-2019.08.09-06-06-24.png)

The banner has only two required fields, `Title` and `Size`.  
Below are all model fields.

| **Field** | **Description** |
|-----------|-----------------|
| Size | Choose the banner size |
| Pre Title | This text are always smallest than `Title` and is up.|
| Title | Basic HTML text, used as main banner text |
| Sub Title | Subtitle is located under the title |
| Text Position | Where to place the texts in the banner. Possible values are `Left`, `Right` or `Center` |
| Offer Price | Text describing some offer. Ex. *up to 70% sale* |
| Button label | Label text of action button |
| Bottom text | A small text placed at bottom of banner |
| Icon button | Choose an icon for action button |
| Link type | Choose an option of type of link on action button. |
| | `None` hide the button. |
| | `Shopaholic Product` display a field to select the product to be linked by action button. |
| | `CMS Page` display a selection to choose the page to link. |
| | `Write the Url manually` display a field to enter a custom URL. |
| Image | Upload an image to your banner. If `Text Position` value is `left` or `right`, image are place in the opposite side. |
| Background | Upload a background image to your banner.<br>**Important**: In theme, there are banners that require of background image  |


## Usage

There are two partials for calling banners.

### Background banners
This partial load only banners with background image.  
Placed in `/themes/planetadeleste-techmarket-store/partials/components/banner/banner-bg.htm`

```twig
    {% partial 'components/banner/banner-bg'
        size     = '300x204'
        multi    = true
        take     = 4
        wrapper  = 'cssWrapperClass'
        cssClass = 'cssCustomClass'
    %}
```
| **Field** | **Description** |
|-----------|-----------------|
| `size` | Size model by name |
| `multi` | Boolean. If `true`, render multiple banners with same settings. |
| `take` | Number. How many banners to load. Only works if `multi` is `true` |
| `wrapper` | If is defined, create a wrapper div with `wrapper` css class |
| `cssClass` | Define a custom css class for main banner element |

### Slide banners
This partial make a slider of banners.   
There isn't a `take` option in this banner. If `multi` is `true`, all banners with same `size` will be loaded.   
Placed in `themes/planetadeleste-techmarket-store/partials/components/banner/banner-slider.htm`

```twig
    {% partial 'components/banner/banner-slider'
        size = '1200x350'
        slideClass = 'home-v6-slider'
        multi = true
    %}
```
| **Field** | **Description** |
|-----------|-----------------|
| `size` | Size model by name |
| `multi` | Boolean. If `true`, render multiple banners with same settings. |
| `slideClass` | Define a custom css class for main banner slide element |