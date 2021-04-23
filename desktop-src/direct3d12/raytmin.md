---
description: Значение типа float, представляющее текущую отправную точку параметрической для луча.
ms.assetid: ''
title: райтмин
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701245"
---
# <a name="raytmin"></a><span data-ttu-id="50b55-103">райтмин</span><span class="sxs-lookup"><span data-stu-id="50b55-103">RayTMin</span></span>

<span data-ttu-id="50b55-104">Значение типа float, представляющее текущую отправную точку параметрической для луча.</span><span class="sxs-lookup"><span data-stu-id="50b55-104">A float representing the current parametric starting point for the ray.</span></span> 

## <a name="syntax"></a><span data-ttu-id="50b55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50b55-105">Syntax</span></span>

```
float RayTMin();

```

## <a name="remarks"></a><span data-ttu-id="50b55-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="50b55-106">Remarks</span></span>

<span data-ttu-id="50b55-107">**Райтмин** определяет начальную точку луча в соответствии со следующей формулой: источник + (направление \* райтмин).</span><span class="sxs-lookup"><span data-stu-id="50b55-107">**RayTMin** defines the starting point of the ray according to the following formula: Origin + (Direction \* RayTMin).</span></span>  <span data-ttu-id="50b55-108">*Источник* и *направление* могут находиться в любом мире или объектном пространстве, что приводит к отправной точке мира или объектного пространства.</span><span class="sxs-lookup"><span data-stu-id="50b55-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space starting point.</span></span>

<span data-ttu-id="50b55-109">**Райтмин** указывается в вызове [**трацерай**](traceray-function.md)и является константой в течение этого вызова.</span><span class="sxs-lookup"><span data-stu-id="50b55-109">**RayTMin** is specified in the call to [**TraceRay**](traceray-function.md), and is constant for the duration of that call.</span></span>




<span data-ttu-id="50b55-110">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="50b55-110">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="50b55-111">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="50b55-111">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="50b55-112">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="50b55-112">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="50b55-113">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="50b55-113">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="50b55-114">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="50b55-114">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="50b55-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50b55-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b55-116">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="50b55-116">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




