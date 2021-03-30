---
title: DVD-диск
description: DVD-диск
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Проигрыватель Windows Media, перенос DVD-дисков
- Объектная модель проигрывателя Windows Media, DVD-диски
- Объектная модель, DVD
- Элемент управления ActiveX проигрывателя Windows Media, DVD-диски
- Элемент управления ActiveX, DVD-диски
- Элемент управления ActiveX проигрывателя Windows Media Mobile, DVD-диски
- Проигрыватель Windows Media Mobile, перенос DVD-дисков
- рекомендации по миграции, DVD-диски
- Миграция DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777162"
---
# <a name="dvd"></a><span data-ttu-id="d8c1a-112">DVD-диск</span><span class="sxs-lookup"><span data-stu-id="d8c1a-112">DVD</span></span>

<span data-ttu-id="d8c1a-113">Элемент управления ActiveX проигрывателя Windows Media 6,4 содержит объект **DVD** , предоставляющий разнообразные методы и свойства, а также одно событие для работы непосредственно с содержимым DVD.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="d8c1a-114">Например, чтобы определить количество доступных наименований DVD-дисков, используйте **Player6**. **титлесаваилабле** , свойство:</span><span class="sxs-lookup"><span data-stu-id="d8c1a-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="d8c1a-115">Объектная модель проигрывателя Windows Media 7 или более поздней версии реализует более интегрированный подход к DVD.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="d8c1a-116">Свойства, методы и события, связанные с DVD, реализуются только там, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="d8c1a-117">В противном случае существующие функции объектной модели работают с DVD-носителями, как вы можете ожидать.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="d8c1a-118">Например, чтобы определить количество заголовков DVD, доступных при использовании проигрывателя Windows Media 7 или более поздней версии, вы получаете объект **списка воспроизведения** из объекта **CDROM** :</span><span class="sxs-lookup"><span data-stu-id="d8c1a-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="d8c1a-119">В предыдущем примере извлекается объект **списка воспроизведения** с первой записью, ПРЕДСТАВЛЯЮЩЕЙ DVD-носитель на первом диске.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="d8c1a-120">Дополнительные записи представляют отдельные заголовки DVD.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="d8c1a-121">Таким образом, количество доступных заголовков можно вычислить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d8c1a-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="d8c1a-122">Ниже приведены основные различия, которые следует учитывать при миграции с версии 6,4.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="d8c1a-123">Воспроизведение DVD поддерживается только при использовании проигрывателя Windows Media для Windows XP или более поздней версии и операционной системы Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="d8c1a-124">Дисководы DVD-дисков перечисляются точно так же, как устройства чтения компакт-дисков с помощью объекта **кдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="d8c1a-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="d8c1a-125">Управление отдельными дисководами DVD-дисков осуществляется с помощью объекта **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="d8c1a-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="d8c1a-126">Объект **DVD** расширяет объектную модель с помощью методов и одного свойства, специально предназначенного для работы с DVD.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="d8c1a-127">Существует два новых события, **опенплайлистсвитч** и **домаинчанже**, специально предназначенные для работы с DVD-дисками.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="d8c1a-128">Содержимое диска DVD организовано с помощью объектов **списков воспроизведения** и **мультимедийных** объектов.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="d8c1a-129">Управление языками DVD осуществляется с помощью функциональных возможностей языка, доступных в объекте **Controls** (Windows Media Player 9 Series или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="d8c1a-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="d8c1a-130">Элементы управления транспорта и сведения о положении для DVD работают так же, как и для других типов цифровых носителей.</span><span class="sxs-lookup"><span data-stu-id="d8c1a-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c1a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d8c1a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c1a-132">**Руководством по миграции объектной модели**</span><span class="sxs-lookup"><span data-stu-id="d8c1a-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="d8c1a-133">**Использование элемента управления проигрывателя Windows Media с Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="d8c1a-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




