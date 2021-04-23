---
title: Значения атрибутов для ТВ-содержимого
description: Значения атрибутов для ТВ-содержимого
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Проигрыватель Windows Media, атрибуты для элементов мультимедиа
- Объектная модель проигрывателя Windows Media, атрибуты элементов мультимедиа
- Объектная модель, атрибуты элементов мультимедиа
- Проигрыватель Windows Media Mobile, атрибуты для элементов мультимедиа
- Элемент управления ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Элемент управления ActiveX, атрибуты для элементов мультимедиа
- Библиотека проигрывателя Windows Media, атрибуты для элементов мультимедиа
- Библиотека, атрибуты для элементов мультимедиа
- атрибуты, ТВ-содержимое
- Значения атрибутов ТВ-содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068611"
---
# <a name="attribute-values-for-tv-content"></a><span data-ttu-id="0dc72-114">Значения атрибутов для ТВ-содержимого</span><span class="sxs-lookup"><span data-stu-id="0dc72-114">Attribute Values for TV Content</span></span>

<span data-ttu-id="0dc72-115">В этом разделе объект **Player** был определен следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0dc72-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="0dc72-116">Проигрыватель Windows Media 10 или более поздней версии может организовывать ТЕЛЕВИЗИОНное содержимое в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="0dc72-116">Windows Media Player 10 or later can organize TV content in the library.</span></span> <span data-ttu-id="0dc72-117">Проигрыватель Windows Media обрабатывает ТЕЛЕВИЗИОНное содержимое как подкатегорию видеосодержимого.</span><span class="sxs-lookup"><span data-stu-id="0dc72-117">Windows Media Player treats TV content as a subcategory of video content.</span></span> <span data-ttu-id="0dc72-118">Чтобы видеосодержимое отображалось на ТВ-узлах в библиотеке, задайте атрибуты **WM/медиакласспримарид** и **WM/медиакласссекондарид** со значениями, приведенными в следующей таблице, с помощью *носителя*. метод **сетитеминфо** :</span><span class="sxs-lookup"><span data-stu-id="0dc72-118">To make video content appear in the TV nodes in the library, set the **WM/MediaClassPrimaryID** and the **WM/MediaClassSecondaryID** attributes to the values in the following table by using the *media*.**setItemInfo** method:</span></span>



| <span data-ttu-id="0dc72-119">attribute</span><span class="sxs-lookup"><span data-stu-id="0dc72-119">Attribute</span></span>                    | <span data-ttu-id="0dc72-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0dc72-120">Value</span></span>                                |
|------------------------------|--------------------------------------|
| <span data-ttu-id="0dc72-121">**WM/Медиакласспримарид**</span><span class="sxs-lookup"><span data-stu-id="0dc72-121">**WM/MediaClassPrimaryID**</span></span>   | <span data-ttu-id="0dc72-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span><span class="sxs-lookup"><span data-stu-id="0dc72-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span></span> |
| <span data-ttu-id="0dc72-123">**WM/Медиакласссекондарид**</span><span class="sxs-lookup"><span data-stu-id="0dc72-123">**WM/MediaClassSecondaryID**</span></span> | <span data-ttu-id="0dc72-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span><span class="sxs-lookup"><span data-stu-id="0dc72-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span></span> |



 

<span data-ttu-id="0dc72-125">Эти значения также можно использовать для определения того, содержит ли конкретный элемент мультимедиа ТВ-содержимое с помощью *носителя*. **getItemInfo** или *Media*. методы **жетитеминфобитипе** .</span><span class="sxs-lookup"><span data-stu-id="0dc72-125">You can also use these values to determine whether a particular digital media item contains TV content by using the *media*.**getItemInfo** or *media*.**getItemInfoByType** methods.</span></span>

<span data-ttu-id="0dc72-126">Не забывайте использовать значения **GUID** в качестве **строковых** значений при указании или извлечении этих значений.</span><span class="sxs-lookup"><span data-stu-id="0dc72-126">Remember to use the **GUID** values as **string** values when specifying or retrieving these values.</span></span>

<span data-ttu-id="0dc72-127">В следующем примере кода C# атрибуты класса мультимедиа устанавливаются таким образом, чтобы элемент мультимедиа был идентифицирован как ТВ-содержимое.</span><span class="sxs-lookup"><span data-stu-id="0dc72-127">The following C# example code sets the media class attributes so that a media item will be identified as TV content.</span></span>


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



<span data-ttu-id="0dc72-128">Дополнительные сведения о возможных значениях атрибутов класса мультимедиа см. в разделе рекомендации по [использованию метаданных мультимедиа Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="0dc72-128">For more info about the possible values for the media class attributes, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dc72-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0dc72-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dc72-130">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="0dc72-130">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="0dc72-131">**Доступ к библиотеке**</span><span class="sxs-lookup"><span data-stu-id="0dc72-131">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="0dc72-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="0dc72-132">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




