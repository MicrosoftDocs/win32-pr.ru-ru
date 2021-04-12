---
title: Субтитры
description: Субтитры
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Проигрыватель Windows Media, синхронизированный доступный медиа-обмен (SAMI)
- Объектная модель проигрывателя Windows Media, синхронизированный доступный обмен мультимедийными данными (SAMI)
- Объектная модель, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media Mobile, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, синхронизированный доступный мультимедийный обмен (SAMI)
- Элемент управления ActiveX, синхронизированный доступный медиа-обмен (SAMI)
- Проигрыватель Windows Media, перенос закрытых субтитров
- Объектная модель проигрывателя Windows Media, Смигратинг субтитры
- Объектная модель, миграция закрытых субтитров
- Проигрыватель Windows Media Mobile, перенос скрытых субтитров
- Элемент управления ActiveX проигрывателя Windows Media, перенос закрытых субтитров
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, перенос скрытых субтитров
- Элемент управления ActiveX, перенос закрытых субтитров
- Синхронизированный доступный медиа-обмен (SAMI), миграция закрытых субтитров
- SAMId (синхронизированный доступный медиа-обмен), миграция закрытых субтитров
- инструкции по миграции, синхронизированный доступный мультимедийный обмен (SAMI)
- рекомендации по миграции, субтитры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104133539"
---
# <a name="closed-captioning"></a><span data-ttu-id="dffed-121">Субтитры</span><span class="sxs-lookup"><span data-stu-id="dffed-121">Closed Captioning</span></span>

<span data-ttu-id="dffed-122">Элемент управления ActiveX проигрывателя Windows Media 6,4 содержит интегрированную панель отображения скрытых субтитров, которая, когда она сделана видимой, позволяет включать синхронизированные закрытые субтитры мультимедиа (SAMId Media Interchange) и отображает текст закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="dffed-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="dffed-123">Элемент управления Windows Media Player 7 или более поздней версии включает отображение субтитров SAMId с помощью HTML- **<DIV>** элемента.</span><span class="sxs-lookup"><span data-stu-id="dffed-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="dffed-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="dffed-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="dffed-125">Этот метод обеспечивает полную гибкость, поскольку веб-страницу можно разрабатывать таким образом, чтобы отображать скрытые субтитры в настроенном виде. Отображение скрытых субтитров больше не требуется в фиксированном расположении, расположенном рядом с пользовательским интерфейсом проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dffed-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="dffed-126">После создания области для вывода скрытых титров используйте *клоседкаптион*. Свойство **каптионингид** для указания расположения, в котором проигрыватель Windows Media визуализирует текст закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="dffed-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="dffed-127">Пакет средств разработки программного обеспечения (SDK) проигрывателя Windows Media содержит рабочий пример встроенного проигрывателя, который отображает текст закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="dffed-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="dffed-128">Чтобы получить примеры пакета SDK, скачайте и установите полный пакет SDK проигрывателя Windows Media с веб-сайта корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="dffed-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="dffed-129">Дополнительные сведения о закрытых субтитрах и SAMI см. на [веб-сайте Microsoft Accessibility](https://www.microsoft.com/enable/).</span><span class="sxs-lookup"><span data-stu-id="dffed-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dffed-130">См. также</span><span class="sxs-lookup"><span data-stu-id="dffed-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dffed-131">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="dffed-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="dffed-132">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="dffed-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="dffed-133">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="dffed-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




