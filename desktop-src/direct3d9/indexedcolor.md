---
description: Состоит из параметра индекса и цвета RGBA и используется для определения цветов вершин сетки. Индекс определяет вершину, к которой применяется цвет.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: индекседколор
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341705"
---
# <a name="indexedcolor"></a><span data-ttu-id="37604-104">индекседколор</span><span class="sxs-lookup"><span data-stu-id="37604-104">IndexedColor</span></span>

<span data-ttu-id="37604-105">Состоит из параметра индекса и цвета RGBA и используется для определения цветов вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="37604-105">Consists of an index parameter and an RGBA color and is used for defining mesh vertex colors.</span></span> <span data-ttu-id="37604-106">Индекс определяет вершину, к которой применяется цвет.</span><span class="sxs-lookup"><span data-stu-id="37604-106">The index defines the vertex to which the color is applied.</span></span>

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

<span data-ttu-id="37604-107">Где:</span><span class="sxs-lookup"><span data-stu-id="37604-107">Where:</span></span>

-   <span data-ttu-id="37604-108">index — DWORD.</span><span class="sxs-lookup"><span data-stu-id="37604-108">index - A DWORD.</span></span> <span data-ttu-id="37604-109">См. описание выше.</span><span class="sxs-lookup"><span data-stu-id="37604-109">See the description above.</span></span>
-   <span data-ttu-id="37604-110">Индексколор — шаблон Колорргба.</span><span class="sxs-lookup"><span data-stu-id="37604-110">indexColor - A ColorRGBA template.</span></span> <span data-ttu-id="37604-111">См. [**колорргба**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="37604-111">See [**ColorRGBA**](colorrgba.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="37604-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37604-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37604-113">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="37604-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



