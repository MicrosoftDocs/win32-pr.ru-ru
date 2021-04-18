---
title: Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox
description: Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Проигрыватель Windows Media, внедрение элемента управления ActiveX
- Объектная модель проигрывателя Windows Media, внедрение элемента управления ActiveX
- Объектная модель, внедрение элемента управления ActiveX
- Проигрыватель Windows Media Mobile, внедрение элемента управления ActiveX
- Элемент управления ActiveX проигрывателя Windows Media, внедрение
- Мобильный элемент управления ActiveX проигрывателя Windows Media, внедрение
- Элемент управления ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, веб-страницы
- Элемент управления ActiveX проигрывателя Windows Media, свойство Инвокеурлс
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, свойство Инвокеурлс
- внедрение, веб-страницы
- Веб-страница внедрения, свойство Инвокеурлс
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, свойство Инвокеурлс
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "105700728"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Использование свойства Инвокеурлс на веб-странице, отображаемой в браузере Firefox

Некоторые файлы мультимедиа содержат внедренные URL-адреса, для которых проигрыватель Windows Media отображает веб-страницы в окне или фрейме браузера по мере воспроизведения файла мультимедиа. В Windows Internet Explorer можно использовать свойство [Settings. инвокеурлс](settings-invokeurls.md) , чтобы указать, отображаются ли страницы для внедренных URL-адресов, а также можно использовать свойство [Settings. дефаултфраме](settings-defaultframe.md) , чтобы указать кадр для отображения таких страниц.

В Firefox некоторые обходные пути необходимы для установки свойства **инвокеурлс** и для указания кадра для отображения страниц для внедренных URL-адресов.

## <a name="setting-the-invokeurls-property"></a>Установка свойства Инвокеурлс

По умолчанию свойство **Settings. инвокеурлс** имеет значение true, поэтому если требуется, чтобы значение было равно false, необходимо явно задать его. В Internet Explorer можно задать **инвокеурлс** в качестве значения false в элементе param внутри элемента объекта управления Player.

Подключаемый модуль Firefox не поддерживает задание свойства **инвокеурлс** в элементе param.

Это ограничение можно обойти, задав свойство **инвокеурлс** в скрипте. В следующем коде показано, как установить свойство **инвокеурлс** в значение false на веб-странице, которая может отображаться как в Internet Explorer, так и в браузере Firefox.


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a>Отображение веб-страниц в рамке

Файл мультимедиа может содержать URL-адреса, отображающие веб-страницы в окне или рамке браузера по мере воспроизведения файла мультимедиа. В Internet Explorer можно использовать свойство [Settings. дефаултфраме](settings-defaultframe.md) , чтобы указать кадр, в котором отображаются эти страницы. Если не задать свойство **дефаултфраме** , URL-адреса будут отображаться в отдельном окне браузера по умолчанию. Однако подключаемый модуль Firefox не поддерживает свойство **Settings. дефаултфраме** . Чтобы обойти это ограничение, присвойте свойству **Settings. инвокеурлс** значение false и напишите обработчик событий [команду скрипта](player-player-scriptcommand.md) , который задает расположение целевого кадра. Этот метод показан в следующем примере, который работает в Internet Explorer и Firefox. Предположим, что веб-страница, показанная в примере, находится в кадрах \[ 0 \] , и вы хотите, чтобы страница URL-адреса отображалась в кадрах \[ 1 \] .


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование элемента управления проигрывателя Windows Media с браузером Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




