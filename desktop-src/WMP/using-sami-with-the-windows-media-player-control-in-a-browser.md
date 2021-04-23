---
title: Использование SAMIs с элементом управления проигрывателя Windows Media в браузере
description: Использование SAMIs с элементом управления проигрывателя Windows Media в браузере
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Синхронизированный доступный мультимедийный обмен (SAMI), файлы
- SAMI (синхронизированный доступный медиа-обмен), файлы
- Синхронизированный доступный мультимедийный обмен (SAMI), пример кода
- SAMId (синхронизированный доступный медиа-обмен), пример кода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986813"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="51732-114">Использование SAMIs с элементом управления проигрывателя Windows Media в браузере</span><span class="sxs-lookup"><span data-stu-id="51732-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="51732-115">Вместо создания файла SAMI для каждого стиля или языка шрифта можно объявить различные классы стилей в одном файле с помощью базовых сценариев и управляющей объектной модели проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="51732-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="51732-116">Можно создавать пользовательские элементы управления, позволяющие пользователю выбирать между различными стилями и параметрами языка.</span><span class="sxs-lookup"><span data-stu-id="51732-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="51732-117">Кроме того, вы можете полностью контролировать структуру интерфейса проигрывателя и настройку каждой функции.</span><span class="sxs-lookup"><span data-stu-id="51732-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="51732-118">Подробные сведения о внедрении элемента управления проигрывателя Windows Media на веб-страницу см. в разделе [простой пример создания сценариев на странице](simple-example-of-scripting-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="51732-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="51732-119">В следующем примере кода демонстрируется использование скрытых субтитров с элементом управления проигрывателя Windows Media, внедренным в веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="51732-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="51732-120">Он включает элементы управления, позволяющие пользователю выбрать стиль и язык шрифта.</span><span class="sxs-lookup"><span data-stu-id="51732-120">It includes controls to allow the user to select font style and language.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="51732-121">См. также</span><span class="sxs-lookup"><span data-stu-id="51732-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51732-122">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="51732-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




