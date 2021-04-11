---
title: Использование элементов PARAM на веб-странице, отображаемой Firefox
description: Использование элементов PARAM на веб-странице, отображаемой Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
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
- Проигрыватель Windows Media, Firefox
- Объектная модель проигрывателя Windows Media, Firefox
- Объектная модель, Firefox
- Проигрыватель Windows Media Mobile, Firefox
- Элемент управления ActiveX проигрывателя Windows Media, Firefox
- Элемент управления ActiveX проигрывателя Windows Media Mobile, Firefox
- Элемент управления ActiveX, Firefox
- Firefox, элементы PARAM в элементе OBJECT
- Внедрение веб-страниц, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332867"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="035f2-122">Использование элементов PARAM на веб-странице, отображаемой Firefox</span><span class="sxs-lookup"><span data-stu-id="035f2-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="035f2-123">Элементы PARAM можно использовать внутри элемента OBJECT для задания начального состояния элемента управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="035f2-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="035f2-124">Например, элементы PARAM в следующем примере указывают, что элемент управления должен автоматически воспроизводиться в Сиэтле. WMV.</span><span class="sxs-lookup"><span data-stu-id="035f2-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="035f2-125">Большинство элементов PARAM можно интерпретировать с помощью Internet Explorer и Firefox.</span><span class="sxs-lookup"><span data-stu-id="035f2-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="035f2-126">Однако существует несколько элементов PARAM, которые не поддерживаются подключаемым модулем Firefox.</span><span class="sxs-lookup"><span data-stu-id="035f2-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="035f2-127">Сведения о том, какие элементы PARAM поддерживаются подключаемым модулем Firefox, см. [в разделе элементы param в ЭЛЕМЕНТЕ Object](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="035f2-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="035f2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="035f2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="035f2-129">**Использование элемента управления проигрывателя Windows Media с браузером Firefox**</span><span class="sxs-lookup"><span data-stu-id="035f2-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




