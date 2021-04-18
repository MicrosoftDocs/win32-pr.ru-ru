---
description: Флаги, передаваемые функции Трацерай для переопределения прозрачности, отбора и поведения при начальном выходе.
ms.assetid: ''
title: Перечисление RAY_FLAG
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
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701249"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="74730-103">\_Перечисление флагов лучей</span><span class="sxs-lookup"><span data-stu-id="74730-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="74730-104">Флаги, передаваемые функции [**трацерай**](traceray-function.md) для переопределения прозрачности, отбора и поведения при начальном выходе.</span><span class="sxs-lookup"><span data-stu-id="74730-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="74730-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74730-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="74730-106">Константы</span><span class="sxs-lookup"><span data-stu-id="74730-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="74730-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**\_флаг луча \_ нет**</span><span class="sxs-lookup"><span data-stu-id="74730-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="74730-108">Параметры не выбраны.</span><span class="sxs-lookup"><span data-stu-id="74730-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="74730-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**\_флаг луча \_ Force \_ непрозрачный**</span><span class="sxs-lookup"><span data-stu-id="74730-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="74730-110">Все пересечения лучей-примитивов, обнаруженные в райтраце, считаются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="74730-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="74730-111">Таким образом, никакие шейдеры попадания не будут выполняться независимо от того, указывает ли геометрический элемент \_ D3D12 \_ райтраЦинг \_ \_ непрозрачный флаг геометрии, и вне зависимости от флагов экземпляра на экземпляре, который был достигнут.</span><span class="sxs-lookup"><span data-stu-id="74730-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="74730-112">Этот флаг взаимоисключающий с \_ флагом лучей \_ Force \_ \_ , непрозрачным, флагом Ray непрозрачность \_ \_ \_ и \_ \_ \_ непрозрачное извлечение флага лучей \_ .</span><span class="sxs-lookup"><span data-stu-id="74730-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="74730-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**\_флаг луча \_ Force \_ не \_ прозрачный**</span><span class="sxs-lookup"><span data-stu-id="74730-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="74730-114">Все пересечения лучей-примитивов, обнаруженные в райтраце, считаются не непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="74730-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="74730-115">Таким образом, любые шейдеры попадания, если они есть, будут выполняться независимо от того, указывает ли геометрический элемент D3D12 \_ райтраЦинг \_ Geometry \_ флаг \_ непрозрачности и вне зависимости от флагов экземпляра на экземпляре, который был достигнут.</span><span class="sxs-lookup"><span data-stu-id="74730-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="74730-116">Этот флаг является взаимоисключающим с \_ флагом луча \_ FORCE_ \Опакуе, флагом луча, непрозрачным \_ \_ \_ и \_ \_ \_ \_ непрозрачным флагом отбора лучей.</span><span class="sxs-lookup"><span data-stu-id="74730-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="74730-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**\_флаг луча \_ допускает \_ первое \_ Нажатие \_ и \_ Завершение \_ поиска**</span><span class="sxs-lookup"><span data-stu-id="74730-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="74730-118">Первое пересечение-примитив лучей, обнаруженное в райтраце, автоматически вызывает **акцепситандендсеарч** сразу после любого шейдера попадания, в том числе при отсутствии шейдера попаданий.</span><span class="sxs-lookup"><span data-stu-id="74730-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="74730-119">Единственным исключением является ситуация, когда предшествующий любой шейдер вызывает **игнорехит**, в этом случае, когда луч остается нетронутым, так что следующее попадание становится еще одним кандидатом.</span><span class="sxs-lookup"><span data-stu-id="74730-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="74730-120">Чтобы это исключение было применено, любой шейдер нажатий должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="74730-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="74730-121">Таким образом, если любой шейдер нажатий пропускается, так как попадание считается непрозрачным (например, из-за флага луч Force или непрозрачного флага \_ \_ \_ D3D12 райтраЦинг или непрозрачного \_ \_ \_ \_ D3D12 \_ \_ \_ флага экземпляра райтраЦинг \_ ), вызывается **акцепситандендсеарч** .</span><span class="sxs-lookup"><span data-stu-id="74730-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="74730-122">Если при первом попадании появится ближайшее построитель текстуры, он вызывается, если \_ также имеется флаг луча, \_ пропуская \_ ближайший \_ \_ построитель текстуры.</span><span class="sxs-lookup"><span data-stu-id="74730-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="74730-123">Найденное совпадение считается ближайшим, даже несмотря на то, что другие потенциальные попадания, которые могут быть ближе к луча, могут быть не посещены.</span><span class="sxs-lookup"><span data-stu-id="74730-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="74730-124">Обычно этот флаг используется для теней, где необходимо найти только одно нажатие.</span><span class="sxs-lookup"><span data-stu-id="74730-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="74730-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**\_флаг луча \_ пропуск \_ ближайшего \_ \_ шейдера попаданий**</span><span class="sxs-lookup"><span data-stu-id="74730-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="74730-126">Даже если зафиксировано хотя бы одно попадание, а группа попаданий для ближайшего попадания содержит ближайший построитель текстуры, пропускает выполнение этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="74730-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="74730-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**Флаг лучей, получающий \_ \_ \_ треугольники с обратным отметкой \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74730-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="74730-128">Включает отбор треугольников, отстоящих от конца.</span><span class="sxs-lookup"><span data-stu-id="74730-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="74730-129">См. раздел **D3D12 \_ райтраЦинг \_ instance \_ flags** для выбора треугольников, для которых выполняется переход на один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="74730-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="74730-130">В экземплярах, задающих \_ \_ флаг экземпляра D3D12 райтраЦинг Disable of \_ flags \_ \_ \_ , этот флаг не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="74730-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="74730-131">Для типов geometry, отличных от D3D12 \_ райтраЦинг \_ Geometry \_ Type \_ , этот флаг не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="74730-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="74730-132">Этот флаг является взаимоисключающим с исключающих \_ треугольников с использованием флагов лучей \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="74730-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="74730-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**Флаги лучей исключать \_ \_ \_ \_ \_ треугольники спереди**</span><span class="sxs-lookup"><span data-stu-id="74730-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="74730-134">Включает отбор покадровых треугольников.</span><span class="sxs-lookup"><span data-stu-id="74730-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="74730-135">См. раздел **D3D12 \_ райтраЦинг \_ instance \_ flags** для выбора треугольников, для которых выполняется переход на один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="74730-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="74730-136">В экземплярах, задающих \_ \_ флаг экземпляра D3D12 райтраЦинг Disable of \_ flags \_ \_ \_ , этот флаг не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="74730-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="74730-137">Для типов geometry, отличных от D3D12 \_ райтраЦинг \_ Geometry \_ Type \_ , этот флаг не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="74730-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="74730-138">Этот флаг является взаимоисключающим с флагами лучей, которые \_ отмечаются \_ \_ обратными \_ \_ треугольниками.</span><span class="sxs-lookup"><span data-stu-id="74730-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="74730-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**\_непрозрачное отбор флагов лучей \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74730-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="74730-140">Исключает все примитивы, которые считаются непрозрачными на основе их геометрических объектов и флагов экземпляров.</span><span class="sxs-lookup"><span data-stu-id="74730-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="74730-141">Этот флаг является взаимоисключающим с непрозрачным \_ флагом лучей, параметром \_ \_ Ray \_ \_ Force \_ \_ , а \_ также \_ \_ \_ флагом луча, не являющийся непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="74730-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="74730-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**\_ \_ непрозрачный отбор ФЛАГов лучей \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74730-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="74730-143">Исключает все примитивы, которые считаются непрозрачными на основе их геометрических объектов и флагов экземпляров.</span><span class="sxs-lookup"><span data-stu-id="74730-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="74730-144">Этот флаг является взаимоисключающим с непрозрачным флагом ЛУЧА, непрозрачным флагом Ray, а параметром " \_ \_ \_ \_ \_ исключить \_ \_ непрозрачный" и \_ флагом луч \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="74730-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="74730-145">Требования</span><span class="sxs-lookup"><span data-stu-id="74730-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="74730-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74730-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74730-147">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="74730-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




