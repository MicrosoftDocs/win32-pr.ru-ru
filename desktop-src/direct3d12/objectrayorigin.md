---
description: Источник пространства объекта для текущего луча.
ms.assetid: ''
title: обжектрайоригин
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayOrigin
api_type:
- NA
ms.openlocfilehash: b64d3f2e6648d47659f180bf2aa3c1e912882677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710771"
---
# <a name="objectrayorigin"></a><span data-ttu-id="716f4-103">обжектрайоригин</span><span class="sxs-lookup"><span data-stu-id="716f4-103">ObjectRayOrigin</span></span>

<span data-ttu-id="716f4-104">Источник пространства объекта для текущего луча.</span><span class="sxs-lookup"><span data-stu-id="716f4-104">The object-space origin for the current ray.</span></span> <span data-ttu-id="716f4-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="716f4-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="716f4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="716f4-106">Syntax</span></span>

```
float3 ObjectRayOrigin();

```

## <a name="remarks"></a><span data-ttu-id="716f4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="716f4-107">Remarks</span></span>

<span data-ttu-id="716f4-108">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="716f4-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="716f4-109">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="716f4-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="716f4-110">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="716f4-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="716f4-111">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="716f4-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="716f4-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="716f4-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716f4-113">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="716f4-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




