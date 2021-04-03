---
title: Добавление визуализаций
description: Добавление визуализаций
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Создание обложек, визуализаций
- Обложки проигрывателя Windows Media, визуализации
- обложки, визуализации
- визуализации, обложки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776322"
---
# <a name="adding-visualizations"></a><span data-ttu-id="87a25-107">Добавление визуализаций</span><span class="sxs-lookup"><span data-stu-id="87a25-107">Adding Visualizations</span></span>

<span data-ttu-id="87a25-108">Окно визуализации можно добавить так же, как вы добавили видеоокно.</span><span class="sxs-lookup"><span data-stu-id="87a25-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="87a25-109">Можно использовать одну и ту же обложку, однако используется элемент **Effects** .</span><span class="sxs-lookup"><span data-stu-id="87a25-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="87a25-110">Сначала необходимо добавить элемент **Effects** и присвоить ему идентификатор и размер:</span><span class="sxs-lookup"><span data-stu-id="87a25-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="87a25-111">Затем можно назначить две кнопки в следующей строке кода визуализации:</span><span class="sxs-lookup"><span data-stu-id="87a25-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="87a25-112">Слои и точечные рисунки были такими же, как в примере с видео, за исключением того, что стрелка воспроизведения была скопирована и отражена по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="87a25-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="87a25-113">Наконец, был добавлен простой элемент **игрока** с атрибутом **URL** , чтобы выбрать композицию для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="87a25-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="87a25-114">Похожая Рабочая оболочка визуализации отображается в разделе примера пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="87a25-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87a25-115">См. также</span><span class="sxs-lookup"><span data-stu-id="87a25-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87a25-116">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="87a25-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




