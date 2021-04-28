---
description: ObjectToWorld3x4 — матрица для преобразования из объектного пространства в мировое пространство.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107742"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="bee5a-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="bee5a-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="bee5a-104">Матрица для преобразования из объектного пространства в мировое пространство.</span><span class="sxs-lookup"><span data-stu-id="bee5a-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="bee5a-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="bee5a-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee5a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bee5a-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="bee5a-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="bee5a-107">Remarks</span></span>

<span data-ttu-id="bee5a-108">Матрица является транспоситион матрицы **ObjectToWorld4x3** .</span><span class="sxs-lookup"><span data-stu-id="bee5a-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="bee5a-109">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="bee5a-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="bee5a-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="bee5a-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="bee5a-111">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="bee5a-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="bee5a-112">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="bee5a-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="bee5a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bee5a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee5a-114">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bee5a-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




