![TechMarket](https://i.imgur.com/2pNzJ6e.png)

### Events
Component can be extended with [Events](https://octobercms.com/docs/services/events).

**planetadeleste.techmarket.on_run**   
This event allows you to send a response to component method `onRun`.   
If response is an instance of `\Illuminate\Http\RedirectResponse`, page will be redirected to response.

```php
    Event::listen(\PlanetaDelEste\TechMarket\Components\ToolBox::EVENT_TM_ONRUN, function($pageId, $page) {
        if($pageId === 'redirect_me') {
            return redirect('/home');
        }
    });
```

| **Parameter** | **Type** | **Description** |
|---------------|----------|-----------------|
| `$pageId` | `String` | Page ID |
| `$page` | `\Cms\Classes\CodeBase` | Page object |

**planetadeleste.techmarket.on_control_bar**   
This event allows you to add your own code in search pages.  
This event is fired on `\PlanetaDelEste\TechMarket\Components\ToolBox::onControlBar` method.   
Must need to return a `\Lovata\Shopaholic\Classes\Collection\ProductCollection` instance

```php
    Event::listen(\PlanetaDelEste\TechMarket\Components\ToolBox::EVENT_TM_CONTROLBAR, function($component, $pageId, $productList) {
        // Your own search methods

        return $productList;
    });
```

| **Parameter** | **Type** | **Description** |
|---------------|----------|-----------------|
| `$component` | `\PlanetaDelEste\TechMarket\Components\ToolBox` | ToolBox instance |
| `$pageId` | `String` | Page ID |
| `$productList` | `\Lovata\Shopaholic\Classes\Collection\ProductCollection` | ProductCollection instance |
