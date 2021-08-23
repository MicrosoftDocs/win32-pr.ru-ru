---
title: Элементы PARAM в элементе OBJECT
description: Элементы PARAM в элементе OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- проигрыватель Windows Media, элементы PARAM в элементе OBJECT
- проигрыватель Windows Media объектная модель, элементы PARAM в элементе object
- Объектная модель, элементы PARAM в элементе OBJECT
- проигрыватель Windows Media Мобильные, элементы PARAM в элементе OBJECT
- проигрыватель Windows Media ActiveX элемент управления, элементы PARAM в элементе OBJECT
- проигрыватель Windows Media мобильный ActiveX элемент управления, элементы PARAM в элементе OBJECT
- элемент управления ActiveX, элементы PARAM в элементе OBJECT
- внедрение, веб-страницы
- Внедрение веб-страниц, элементы PARAM в элементе OBJECT
- Элементы PARAM в элементе OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054432"
---
# <a name="param-elements-in-an-object-element"></a>Элементы PARAM в элементе OBJECT

проигрыватель Windows Media использует элемент PARAM для определения определенных условий запуска для элемента управления. Элемент PARAM внедряется в ОБЪЕКТный элемент.

Например, если необходимо определить, имеет ли свойство **автозапуска** значение true, элемент param следует встроить ВНУТРЬ элемента Object.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



В элементе OBJECT можно использовать столько элементов PARAM, сколько требуется. Параметр PARAM имеет два атрибута: Name и value. Необходимо задать оба атрибута.

Поддерживаемые атрибуты PARAM несколько разных браузеров и типов MIME. В следующей таблице показаны атрибуты, поддерживаемые браузерами Internet Explorer и Firefox. Предпочтительным типом MIME для браузера Firefox является Application/x-MS-WMP, однако существует несколько других типов MIME, которые можно использовать для внедрения элемента управления проигрывателя в веб-страницу, размещенную в браузере Firefox. В четвертом столбце таблицы показаны атрибуты, которые поддерживаются при использовании типа MIME, отличного от Application/x-MS-WMP.



| Имя параметра                                            | Internet Explorer | Firefox с типом MIME application/x-MS-WMP | Firefox с любым другим типом MIME |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Автозапуска](settings-autostart.md)                   | Да               | Да                                         | Да                              |
| [между](settings-balance.md)                       | Да               | Да                                         | Да                              |
| [baseURL](settings-baseurl.md)                       | Да               | Да                                         | Да                              |
| [каптионингид](closedcaption-captioningid.md)        | Да               | Да                                         | Да                              |
| [куррентмаркер](controls-currentmarker.md)           | Да               | Да                                         | Да                              |
| [currentPosition](controls-currentposition.md)       | Да               | Да                                         | Да                              |
| [дефаултфраме](settings-defaultframe.md)             | Да               | Нет                                          | Нет                               |
| [енаблеконтекстмену](player-enablecontextmenu.md)     | Да               | Да                                         | Да                              |
| [enabled](player-enabled.md)                         | Да               | Да                                         | Да                              |
| [енаблиррордиалогс](settings-enableerrordialogs.md) | Да               | Да                                         | Нет                               |
| **fileName**                                          | Нет                | да                                         | Да                              |
| [fullScreen](player-fullscreen.md)                   | Да               | Нет                                          | Нет                               |
| [инвокеурлс](settings-invokeurls.md)                 | Да               | Нет                                          | Нет                               |
| [отключен](settings-mute.md)                             | Да               | Да                                         | Да                              |
| [плайкаунт](settings-playcount.md)                   | Да               | Да                                         | Нет                               |
| [курсе](settings-rate.md)                             | Да               | Да                                         | Да                              |
| [самифиленаме](closedcaption-samifilename.md)        | Да               | Да                                         | Да                              |
| [самиланг](closedcaption-samilang.md)                | Да               | Да                                         | Да                              |
| [самистиле](closedcaption-samistyle.md)              | Да               | Да                                         | Да                              |
| **SRC**                                               | Нет                | да                                         | Да                              |
| [стретчтофит](player-stretchtofit.md)               | Да               | Да                                         | Нет                               |
| [URL-адрес](player-url.md)                                 | Да               | Да                                         | Да                              |
| [volume](settings-volume.md)                         | Да               | Да                                         | Да                              |
| [виндовлессвидео](player-windowlessvideo.md)         | Да               | Да                                         | Да                              |



 

> [!Note]  
> Элементы параметров **filename** и **src** поддерживаются подключаемым модулем Firefox, но не Internet Explorer. Они выполняют ту же функцию, что и элемент param параметра **URL-адреса** .

 

Дополнительные сведения о значениях для каждого атрибута Name см. в [справочнике по объектной модели](object-model-reference-for-scripting.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**использование элемента управления проигрыватель Windows Media на веб-странице**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




