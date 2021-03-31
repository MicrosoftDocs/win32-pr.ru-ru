---
title: Раздел кнопок
description: Раздел кнопок
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Обложки мобильных приложений проигрывателя Windows Media, раздел кнопок
- обложки, раздел кнопок
- Создание обложек, раздел кнопок
- Написание кода для обложек, раздел кнопок
- кнопки в обложках, раздел кнопок
- файлы определения обложки, раздел кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068194"
---
# <a name="buttons-section"></a><span data-ttu-id="1d6da-109">Раздел кнопок</span><span class="sxs-lookup"><span data-stu-id="1d6da-109">Buttons Section</span></span>

<span data-ttu-id="1d6da-110">Далее необходимо определить кнопки, которые будут использоваться:</span><span class="sxs-lookup"><span data-stu-id="1d6da-110">Next, you must define the buttons you will be using:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



<span data-ttu-id="1d6da-111">В этом разделе определены четыре кнопки.</span><span class="sxs-lookup"><span data-stu-id="1d6da-111">There are four buttons defined in this section.</span></span> <span data-ttu-id="1d6da-112">Просматриваемая страница может переносить эти строки, но при вводе кода необходимо не переносить строки. то есть каждая строка должна быть заполнена и заканчиваться знаком абзаца.</span><span class="sxs-lookup"><span data-stu-id="1d6da-112">The page you are viewing may wrap these lines, but when you type in the code, you must not wrap lines; that is, each line must be complete and end with a paragraph mark.</span></span>

> [!Note]  
> <span data-ttu-id="1d6da-113">Типы кнопок не рекомендуются в обложек проигрывателя Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1d6da-113">Buttons types are deprecated in Windows Media Player 10 Mobile or later skins.</span></span> <span data-ttu-id="1d6da-114">Вместо типа кнопки, объявленного в файле обложки, введите НД для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="1d6da-114">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

<span data-ttu-id="1d6da-115">Для каждой кнопки необходимо определить функцию, тип, расположение, источник изображения, отключенный источник и цвет (для кнопок с типом курсора).</span><span class="sxs-lookup"><span data-stu-id="1d6da-115">For each button you must define the function, type, location, pushed image source, disabled source, and color (for hit-type buttons).</span></span> <span data-ttu-id="1d6da-116">Кроме того, для кнопки Плайпаусе необходимо определить обычные и отправленные источники изображений для приостановленного состояния.</span><span class="sxs-lookup"><span data-stu-id="1d6da-116">In addition, for the PlayPause button, you must define the normal and pushed image sources for the paused state.</span></span>

<span data-ttu-id="1d6da-117">Дополнительные сведения о разделе Buttons файла определения обложки см. в статье [кнопки](buttons.md) в справочнике по обложкам.</span><span class="sxs-lookup"><span data-stu-id="1d6da-117">For more about the Buttons section of the skin definition file, see [Buttons](buttons.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d6da-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1d6da-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d6da-119">**Написание кода**</span><span class="sxs-lookup"><span data-stu-id="1d6da-119">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




