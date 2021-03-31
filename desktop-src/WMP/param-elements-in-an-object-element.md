---
title: Элементы PARAM в элементе OBJECT
description: Элементы PARAM в элементе OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Проигрыватель Windows Media, элементы PARAM в элементе OBJECT
- Объектная модель проигрывателя Windows Media, элементы PARAM в элементе OBJECT
- Объектная модель, элементы PARAM в элементе OBJECT
- Проигрыватель Windows Media Mobile, элементы PARAM в элементе OBJECT
- Элемент управления ActiveX проигрывателя Windows Media, элементы PARAM в элементе OBJECT
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, элементы PARAM в элементе OBJECT
- Элемент управления ActiveX, элементы PARAM в элементе OBJECT
- внедрение, веб-страницы
- Внедрение веб-страниц, элементы PARAM в элементе OBJECT
- Элементы PARAM в элементе OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "103889283"
---
# <a name="param-elements-in-an-object-element"></a>Элементы PARAM в элементе OBJECT

Проигрыватель Windows Media использует элемент PARAM для определения определенных условий запуска элемента управления. Элемент PARAM внедряется в ОБЪЕКТный элемент.

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
| [Автозапуска](settings-autostart.md)                   | да               | да                                         | да                              |
| [между](settings-balance.md)                       | да               | да                                         | да                              |
| [baseURL](settings-baseurl.md)                       | да               | да                                         | да                              |
| [каптионингид](closedcaption-captioningid.md)        | да               | да                                         | да                              |
| [куррентмаркер](controls-currentmarker.md)           | да               | да                                         | да                              |
| [currentPosition](controls-currentposition.md)       | да               | да                                         | да                              |
| [дефаултфраме](settings-defaultframe.md)             | да               | Нет                                          | Нет                               |
| [енаблеконтекстмену](player-enablecontextmenu.md)     | да               | да                                         | да                              |
| [доступной](player-enabled.md)                         | да               | да                                         | да                              |
| [енаблиррордиалогс](settings-enableerrordialogs.md) | да               | да                                         | Нет                               |
| **Файлов**                                          | Нет                | да                                         | да                              |
| [fullScreen](player-fullscreen.md)                   | да               | Нет                                          | Нет                               |
| [инвокеурлс](settings-invokeurls.md)                 | да               | Нет                                          | Нет                               |
| [отключен](settings-mute.md)                             | да               | да                                         | да                              |
| [плайкаунт](settings-playcount.md)                   | да               | да                                         | Нет                               |
| [курсе](settings-rate.md)                             | да               | да                                         | да                              |
| [самифиленаме](closedcaption-samifilename.md)        | да               | да                                         | да                              |
| [самиланг](closedcaption-samilang.md)                | да               | да                                         | да                              |
| [самистиле](closedcaption-samistyle.md)              | да               | да                                         | да                              |
| **SRC**                                               | Нет                | да                                         | да                              |
| [стретчтофит](player-stretchtofit.md)               | да               | да                                         | Нет                               |
| [URL-адрес](player-url.md)                                 | да               | да                                         | да                              |
| [тома](settings-volume.md)                         | да               | да                                         | да                              |
| [виндовлессвидео](player-windowlessvideo.md)         | да               | да                                         | да                              |



 

> [!Note]  
> Элементы параметров **filename** и **src** поддерживаются подключаемым модулем Firefox, но не Internet Explorer. Они выполняют ту же функцию, что и элемент param параметра **URL-адреса** .

 

Дополнительные сведения о значениях для каждого атрибута Name см. в [справочнике по объектной модели](object-model-reference-for-scripting.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media на веб-странице**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




