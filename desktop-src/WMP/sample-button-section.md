---
title: Раздел "пример"
description: Раздел "пример"
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, раздел "Кнопка"
- обложки, раздел "Кнопка"
- Справочник по обложкам, разделу кнопки
- кнопки в обложках, раздел "Кнопка"
- файлы определения обложки, раздел кнопки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068217"
---
# <a name="sample-button-section"></a><span data-ttu-id="aca72-108">Раздел "пример"</span><span class="sxs-lookup"><span data-stu-id="aca72-108">Sample Button Section</span></span>

<span data-ttu-id="aca72-109">В следующих строках показана типичная область кнопок в файле определения обложки:</span><span class="sxs-lookup"><span data-stu-id="aca72-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="aca72-110">Этот код определяет восемь кнопок, которые используются для предоставления всех следующих функций в обложке:</span><span class="sxs-lookup"><span data-stu-id="aca72-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="aca72-111">Воспроизведение, приостановка и остановка элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aca72-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="aca72-112">В случайном порядке, повторении и перемещении по списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="aca72-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="aca72-113">Отключите громкость.</span><span class="sxs-lookup"><span data-stu-id="aca72-113">Mute the volume.</span></span>

<span data-ttu-id="aca72-114">Все кнопки, кроме кнопки «Выключить звук», являются кнопками области.</span><span class="sxs-lookup"><span data-stu-id="aca72-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="aca72-115">Кнопка «выключить звук» получает оттуда и отключает изображения из Super Bitmap для удобства.</span><span class="sxs-lookup"><span data-stu-id="aca72-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="aca72-116">Типы кнопок являются устаревшими в обложках проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="aca72-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="aca72-117">Вместо типа кнопки, объявленного в файле обложки, введите НД для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="aca72-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aca72-118">См. также</span><span class="sxs-lookup"><span data-stu-id="aca72-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aca72-119">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="aca72-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




