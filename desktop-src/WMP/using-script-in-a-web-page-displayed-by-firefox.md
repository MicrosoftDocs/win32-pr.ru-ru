---
title: Использование сценария на веб-странице, отображаемой Firefox
description: Использование сценария на веб-странице, отображаемой Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX, веб-страницы
- Элемент управления ActiveX проигрывателя Windows Media, пример сценария
- Элемент управления ActiveX проигрывателя Windows Media для мобильных устройств, пример сценария
- Элемент управления ActiveX, пример сценария
- внедрение, веб-страницы
- Внедрение веб-страниц, пример сценария
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, пример сценария
- Внедрение веб-страниц, Firefox
- Пример сценария для внедрения веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105700727"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Использование сценария на веб-странице, отображаемой Firefox

Скрипт на веб-странице может использовать объектную модель проигрывателя для управления проигрывателем при взаимодействии пользователя со страницей. Например, следующий элемент INPUT содержит сценарий, который задает громкость проигрывателя.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Многие объекты в объектной модели проигрывателя Windows Media поддерживаются Internet Explorer и подключаемым модулем Firefox. Тем не менее некоторые объекты не поддерживаются подключаемым модулем Firefox. В следующей таблице перечислены все объекты в объектной модели проигрывателя и показано, какие объекты поддерживаются подключаемым модулем Firefox.



| Объект                                              | Поддержка Firefox |
|-----------------------------------------------------|-----------------|
| [ROM](cdrom-object.md)                           | Нет              |
| [кдромколлектион](cdromcollection-object.md)       | Нет              |
| [клоседкаптион](closedcaption-object.md)           | да             |
| [Элементы управления](controls-object.md)                     | Нет              |
| [ОПТИЧЕСКИ](dvd-object.md)                               | Нет              |
| [Ошибка](error-object.md)                           | да             |
| [ерроритем](erroritem-object.md)                   | да             |
| [Носитель](media-object.md)                           | да             |
| [медиаколлектион](mediacollection-object.md)       | Нет              |
| [метадатапиктуре](metadatapicture-object.md)       | Нет              |
| [метадататекст](metadatatext-object.md)             | Нет              |
| [Network](network-object.md)                       | да             |
| [Игрок](player-object.md)                         | да             |
| [PlayerApplication](playerapplication-object.md)   | Нет              |
| [Списком](playlist-object.md)                     | да             |
| [плайлистаррай](playlistarray-object.md)           | Нет              |
| [плайлистколлектион](playlistcollection-object.md) | Нет              |
| [Запрос](query-object.md)                           | Нет              |
| [Параметры](settings-object.md)                     | да             |
| [StringCollection](stringcollection-object.md)     | Нет              |



 

Подключаемый модуль Firefox поддерживает объект **Player** , но некоторые свойства объекта **Player** возвращают **значение NULL** в браузере Firefox. Например, свойство [кдромколлектион](player-cdromcollection.md) объекта **Player** возвращает **значение NULL** , так как подключаемый модуль Firefox не поддерживает объект **CDROM** . Аналогичным образом, свойства [DVD](player-dvd.md), [медиаколлектион](player-mediacollection.md), [плайераппликатион](player-playerapplication.md)и [плайлистколлектион](player-playlistcollection.md) объекта **Player** возвращают **значение NULL** в браузере Firefox.

Свойство **Player. плугинверсионинфо** поддерживается подключаемым модулем Firefox, но не Internet Explorer. Это свойство возвращает версию подключаемого модуля Firefox.

Подключаемый модуль Firefox поддерживает объект **мультимедиа** , включая свойство [жетитеминфобитипе](media-getiteminfobytype.md) . Однако в браузере Firefox свойство **жетитеминфобитипе** не поддерживает возвращаемые типы **метадататекст** и **метадатапиктуре** .

Подключаемый модуль Firefox поддерживает объект [Settings](settings-object.md) , за исключением метода [SetMode](settings-setmode.md) и свойства [рекуестмедиаакцессригхтс](settings-requestmediaaccessrights.md) . В браузере Firefox свойство **рекуестмедиаакцессригхт** всегда возвращает значение false.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




