---
title: Цвет попадания в RGB
description: Цвет попадания в RGB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, цвета кнопок
- обложки, цвета кнопок
- Справочник по обложкам, кнопкам
- кнопки в обложках, цвета
- Справочник по цвету для обложек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691328"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="0cb3c-108">Цвет попадания в RGB</span><span class="sxs-lookup"><span data-stu-id="0cb3c-108">Hit RGB Color</span></span>

<span data-ttu-id="0cb3c-109">Если вы используете кнопки региона (Пушхит, Тогглехит и 2PushHit), необходимо определить цвет, который проигрыватель Windows Media будет использовать для определения области попадания кнопки.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="0cb3c-110">Это значение должно быть указано с использованием трех положительных целых чисел, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="0cb3c-111">Эти целые числа представляют красный, зеленый и синий цвет точечного рисунка, а также диапазон от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="0cb3c-112">Типы кнопок являются устаревшими в обложках проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="0cb3c-113">Можно использовать любые цвета для значений, но убедитесь, что каждая настроенная кнопка региона имеет уникальный цвет в файле изображения региона, а значение цвета, которое вы определяете здесь как число, соответствует фактическому цвету, используемому в изображении региона.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="0cb3c-114">В следующей таблице показаны некоторые типичные цвета, которые может потребоваться использовать.</span><span class="sxs-lookup"><span data-stu-id="0cb3c-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="0cb3c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0cb3c-115">Value</span></span>       | <span data-ttu-id="0cb3c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb3c-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="0cb3c-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="0cb3c-117">0,0,0</span></span>       | <span data-ttu-id="0cb3c-118">Черный</span><span class="sxs-lookup"><span data-stu-id="0cb3c-118">Black</span></span>       |
| <span data-ttu-id="0cb3c-119">255 255 255</span><span class="sxs-lookup"><span data-stu-id="0cb3c-119">255,255,255</span></span> | <span data-ttu-id="0cb3c-120">Белый</span><span class="sxs-lookup"><span data-stu-id="0cb3c-120">White</span></span>       |
| <span data-ttu-id="0cb3c-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="0cb3c-121">255,0,0</span></span>     | <span data-ttu-id="0cb3c-122">Красный</span><span class="sxs-lookup"><span data-stu-id="0cb3c-122">Red</span></span>         |
| <span data-ttu-id="0cb3c-123">0255, 0</span><span class="sxs-lookup"><span data-stu-id="0cb3c-123">0,255,0</span></span>     | <span data-ttu-id="0cb3c-124">Зеленый</span><span class="sxs-lookup"><span data-stu-id="0cb3c-124">Green</span></span>       |
| <span data-ttu-id="0cb3c-125">0, 0255</span><span class="sxs-lookup"><span data-stu-id="0cb3c-125">0,0,255</span></span>     | <span data-ttu-id="0cb3c-126">Синий</span><span class="sxs-lookup"><span data-stu-id="0cb3c-126">Blue</span></span>        |



 

<span data-ttu-id="0cb3c-127">Если кнопки области не используются, необходимо ввести следующее:</span><span class="sxs-lookup"><span data-stu-id="0cb3c-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="0cb3c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0cb3c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb3c-129">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="0cb3c-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




