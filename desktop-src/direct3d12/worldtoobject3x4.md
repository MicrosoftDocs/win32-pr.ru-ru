---
description: WorldToObject3x4 — матрица для преобразования из мирового пространства в объектно-пространство.
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
ms.openlocfilehash: cc7bf7dc2f06102b9b23eafd45655f12816c8359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105243"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="62441-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="62441-103">WorldToObject3x4</span></span>

<span data-ttu-id="62441-104">Матрица для преобразования из мирового пространства в объектно-пространство.</span><span class="sxs-lookup"><span data-stu-id="62441-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="62441-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="62441-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="62441-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62441-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="62441-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="62441-107">Remarks</span></span>

<span data-ttu-id="62441-108">Матрица является транспоситион матрицы **WorldToObject4x3** .</span><span class="sxs-lookup"><span data-stu-id="62441-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="62441-109">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="62441-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="62441-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="62441-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="62441-111">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="62441-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="62441-112">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="62441-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="62441-113">См. также</span><span class="sxs-lookup"><span data-stu-id="62441-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62441-114">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="62441-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




