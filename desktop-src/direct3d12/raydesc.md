---
description: Передается функции Трацерай для определения источника, направления и экстентов луча.
ms.assetid: ''
title: Структура Райдеск
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: a5fd6e041fc476c24ff926c9c8f99f05699f5e41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701248"
---
# <a name="raydesc-structure"></a><span data-ttu-id="85318-103">Структура Райдеск</span><span class="sxs-lookup"><span data-stu-id="85318-103">RayDesc structure</span></span>

<span data-ttu-id="85318-104">Передается функции [**трацерай**](traceray-function.md) для определения источника, направления и экстентов луча.</span><span class="sxs-lookup"><span data-stu-id="85318-104">Passed to the [**TraceRay**](traceray-function.md) function to define the origin, direction, and extents of the ray.</span></span>

## <a name="syntax"></a><span data-ttu-id="85318-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85318-105">Syntax</span></span>


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a><span data-ttu-id="85318-106">Поля</span><span class="sxs-lookup"><span data-stu-id="85318-106">Fields</span></span>

<dl> <dt>

<span data-ttu-id="85318-107"><span id="Origin"></span><span id="origin"></span>**Лета**</span><span class="sxs-lookup"><span data-stu-id="85318-107"><span id="Origin"></span><span id="origin"></span>**Origin**</span></span>
</dt> <dd>

<span data-ttu-id="85318-108">Источник луча.</span><span class="sxs-lookup"><span data-stu-id="85318-108">The origin of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="85318-109"><span id="TMin"></span><span id="tmin"></span>**тмин**</span><span class="sxs-lookup"><span data-stu-id="85318-109"><span id="TMin"></span><span id="tmin"></span>**TMin**</span></span>
</dt> <dd>

<span data-ttu-id="85318-110">Минимальная область луча.</span><span class="sxs-lookup"><span data-stu-id="85318-110">The minimum extent of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="85318-111"><span id="Direction"></span><span id="direction"></span>**Двух**</span><span class="sxs-lookup"><span data-stu-id="85318-111"><span id="Direction"></span><span id="direction"></span>**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="85318-112">Направление луча.</span><span class="sxs-lookup"><span data-stu-id="85318-112">The direction of the ray.</span></span>


</dd> <dt>

<span data-ttu-id="85318-113"><span id="TMax"></span><span id="tmax"></span>**тмакс**</span><span class="sxs-lookup"><span data-stu-id="85318-113"><span id="TMax"></span><span id="tmax"></span>**TMax**</span></span>
</dt> <dd>

<span data-ttu-id="85318-114">Максимальная область луча.</span><span class="sxs-lookup"><span data-stu-id="85318-114">The maximum extent of the ray.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="85318-115">Требования</span><span class="sxs-lookup"><span data-stu-id="85318-115">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="85318-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85318-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85318-117">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="85318-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




