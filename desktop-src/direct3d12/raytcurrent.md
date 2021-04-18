---
description: Значение типа float, представляющее текущую конечную точку параметрической для луча.
ms.assetid: ''
title: райткуррент
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701246"
---
# <a name="raytcurrent"></a><span data-ttu-id="a7c02-103">райткуррент</span><span class="sxs-lookup"><span data-stu-id="a7c02-103">RayTCurrent</span></span>

<span data-ttu-id="a7c02-104">Значение типа float, представляющее текущую конечную точку параметрической для луча.</span><span class="sxs-lookup"><span data-stu-id="a7c02-104">A float representing the current parametric ending point for the ray.</span></span>  

## <a name="syntax"></a><span data-ttu-id="a7c02-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7c02-105">Syntax</span></span>

```
float RayTCurrent();

```


## <a name="remarks"></a><span data-ttu-id="a7c02-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7c02-106">Remarks</span></span>

<span data-ttu-id="a7c02-107">**Райткуррент** определяет текущую конечную точку луча в соответствии со следующей формулой: Origin + (направление \* райткуррент).</span><span class="sxs-lookup"><span data-stu-id="a7c02-107">**RayTCurrent** defines the current ending point of the ray according to the following formula: Origin + (Direction \* RayTCurrent).</span></span>  <span data-ttu-id="a7c02-108">*Источник* и *направление* могут находиться в мировом или объектном пространстве, что приводит к заполнению точки мира или объектного пространства.</span><span class="sxs-lookup"><span data-stu-id="a7c02-108">*Origin* and *Direction* may be in either world or object space, which results in either a world or an object space ending point.</span></span>

<span data-ttu-id="a7c02-109">**Райткуррент** инициализируется в вызове [**трацерай**](traceray-function.md) с использованием значения [**райдеск:: тмакс**](raydesc.md) , а затем обновляется во время выполнения запроса трассировки в отчетах о пересечениях (при любом попадании) и принимается.</span><span class="sxs-lookup"><span data-stu-id="a7c02-109">**RayTCurrent** is initialized in the call [**TraceRay**](traceray-function.md) call with the [**RayDesc::TMax**](raydesc.md) value and then is updated during the trace query as intersections are reported (in the any hit), and accepted.</span></span>

<span data-ttu-id="a7c02-110">В [шейдере пересечения](intersection-shader.md)он представляет расстояние до ближайшего пересечения, обнаруженного до сих пор.</span><span class="sxs-lookup"><span data-stu-id="a7c02-110">In the [intersection shader](intersection-shader.md), it represents the distance to the closest intersection found so far.</span></span>  <span data-ttu-id="a7c02-111">Оно будет обновлено после () для значения сит, если оно было принято.</span><span class="sxs-lookup"><span data-stu-id="a7c02-111">It will be updated after () to the THit value provided if the hit was accepted.</span></span>

<span data-ttu-id="a7c02-112">В [любом шейдере попадания](any-hit-shader.md)он представляет расстояние до переданного перекрестного сообщения.</span><span class="sxs-lookup"><span data-stu-id="a7c02-112">In the [any hit shader](any-hit-shader.md), it represents the distance to the current intersection being reported.</span></span>

<span data-ttu-id="a7c02-113">В [ближайшем шейдере попадания](closest-hit-shader.md)он представляет расстояние до ближайшего принимаемого пересечения.</span><span class="sxs-lookup"><span data-stu-id="a7c02-113">In the [closest hit shader](closest-hit-shader.md), it represents the distance to the closest intersection accepted.</span></span>

<span data-ttu-id="a7c02-114">В [шейдере промахов](miss-shader.md)он равен *тмакс* , переданному в вызов **трацерай** .</span><span class="sxs-lookup"><span data-stu-id="a7c02-114">In the [miss shader](miss-shader.md), it is equal to *TMax* passed to the **TraceRay** call.</span></span>


<span data-ttu-id="a7c02-115">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="a7c02-115">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="a7c02-116">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="a7c02-116">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="a7c02-117">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="a7c02-117">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="a7c02-118">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="a7c02-118">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="a7c02-119">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="a7c02-119">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="a7c02-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7c02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c02-121">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a7c02-121">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




