---
title: Расширенное расширение
description: Расширенное расширение
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Касание Windows, расширение
- Windows Touch, расширенное расширение
- Касание Windows, манипуляции
- манипуляции, расширение
- манипуляции, расширенное расширение
- расширение, дополнительно
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252839"
---
# <a name="advanced-expansion"></a><span data-ttu-id="07949-109">Расширенное расширение</span><span class="sxs-lookup"><span data-stu-id="07949-109">Advanced Expansion</span></span>

<span data-ttu-id="07949-110">На следующем рисунке показаны два способа расширения объекта.</span><span class="sxs-lookup"><span data-stu-id="07949-110">The following illustration shows two ways that an object can be expanded.</span></span>

![Иллюстрация, демонстрирующая простое увеличение вокруг центральной точки объекта и расширенное расширение вокруг центральной точки манипуляции](images/expansion.png)

<span data-ttu-id="07949-112">В примере а, простой пример расширения, объект разворачивается вокруг центральной точки.</span><span class="sxs-lookup"><span data-stu-id="07949-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="07949-113">В примере б объект разворачивается вокруг центральной точки манипуляции.</span><span class="sxs-lookup"><span data-stu-id="07949-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="07949-114">Чтобы сделать это, необходимо перевести объект во время его развертывания.</span><span class="sxs-lookup"><span data-stu-id="07949-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="07949-115">Величина, на которую будет преобразован объект, совпадает с расстоянием от центра объекта до центральной точки жеста.</span><span class="sxs-lookup"><span data-stu-id="07949-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="07949-116">Интуитивно понятно, что вы расширяете объект от центральной точки жеста расширения и затем перемещаете его, чтобы он по-прежнему находящийся в том же центре, что и его начальное расположение.</span><span class="sxs-lookup"><span data-stu-id="07949-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="07949-117">В следующем коде показан один из способов применения этой концепции для включения расширения вокруг центральной точки.</span><span class="sxs-lookup"><span data-stu-id="07949-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="07949-118">См. также</span><span class="sxs-lookup"><span data-stu-id="07949-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07949-119">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="07949-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




