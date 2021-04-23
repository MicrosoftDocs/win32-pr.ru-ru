---
title: Расширенный Поворот
description: В этом разделе объясняется, как повернуть объект в зависимости от того, где пользователь выполняет манипуляции с вращением.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Касание Windows, поворот
- Касание Windows, Расширенный Поворот
- Касание Windows, манипуляции
- манипуляции, вращение
- манипуляции, Расширенный Поворот
- вращение, дополнительно
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986193"
---
# <a name="advanced-rotation"></a><span data-ttu-id="01d88-109">Расширенный Поворот</span><span class="sxs-lookup"><span data-stu-id="01d88-109">Advanced Rotation</span></span>

<span data-ttu-id="01d88-110">В этом разделе объясняется, как повернуть объект в зависимости от того, где пользователь выполняет манипуляции с вращением.</span><span class="sxs-lookup"><span data-stu-id="01d88-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="01d88-111">На следующем рисунке показаны два разных способа вращения объекта.</span><span class="sxs-lookup"><span data-stu-id="01d88-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![Иллюстрация, демонстрирующая два типа поворота одного пальца: вокруг центра или вокруг края, с границей, включающей вращение и перевод](images/rotation.png)

<span data-ttu-id="01d88-113">В примере а объект обрабатывается вокруг центральной точки объекта.</span><span class="sxs-lookup"><span data-stu-id="01d88-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="01d88-114">В примере б объект поворачивается вокруг центральной точки манипуляции.</span><span class="sxs-lookup"><span data-stu-id="01d88-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="01d88-115">Для поддержки манипуляций с точкой, отличной от центральной точки объекта, необходимо выполнить составную манипуляцию, которая выполняет поворот и перевод.</span><span class="sxs-lookup"><span data-stu-id="01d88-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="01d88-116">В следующем коде показано, как выполняется и вычисляется эта манипуляция.</span><span class="sxs-lookup"><span data-stu-id="01d88-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="01d88-117">См. также</span><span class="sxs-lookup"><span data-stu-id="01d88-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d88-118">Расширенные манипуляции</span><span class="sxs-lookup"><span data-stu-id="01d88-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="01d88-119">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="01d88-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




