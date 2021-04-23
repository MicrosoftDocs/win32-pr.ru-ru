---
title: Раздел точечных рисунков
description: Раздел точечных рисунков
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Обложки Windows Media Player для мобильных устройств, точечные рисунки
- обложки, точечные рисунки
- Создание обложек, раздел растровых изображений
- Написание кода для обложек, раздел точечных рисунков
- точечные рисунки в обложках, раздел точечных рисунков
- файлы определения обложки, раздел растровых изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067891"
---
# <a name="bitmaps-section"></a><span data-ttu-id="c20ee-109">Раздел точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="c20ee-109">Bitmaps Section</span></span>

<span data-ttu-id="c20ee-110">Далее необходимо иметь раздел, который определяет каждый из файлов растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="c20ee-110">Next, you must have a section that defines each of your bitmap files.</span></span> <span data-ttu-id="c20ee-111">Каждый тип точечного рисунка, который вы будете использовать, должен иметь назначенный ему файл, хотя можно использовать несколько типов, использующих один и тот же точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="c20ee-111">Each type of bitmap you will use must have a file assigned to it, though you can have more than one type using the same bitmap.</span></span>


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="c20ee-112">Раздел растровых изображений должен начинаться с точечных рисунков Word в квадратных скобках, а затем по строке для каждого типа точечного рисунка, который необходимо определить.</span><span class="sxs-lookup"><span data-stu-id="c20ee-112">The Bitmaps section must begin with the word Bitmaps in brackets and then a line for each bitmap type you want to define.</span></span> <span data-ttu-id="c20ee-113">В этом примере определено пять типов точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="c20ee-113">In this example, five types of bitmaps were defined.</span></span> <span data-ttu-id="c20ee-114">Дополнительные сведения см. в разделе [точечные](bitmaps.md) рисунки в справочнике по обложкам.</span><span class="sxs-lookup"><span data-stu-id="c20ee-114">For more about the Bitmaps section, see [Bitmaps](bitmaps.md) in the Skin Reference.</span></span>

> [!Note]  
> <span data-ttu-id="c20ee-115">В проигрывателе Windows Media 10 Mobile или более поздних обложек не рекомендуется использовать область и супер точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="c20ee-115">The Region and Super bitmaps are deprecated in Windows Media Player 10 Mobile or later skins.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c20ee-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c20ee-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c20ee-117">**Написание кода**</span><span class="sxs-lookup"><span data-stu-id="c20ee-117">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




