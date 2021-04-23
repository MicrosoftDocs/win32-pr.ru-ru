---
description: Возвращает значение, передаваемое в качестве параметра Хиткинд в Репорсит.
ms.assetid: ''
title: хиткинд
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647145"
---
# <a name="hitkind"></a><span data-ttu-id="37913-103">хиткинд</span><span class="sxs-lookup"><span data-stu-id="37913-103">HitKind</span></span>

<span data-ttu-id="37913-104">Возвращает значение, передаваемое в качестве параметра **хиткинд** в [**репорсит**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="37913-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="37913-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37913-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="37913-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="37913-106">Remarks</span></span>

<span data-ttu-id="37913-107">Если пересечение было сообщено пересечением треугольника с фиксированной функцией, **хиткинд** будет одной из сторон, **\_ \_ \_ лицевой \_ стороной** треугольника (254) или координатами **типа курсора \_ \_ \_ \_** (255).</span><span class="sxs-lookup"><span data-stu-id="37913-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="37913-108">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="37913-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="37913-109">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="37913-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="37913-110">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="37913-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="37913-111">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="37913-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="37913-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37913-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37913-113">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="37913-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




