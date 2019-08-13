![TechMarket](https://i.imgur.com/2pNzJ6e.png)

### Slider and Banners Home v2
![home-v2-banners-block](https://s.nimbusweb.me/attachment/3189195/17cxiwm0rfbrd13q7h7n/yVLn24WLeJCxNMQw/screenshot-shop.teros.uy-2019.08.12-20_50_29.png)

```twig
<div class="slider-block column-1-slider-block ">
    {% partial 'components/banner/banner-slider'
        size = '1016x532'
        slideClass = 'home-v2-slider'
        multi = true
    %}
</div>
<div class="banners-block column-2-banners-block">
    {% partial 'components/banner/banner-bg' 
        size  = '414x256' 
        multi = true
        take  = 2
    %}
</div>
```
##### For slider, load all banners with `Size` name of `1016x532`.

![Slider 01](https://s.nimbusweb.me/attachment/3189213/dm3xrtthxlwoyv5ho32d/NEpv5Gzor9XoMMZs/screenshot-shop.teros.uy-2019.08.12-21_08_32.png)

| **Field** | **Text/Setting** |
|-----------|------------------|
| **Title** | *The new-tech gift you are wishing for is right here* |
| **Sub Title** | *Big screens in incredibly slim designs that in your hand.* |
| **Text Position** | *Left* |
| **Bottom Text** | *Free shipping on US Terority* |
| **Button label** | *Browse now* |
| **Icon button** | *Long Arrow Right* |
| **Link type** | *Shopaholic Product* |
| **Shopaholic Product** | *Choose any* |
| **Image** | *Cellphones* |
| **Background** | *UX image* |

##### For background banners, take only first two

![banner 01](https://s.nimbusweb.me/attachment/3189201/dapy2vcoc7x0y4zg637s/t84T14C9KyHOSL2k/screenshot-shop.teros.uy-2019.08.12-21_00_38.png)

| **Field** | **Text/Setting** |
|-----------|------------------|
| **Sub Title** | *Best Gift Idea* |
| **Title** | *Mini Two Wheel Self Balancing Scooter* |
| **Text Position** | *Left* |
| **Link type** | *Shopaholic Product* |
| **Shopaholic Product** | *Choose any* |
| **Background** | *Scooter image* |