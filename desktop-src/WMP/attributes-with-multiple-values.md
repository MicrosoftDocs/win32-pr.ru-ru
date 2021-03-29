---
title: Атрибуты с несколькими значениями (пакет SDK для проигрывателя Windows Media)
description: Атрибуты с несколькими значениями
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
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
- атрибуты, несколько значений
- несколько значений атрибута
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414593"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="7843e-114">Атрибуты с несколькими значениями (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="7843e-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="7843e-115">Некоторые атрибуты элемента мультимедиа могут иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="7843e-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="7843e-116">Например, атрибуты **Author**, **WM, composer** и **WM/жанр** могут иметь более одного значения.</span><span class="sxs-lookup"><span data-stu-id="7843e-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="7843e-117">Тип данных таких атрибутов является **строкой с несколькими значениями**.</span><span class="sxs-lookup"><span data-stu-id="7843e-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="7843e-118">В проигрывателе Windows Media Библиотека отображает несколько значений в одном поле, разделяя их точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="7843e-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="7843e-119">Однако каждое значение на самом деле является отдельным атрибутом в элементе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7843e-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="7843e-120">Можно написать код, который определит, имеет ли данный атрибут несколько значений, а затем извлечет все эти значения.</span><span class="sxs-lookup"><span data-stu-id="7843e-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="7843e-121">Необходимо использовать *носитель*. **жетитеминфобитипе**.</span><span class="sxs-lookup"><span data-stu-id="7843e-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="7843e-122">При использовании *носителя*. метод **getItemInfo** для получения атрибута с несколькими значениями вы получите только первое значение.</span><span class="sxs-lookup"><span data-stu-id="7843e-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="7843e-123">В последнем примере в разделе [чтение значений атрибутов](reading-attribute-values.md) показано использование *мультимедиа*. **жетаттрибутекаунтбитипе** и *Media*. методы **жетитеминфобитипе** для получения нескольких значений для заданного атрибута.</span><span class="sxs-lookup"><span data-stu-id="7843e-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7843e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7843e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7843e-125">**Атрибуты элемента мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="7843e-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="7843e-126">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="7843e-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7843e-127">**Считывание значений атрибутов с компакт-диска или DVD-диска**</span><span class="sxs-lookup"><span data-stu-id="7843e-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




