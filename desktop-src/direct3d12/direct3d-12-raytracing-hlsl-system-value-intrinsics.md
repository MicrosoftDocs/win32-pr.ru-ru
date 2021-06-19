---
title: Встроенные функции системных значений HLSL для трассировки лучей в Direct3D 12
description: Просмотрите ссылки на статьи, описывающие встроенные функции системных значений HLSL, поддерживающие конвейер Direct3D 12 райтраЦинг.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396439"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a><span data-ttu-id="2f8a1-103">Встроенные функции системных значений HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2f8a1-103">Direct3D 12 raytracing HLSL system value intrinsics</span></span>

<span data-ttu-id="2f8a1-104">Системные значения извлекаются с помощью специальных встроенных функций, а не включают параметры с особой семантикой в сигнатуре функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-104">System values are retrieved by using special intrinsic functions, rather than including parameters with special semantics in your shader function signature.</span></span> 

## <a name="in-this-section"></a><span data-ttu-id="2f8a1-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2f8a1-105">In this section</span></span>

### <a name="ray-dispatch-system-values"></a><span data-ttu-id="2f8a1-106">Значения системы диспетчеризации луча</span><span class="sxs-lookup"><span data-stu-id="2f8a1-106">Ray dispatch system values</span></span>

| <span data-ttu-id="2f8a1-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="2f8a1-107">Topic</span></span> | <span data-ttu-id="2f8a1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2f8a1-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="2f8a1-109">**диспатчрайсиндекс**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-109">**DispatchRaysIndex**</span></span>](dispatchraysindex.md) | <span data-ttu-id="2f8a1-110">Возвращает текущее расположение x и y в пределах ширины и высоты, полученных с помощью встроенного системного значения **диспатчрайсдименсионс** .</span><span class="sxs-lookup"><span data-stu-id="2f8a1-110">Gets the current x and y location within the width and height obtained with the **DispatchRaysDimensions** system value intrinsic.</span></span> |
| [<span data-ttu-id="2f8a1-111">**DispatchRaysDimensions**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-111">**DispatchRaysDimensions**</span></span>](dispatchraysdimensions.md) | <span data-ttu-id="2f8a1-112">Значения ширины, высоты и глубины из структуры **\_ \_ \_ DESC D3D12 диспетчеризации** , указанной в исходном вызове **диспатчрайс** .</span><span class="sxs-lookup"><span data-stu-id="2f8a1-112">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating **DispatchRays** call.</span></span> |

### <a name="ray-system-values"></a><span data-ttu-id="2f8a1-113">Значения системы лучей</span><span class="sxs-lookup"><span data-stu-id="2f8a1-113">Ray system values</span></span>

| <span data-ttu-id="2f8a1-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="2f8a1-114">Topic</span></span> | <span data-ttu-id="2f8a1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="2f8a1-115">Description</span></span> |
|-|-|
| [<span data-ttu-id="2f8a1-116">**ворлдрайоригин**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-116">**WorldRayOrigin**</span></span>](worldrayorigin.md) | <span data-ttu-id="2f8a1-117">Источник универсального пространства текущего луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-117">The world-space origin of the current ray.</span></span> |
| [<span data-ttu-id="2f8a1-118">**ворлдрайдиректион**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-118">**WorldRayDirection**</span></span>](worldraydirection.md) | <span data-ttu-id="2f8a1-119">Направление международного пространства для текущего луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-119">The world-space direction for the current ray.</span></span> |
| [<span data-ttu-id="2f8a1-120">**райтмин**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-120">**RayTMin**</span></span>](raytmin.md) | <span data-ttu-id="2f8a1-121">Значение типа float, представляющее текущую отправную точку параметрической для луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-121">A float representing the current parametric starting point for the ray.</span></span> |
| [<span data-ttu-id="2f8a1-122">**райткуррент**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-122">**RayTCurrent**</span></span>](raytcurrent.md) | <span data-ttu-id="2f8a1-123">Значение типа float, представляющее текущую конечную точку параметрической для луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-123">A float representing the current parametric ending point for the ray.</span></span>  |
| [<span data-ttu-id="2f8a1-124">**райфлагс**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-124">**RayFlags**</span></span>](rayflags.md) | <span data-ttu-id="2f8a1-125">Целое число без знака, содержащее текущие флаги **ray_flag** .</span><span class="sxs-lookup"><span data-stu-id="2f8a1-125">An unsigned integer containing the current **ray_flag** flags.</span></span> |

### <a name="primitiveobject-space-system-values"></a><span data-ttu-id="2f8a1-126">Системные значения примитива или объектного пространства</span><span class="sxs-lookup"><span data-stu-id="2f8a1-126">Primitive/object space system values</span></span>

| <span data-ttu-id="2f8a1-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="2f8a1-127">Topic</span></span> | <span data-ttu-id="2f8a1-128">Описание</span><span class="sxs-lookup"><span data-stu-id="2f8a1-128">Description</span></span> |
|-|-|
| [<span data-ttu-id="2f8a1-129">**инстанцеиндекс**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-129">**InstanceIndex**</span></span>](instanceindex.md) | <span data-ttu-id="2f8a1-130">Автоматически сформированный индекс текущего экземпляра в структуре ускорения райтраЦинг верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-130">The autogenerated index of the current instance in the top-level raytracing acceleration structure.</span></span> |
| [<span data-ttu-id="2f8a1-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-131">**InstanceID**</span></span>](instanceid.md) | <span data-ttu-id="2f8a1-132">Предоставленный пользователем идентификатор для экземпляра на экземпляре структуры ускорения нижнего уровня в структуре верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-132">The user-provided identifier for the instance on the bottom-level acceleration structure instance within the top-level structure.</span></span> |
| [<span data-ttu-id="2f8a1-133">**примитивеиндекс**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-133">**PrimitiveIndex**</span></span>](primitiveindex.md) | <span data-ttu-id="2f8a1-134">Автоматически сформированный индекс примитива внутри геометрии внутри экземпляра структуры ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-134">The autogenerated index of the primitive within the geometry inside the bottom-level acceleration structure instance.</span></span> |
| [<span data-ttu-id="2f8a1-135">**обжектрайоригин**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-135">**ObjectRayOrigin**</span></span>](objectrayorigin.md) | <span data-ttu-id="2f8a1-136">Источник пространства объекта для текущего луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-136">The object-space origin for the current ray.</span></span> |
| [<span data-ttu-id="2f8a1-137">**обжектрайдиректион**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-137">**ObjectRayDirection**</span></span>](objectraydirection.md) | <span data-ttu-id="2f8a1-138">Направление объектного пространства для текущего луча.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-138">The object-space direction for the current ray.</span></span> |
| [<span data-ttu-id="2f8a1-139">**ObjectToWorld3x4**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-139">**ObjectToWorld3x4**</span></span>](objecttoworld3x4.md) | <span data-ttu-id="2f8a1-140">Матрица для преобразования из объектного пространства в мировое пространство.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-140">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="2f8a1-141">**ObjectToWorld4x3**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-141">**ObjectToWorld4x3**</span></span>](objecttoworld4x3.md) | <span data-ttu-id="2f8a1-142">Матрица для преобразования из объектного пространства в мировое пространство.</span><span class="sxs-lookup"><span data-stu-id="2f8a1-142">A matrix for transforming from object-space to world-space.</span></span> |
| [<span data-ttu-id="2f8a1-143">**WorldToObject3x4**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-143">**WorldToObject3x4**</span></span>](worldtoobject3x4.md) | <span data-ttu-id="2f8a1-144">Матрица для преобразования из мирового пространства в объектно-пространство</span><span class="sxs-lookup"><span data-stu-id="2f8a1-144">A matrix for transforming from world-space to object-space</span></span> |
| [<span data-ttu-id="2f8a1-145">**WorldToObject4x3**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-145">**WorldToObject4x3**</span></span>](worldtoobject4x3.md) | <span data-ttu-id="2f8a1-146">Матрица для преобразования из мирового пространства в объектно-пространство</span><span class="sxs-lookup"><span data-stu-id="2f8a1-146">A matrix for transforming from world-space to object-space</span></span> |
### <a name="hit-specific-system-values"></a><span data-ttu-id="2f8a1-147">Системные значения для конкретного попадания</span><span class="sxs-lookup"><span data-stu-id="2f8a1-147">Hit-specific system values</span></span>

| <span data-ttu-id="2f8a1-148">Раздел</span><span class="sxs-lookup"><span data-stu-id="2f8a1-148">Topic</span></span> | <span data-ttu-id="2f8a1-149">Описание</span><span class="sxs-lookup"><span data-stu-id="2f8a1-149">Description</span></span> |
|-|-|
| [<span data-ttu-id="2f8a1-150">**хиткинд**</span><span class="sxs-lookup"><span data-stu-id="2f8a1-150">**HitKind**</span></span>](hitkind.md) | <span data-ttu-id="2f8a1-151">Возвращает значение, передаваемое в качестве параметра **хиткинд** в [**репорсит**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="2f8a1-151">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="2f8a1-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2f8a1-152">Related topics</span></span>

* [<span data-ttu-id="2f8a1-153">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="2f8a1-153">Core Reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="2f8a1-154">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2f8a1-154">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
