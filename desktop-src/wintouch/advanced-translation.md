---
title: Расширенный перевод
description: Расширенный перевод
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch, перевод
- Windows Touch, расширенный перевод
- Касание Windows, манипуляции
- манипуляции, перевод
- манипуляции, расширенный перевод
- преобразование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887739"
---
# <a name="advanced-translation"></a><span data-ttu-id="afc77-109">Расширенный перевод</span><span class="sxs-lookup"><span data-stu-id="afc77-109">Advanced Translation</span></span>

<span data-ttu-id="afc77-110">На следующем рисунке показаны две интерпретации преобразования.</span><span class="sxs-lookup"><span data-stu-id="afc77-110">The following illustration shows two interpretations of translation.</span></span>

![Иллюстрация, на которой сначала показан простой перевод, в котором объект перемещается без вращения, а затем отображается расширенный перевод, включающий перемещение с поворотом.](images/translation.png)

<span data-ttu-id="afc77-112">В примере с простым примером перевода объект перемещается без вращения.</span><span class="sxs-lookup"><span data-stu-id="afc77-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="afc77-113">В примере б объект поворачивается во время перевода, в зависимости от того, где находится точка контакта объекта.</span><span class="sxs-lookup"><span data-stu-id="afc77-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="afc77-114">При включении ротации с одним пальцем, как описано в разделе [однонаправленный поворот](single-finger-rotation.md), можно включить сложный перевод.</span><span class="sxs-lookup"><span data-stu-id="afc77-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="afc77-115">На следующей диаграмме показаны различные компоненты ротации с одним пальцем при выполнении перевода.</span><span class="sxs-lookup"><span data-stu-id="afc77-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![Иллюстрация, в которой показаны компоненты ротации с одним пальцем: пивотпоинткс, пивотпоинти и пивотрадиус](images/translation-complex-components.png)

<span data-ttu-id="afc77-117">При перемещении объекта происходит повторное вычисление радиуса и перемещение точки вращения.</span><span class="sxs-lookup"><span data-stu-id="afc77-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="afc77-118">В следующем коде показан один из способов, которые можно выполнить в реализации [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) , которая обеспечивает сложный перевод.</span><span class="sxs-lookup"><span data-stu-id="afc77-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="afc77-119">Преобразования объектов происходят до вычисления точек вращения и RADIUS.</span><span class="sxs-lookup"><span data-stu-id="afc77-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="afc77-120">Таким образом объект будет перемещаться правильно, если пользователь выполняет расширение объекта во время его перемещения.</span><span class="sxs-lookup"><span data-stu-id="afc77-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="afc77-121">См. также</span><span class="sxs-lookup"><span data-stu-id="afc77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc77-122">Манипуляции</span><span class="sxs-lookup"><span data-stu-id="afc77-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




