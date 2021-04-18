---
description: Матрица для преобразования из объектного пространства в мировое пространство.
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
ms.openlocfilehash: 04f80dde64984010c6e015f6e885565396d3b9c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710716"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="66226-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="66226-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="66226-104">Матрица для преобразования из объектного пространства в мировое пространство.</span><span class="sxs-lookup"><span data-stu-id="66226-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="66226-105">Объектное пространство — это пространство текущей структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="66226-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="66226-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66226-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="66226-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="66226-107">Remarks</span></span>

<span data-ttu-id="66226-108">Матрица является транспоситион матрицы **ObjectToWorld4x3** .</span><span class="sxs-lookup"><span data-stu-id="66226-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="66226-109">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="66226-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="66226-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="66226-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="66226-111">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="66226-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="66226-112">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="66226-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="66226-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66226-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66226-114">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="66226-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




