---
title: Пример раздела точечного рисунка
description: Пример раздела точечного рисунка
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Обложки Windows Media Player для мобильных устройств, точечные рисунки
- обложки, точечные рисунки
- Справочник по обложкам, точечным рисункам
- точечные рисунки в обложках, раздел точечных рисунков
- файлы определения обложки, раздел растровых изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888804"
---
# <a name="sample-bitmap-section"></a><span data-ttu-id="4bd8d-108">Пример раздела точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="4bd8d-108">Sample Bitmap Section</span></span>

<span data-ttu-id="4bd8d-109">В следующих строках показан типичный раздел точечных рисунков в файле определения обложки:</span><span class="sxs-lookup"><span data-stu-id="4bd8d-109">The following lines show a typical Bitmaps section of a skin definition file:</span></span>


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



<span data-ttu-id="4bd8d-110">Он определяет пять растровых изображений, которые используются для создания фонового изображения, изображения для отключенных и отправленных кнопок, изображение региона для кнопок области и супер-изображение для значений TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4bd8d-110">This defines five bitmaps that are used to create a Background image, images for Disabled and Pushed buttons, a Region image for region buttons, and a Super image for trackbars.</span></span>

> [!Note]  
> <span data-ttu-id="4bd8d-111">В обложках для проигрывателя Windows Media 10 Mobile или более поздней версии не рекомендуется использовать региональные и Super Bitmap.</span><span class="sxs-lookup"><span data-stu-id="4bd8d-111">The Region and Super bitmaps are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4bd8d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4bd8d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd8d-113">**Растровые изображения**</span><span class="sxs-lookup"><span data-stu-id="4bd8d-113">**Bitmaps**</span></span>](bitmaps.md)
</dt> </dl>

 

 




