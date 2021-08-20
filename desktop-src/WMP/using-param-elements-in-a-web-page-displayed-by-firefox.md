---
title: Использование элементов PARAM на веб-странице, отображаемой Firefox
description: Использование элементов PARAM на веб-странице, отображаемой Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
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
- проигрыватель Windows Media, Firefox
- объектная модель проигрыватель Windows Media, Firefox
- Объектная модель, Firefox
- проигрыватель Windows Media Mobile, Firefox
- проигрыватель Windows Media ActiveX элемент управления, Firefox
- проигрыватель Windows Media мобильный ActiveX элемент управления, Firefox
- ActiveX элемент управления, Firefox
- Firefox, элементы PARAM в элементе OBJECT
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767b9b0d5e4367a17f07f68600ff8e9cac488ca9e4c950165d84677fd7d03956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117309"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Использование элементов PARAM на веб-странице, отображаемой Firefox

Элементы PARAM можно использовать внутри элемента OBJECT для задания начального состояния элемента управления проигрывателя. Например, элементы PARAM в следующем примере указывают, что элемент управления должен автоматически воспроизводиться в Сиэтле. WMV.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



Большинство элементов PARAM можно интерпретировать с помощью Internet Explorer и Firefox. Однако существует несколько элементов PARAM, которые не поддерживаются подключаемым модулем Firefox. Сведения о том, какие элементы PARAM поддерживаются подключаемым модулем Firefox, см. [в разделе элементы param в ЭЛЕМЕНТЕ Object](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**использование элемента управления проигрыватель Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




