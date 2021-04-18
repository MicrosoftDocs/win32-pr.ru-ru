---
title: Соответствующие цвета проигрывателя Windows Media
description: Соответствующие цвета проигрывателя Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player — Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Тип 1 Интернет-магазины, соответствующие цвета проигрывателя Windows Media
- Тип 2 Интернет-магазинов, соответствующие цвета проигрывателя Windows Media
- Интернет-магазины проигрывателя Windows Media, сопоставление цветов проигрывателя Windows Media
- Интернет-магазины, сопоставление цветов проигрывателем Windows Media
- Тип 1 Интернет-магазины, сопоставление цветов проигрывателя Windows Media
- Тип 2 Интернет-магазинов, сопоставление цветов проигрывателя Windows Media
- Интернет-магазины проигрывателя Windows Media, сопоставление цветов для проигрывателя Windows Media
- Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Тип 1 Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Тип 2. Интернет-магазины, сопоставление цветов для проигрывателя Windows Media
- Сопоставление цветов для проигрывателя Windows Media
- соответствующие цвета проигрывателя Windows Media
- Проигрыватель Windows Media, сопоставление цветов
- Проигрыватель Windows Media, сопоставление цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700665"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="be1f6-119">Соответствующие цвета проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="be1f6-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="be1f6-120">Создание веб-страницы Интернет-магазина с помощью цветовой схемы проигрывателя Windows Media — это просто.</span><span class="sxs-lookup"><span data-stu-id="be1f6-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="be1f6-121">Просто обработайте событие **External. онколорчанже** .</span><span class="sxs-lookup"><span data-stu-id="be1f6-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="be1f6-122">Чтобы указать функцию для работы с событием, используйте код, подобный приведенному ниже, при загрузке веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="be1f6-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="be1f6-123">Каждый раз, когда пользователь изменяет цветовую схему проигрывателя Windows Media, проигрыватель вызывает функцию.</span><span class="sxs-lookup"><span data-stu-id="be1f6-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="be1f6-124">В следующем примере показана простая функция, которая задает фон веб-страницы в соответствии со свойством **External. аппколорлигхт** :</span><span class="sxs-lookup"><span data-stu-id="be1f6-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="be1f6-125">Существуют и другие свойства цвета, доступные для использования.</span><span class="sxs-lookup"><span data-stu-id="be1f6-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="be1f6-126">См. [внешний объект для Интернет-магазинов типа 2](external-object-for-type-2-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="be1f6-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be1f6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="be1f6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be1f6-128">**External. Аппколорлигхт**</span><span class="sxs-lookup"><span data-stu-id="be1f6-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="be1f6-129">**Внешнее событие Онколорчанже**</span><span class="sxs-lookup"><span data-stu-id="be1f6-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="be1f6-130">**Сведения, общие для типа 1 и 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="be1f6-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




