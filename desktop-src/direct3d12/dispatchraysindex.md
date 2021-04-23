---
description: Возвращает текущее расположение в пределах ширины, высоты и глубины, полученное с помощью встроенного системного значения [**диспатчрайсдименсионс**](dispatchraysdimensions.md) .
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "105691706"
---
# <a name="dispatchraysindex"></a><span data-ttu-id="fc440-103">DispatchRaysIndex </span><span class="sxs-lookup"><span data-stu-id="fc440-103">DispatchRaysIndex</span></span>

<span data-ttu-id="fc440-104">Возвращает текущее расположение в пределах ширины, высоты и глубины, полученное с помощью встроенного системного значения [**диспатчрайсдименсионс**](dispatchraysdimensions.md) .</span><span class="sxs-lookup"><span data-stu-id="fc440-104">Gets the current location within the width, height, and depth obtained with the [**DispatchRaysDimensions**](dispatchraysdimensions.md) system value intrinsic.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc440-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc440-105">Syntax</span></span>

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a><span data-ttu-id="fc440-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="fc440-106">Remarks</span></span>

<span data-ttu-id="fc440-107">Эту функцию можно вызвать из следующих типов шейдеров райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="fc440-107">This function can be called from the following raytracing shader types.</span></span>

* [<span data-ttu-id="fc440-108">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="fc440-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="fc440-109">**Вызываемый шейдер**</span><span class="sxs-lookup"><span data-stu-id="fc440-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="fc440-110">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="fc440-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="fc440-111">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="fc440-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="fc440-112">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="fc440-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="fc440-113">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="fc440-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="fc440-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc440-114">See also</span></span>

* [<span data-ttu-id="fc440-115">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="fc440-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
