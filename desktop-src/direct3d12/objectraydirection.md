---
description: Направление объектного пространства для текущего луча.
ms.assetid: ''
title: обжектрайдиректион
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayDirection
api_type:
- NA
ms.openlocfilehash: 1cc291a33f91bf7fc0565596bdd075a86e193246
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710717"
---
# <a name="objectraydirection"></a><span data-ttu-id="1cb85-103">обжектрайдиректион</span><span class="sxs-lookup"><span data-stu-id="1cb85-103">ObjectRayDirection</span></span>

<span data-ttu-id="1cb85-104">Направление объектного пространства для текущего луча.</span><span class="sxs-lookup"><span data-stu-id="1cb85-104">The object-space direction for the current ray.</span></span> <span data-ttu-id="1cb85-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1cb85-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb85-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cb85-106">Syntax</span></span>

```
float3 ObjectRayDirection();

```



## <a name="remarks"></a><span data-ttu-id="1cb85-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="1cb85-107">Remarks</span></span>

<span data-ttu-id="1cb85-108">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="1cb85-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="1cb85-109">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="1cb85-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="1cb85-110">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="1cb85-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="1cb85-111">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="1cb85-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="1cb85-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cb85-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb85-113">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1cb85-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




