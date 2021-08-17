---
title: использование SAMI с элементом управления проигрыватель Windows Media в браузере
description: использование SAMI с элементом управления проигрыватель Windows Media в браузере
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- объектная модель проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- проигрыватель Windows Media Мобильный, синхронизированный доступный мультимедийный обмен (SAMI)
- проигрыватель Windows Media ActiveX элемент управления, синхронизированный доступный медиа-обмен (SAMI)
- проигрыватель Windows Media мобильный ActiveX элемент управления, синхронизированный доступный мультимедийный обмен (SAMI)
- ActiveX элемент управления, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), файлы
- SAMI (синхронизированный доступный медиа-обмен), файлы
- Синхронизированный доступный мультимедийный обмен (SAMI), пример кода
- SAMId (синхронизированный доступный медиа-обмен), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d277f2849e6036d85bc8c03940a7dbd59df8b81083ca88240ebd68be768fde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134347"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>использование SAMI с элементом управления проигрыватель Windows Media в браузере

вместо создания файла SAMI для каждого стиля или языка шрифта можно объявить различные классы стилей в одном файле с помощью базовых сценариев и объектной модели элемента управления проигрыватель Windows Media. Можно создавать пользовательские элементы управления, позволяющие пользователю выбирать между различными стилями и параметрами языка. Кроме того, вы можете полностью контролировать структуру интерфейса проигрывателя и настройку каждой функции.

подробные сведения о внедрении элемента управления проигрыватель Windows Media на веб-странице см. в разделе [простой пример создания сценариев на странице](simple-example-of-scripting-in-a-web-page.md).

в следующем примере кода показано, как использовать закрытые заголовки с элементом управления проигрыватель Windows Media, внедренным в веб-страницу. Он включает элементы управления, позволяющие пользователю выбрать стиль и язык шрифта.


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




