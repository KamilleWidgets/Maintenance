Maintenance
===============
2017-04-07



Widget for displaying a maintenance page.


This is a widget for the [kamille framework](https://github.com/lingtalfi/Kamille).


[![maintenance.png](https://s19.postimg.org/g16e6s9gj/maintenance.png)](https://postimg.org/image/kn2if4uzj/)

Install
===========
using the [kamille installer tool](https://github.com/lingtalfi/kamille-installer-tool)
```bash
kamille winstall Maintenance
```



Model
===========

This model contains the following variables:

- logo_src: the source for the logo 
- logo_alt: the alt text for the logo 
- main_text: the main text (Our website is currently down for maintenance.)
- aux_text: an auxiliary text (We expect to be back in a couple of hours. Thanks for your patience.)
- image_src: the source for the image 
- image_alt: the alt text for the image




Demo snippet
=========

```php
<?php


use Kamille\Architecture\ApplicationParameters\ApplicationParameters;

$theme = ApplicationParameters::get("theme");

$conf = [
    "layout" => [
        "tpl" => "splash/default",
    ],
    "widgets" => [
        "main.maintenance" => [
            "tpl" => "Maintenance/default",
            "conf" => [
                "logo_src" => "theme/$theme/widgets/maintenance/logo.png",
                "logo_alt" => "logo",
                "main_text" => "Our website is currently down for maintenance.",
                "aux_text" => "We expect to be back in a couple of hours. Thanks for your patience.",
                "image_src" => "theme/$theme/widgets/maintenance/maintenance.png",
                "image_alt" => "maintenance",
            ],
        ],
    ],
];
```







History Log
------------------

- 1.2.1 -- 2017-04-07

    - really removing laws conf file (forgot)

- 1.2.0 -- 2017-04-07

    - removed laws conf file, providing snippet in README instead

- 1.1.0 -- 2017-04-07

    - changed viewId to widget.maintenance
    
- 1.0.0 -- 2017-04-07

    - initial commit