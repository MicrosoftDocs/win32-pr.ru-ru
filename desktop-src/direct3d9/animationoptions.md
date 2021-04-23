---
description: Позволяет задать параметры анимации.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: аниматионоптионс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141971"
---
# <a name="animationoptions"></a><span data-ttu-id="8367b-103">аниматионоптионс</span><span class="sxs-lookup"><span data-stu-id="8367b-103">AnimationOptions</span></span>

<span data-ttu-id="8367b-104">Позволяет задать параметры анимации.</span><span class="sxs-lookup"><span data-stu-id="8367b-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="8367b-105">Где:</span><span class="sxs-lookup"><span data-stu-id="8367b-105">Where:</span></span>

-   <span data-ttu-id="8367b-106">опенклосед — используйте 0 для закрытой анимации или 1 для открытой анимации.</span><span class="sxs-lookup"><span data-stu-id="8367b-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="8367b-107">По умолчанию анимация закрыта.</span><span class="sxs-lookup"><span data-stu-id="8367b-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="8367b-108">поситионкуалити — задайте качество расположения для всех указанных ключей позиционирования.</span><span class="sxs-lookup"><span data-stu-id="8367b-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="8367b-109">Используйте 0 для позиционирования сплайна или 1 для линейных позиций.</span><span class="sxs-lookup"><span data-stu-id="8367b-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="8367b-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8367b-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8367b-111">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="8367b-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



