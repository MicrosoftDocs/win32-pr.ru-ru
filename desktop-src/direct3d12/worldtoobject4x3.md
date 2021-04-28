---
description: WorldToObject4x3 — матрица для преобразования из мирового пространства в объектно-пространство.
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105251"
---
# <a name="worldtoobject4x3"></a><span data-ttu-id="98bde-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="98bde-103">WorldToObject4x3</span></span>

<span data-ttu-id="98bde-104">Матрица для преобразования из мирового пространства в объектно-пространство.</span><span class="sxs-lookup"><span data-stu-id="98bde-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="98bde-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="98bde-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bde-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98bde-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="98bde-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="98bde-107">Remarks</span></span>

<span data-ttu-id="98bde-108">Матрица является транспоситион матрицы **WorldToObject3x4** .</span><span class="sxs-lookup"><span data-stu-id="98bde-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="98bde-109">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="98bde-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="98bde-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="98bde-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="98bde-111">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="98bde-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="98bde-112">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="98bde-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="98bde-113">См. также</span><span class="sxs-lookup"><span data-stu-id="98bde-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bde-114">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="98bde-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




