---
description: Матрица для преобразования из мирового пространства в объектно-пространство.
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673147"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="dfc46-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="dfc46-103">WorldToObject3x4</span></span>

<span data-ttu-id="dfc46-104">Матрица для преобразования из мирового пространства в объектно-пространство.</span><span class="sxs-lookup"><span data-stu-id="dfc46-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="dfc46-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="dfc46-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc46-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfc46-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="dfc46-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfc46-107">Remarks</span></span>

<span data-ttu-id="dfc46-108">Матрица является транспоситион матрицы **WorldToObject4x3** .</span><span class="sxs-lookup"><span data-stu-id="dfc46-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="dfc46-109">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="dfc46-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="dfc46-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="dfc46-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="dfc46-111">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="dfc46-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="dfc46-112">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="dfc46-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="dfc46-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfc46-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc46-114">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="dfc46-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




