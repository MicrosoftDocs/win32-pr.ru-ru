---
description: Шейдер, который вызывается, когда ни один из пересечения лучей не найден или не принят.
ms.assetid: ''
title: Шейдер непопаданий
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692036"
---
# <a name="miss-shader"></a><span data-ttu-id="3d477-103">Шейдер непопаданий</span><span class="sxs-lookup"><span data-stu-id="3d477-103">Miss Shader</span></span>

<span data-ttu-id="3d477-104">Шейдер, который вызывается, когда ни один из пересечения лучей не найден или не принят.</span><span class="sxs-lookup"><span data-stu-id="3d477-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="3d477-105">Это удобно для фона или штриховки.</span><span class="sxs-lookup"><span data-stu-id="3d477-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="3d477-106">Чтобы запланировать больше работы, шейдер может использовать [**каллшадер**](callshader-function.md) и **трацерай** .</span><span class="sxs-lookup"><span data-stu-id="3d477-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="3d477-107">В раскрывающемся шейдере должен быть указан параметр полезной нагрузки с определяемой пользователем структурой, соответствующий указанному в [**трацерай**](traceray-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d477-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="3d477-108">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="3d477-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="3d477-109">Пример</span><span class="sxs-lookup"><span data-stu-id="3d477-109">Example</span></span>

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




