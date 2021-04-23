---
description: Отправляет луч в поиск на предмет попаданий в структуре ускорения.
ms.assetid: ''
title: Функция TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: faeed928b25acb4dac95e47a46a103daf87124e0
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "105703479"
---
# <a name="traceray-function"></a><span data-ttu-id="0e06b-103">Функция TraceRay</span><span class="sxs-lookup"><span data-stu-id="0e06b-103">TraceRay function</span></span>

<span data-ttu-id="0e06b-104">Отправляет луч в поиск на предмет попаданий в структуре ускорения.</span><span class="sxs-lookup"><span data-stu-id="0e06b-104">Sends a ray into a search for hits in an acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e06b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e06b-105">Syntax</span></span>
<span data-ttu-id="0e06b-106">Это встроенное определение функции эквивалентно следующему шаблону функции:</span><span class="sxs-lookup"><span data-stu-id="0e06b-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a><span data-ttu-id="0e06b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e06b-107">Parameters</span></span>

`AccelerationStructure`

<span data-ttu-id="0e06b-108">Используемая структура ускорения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="0e06b-108">The top-level acceleration structure to use.</span></span> <span data-ttu-id="0e06b-109">Указание НУЛЕВой структуры ускорения приводит к неудаче.</span><span class="sxs-lookup"><span data-stu-id="0e06b-109">Specifying a NULL acceleration structure forces a miss.</span></span>

`RayFlags`

<span data-ttu-id="0e06b-110">Допустимое сочетание значений [ray_flag](ray_flag.md) .</span><span class="sxs-lookup"><span data-stu-id="0e06b-110">Valid combination of [ray_flag](ray_flag.md) values.</span></span> <span data-ttu-id="0e06b-111">Только определенные флаги лучей передаются системой, т. е. являются видимыми для встроенного шейдера [райфлагс](rayflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0e06b-111">Only defined ray flags are propagated by the system, i.e. are visible to the [RayFlags](rayflags.md) shader intrinsic.</span></span>

`InstanceInclusionMask`

<span data-ttu-id="0e06b-112">Целое число без знака, 8 нижних бит, которые используются для включения или отклонения экземпляров геометрических объектов на основе Инстанцемаск в каждом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="0e06b-112">An unsigned integer, the bottom 8 bits of which are used to include or reject geometry instances based on the InstanceMask in each instance.</span></span> <span data-ttu-id="0e06b-113">Пример:</span><span class="sxs-lookup"><span data-stu-id="0e06b-113">For example:</span></span>
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

<span data-ttu-id="0e06b-114">Целое число без знака, указывающее смещение, которое добавляется в вычисления адресации в таблицах шейдеров для индексирования групп попаданий.</span><span class="sxs-lookup"><span data-stu-id="0e06b-114">An unsigned integer specifying the offset to add into addressing calculations within shader tables for hit group indexing.</span></span>  <span data-ttu-id="0e06b-115">Используются только 4 нижних бита этого значения.</span><span class="sxs-lookup"><span data-stu-id="0e06b-115">Only the bottom 4 bits of this value are used.</span></span>

`MultiplierForGeometryContributionToHitGroupIndex`

<span data-ttu-id="0e06b-116">Целое число без знака, указывающее шаг для умножения на *жеометриконтрибутионтохитграупиндекс*, который является просто индексом, основанным на 0. геометрический объект был передан приложением в структуру ускорения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="0e06b-116">An unsigned integer specifying the stride to multiply by *GeometryContributionToHitGroupIndex*, which is just the 0 based index the geometry was supplied by the app into its bottom-level acceleration structure.</span></span> <span data-ttu-id="0e06b-117">Используются только нижние 16 бит этого значения множителя.</span><span class="sxs-lookup"><span data-stu-id="0e06b-117">Only the bottom 16 bits of this multiplier value are used.</span></span>

`MissShaderIndex`

<span data-ttu-id="0e06b-118">Целое число без знака, указывающее индекс незашифрованного шейдера в таблице шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0e06b-118">An unsigned integer specifying the index of the miss shader within a shader table.</span></span>

`Ray`

<span data-ttu-id="0e06b-119">Объект [**райдеск**](raydesc.md) , представляющий луча для трассировки.</span><span class="sxs-lookup"><span data-stu-id="0e06b-119">A [**RayDesc**](raydesc.md) representing the ray to be traced.</span></span>

`Payload`

<span data-ttu-id="0e06b-120">Определяемые пользователем полезные данные луча, доступные как для ввода, так и для вывода с помощью шейдеров, которые вызываются во время райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="0e06b-120">A user defined ray payload accessed both for both input and output by shaders invoked during raytracing.</span></span>  <span data-ttu-id="0e06b-121">После завершения [**трацерай**](traceray-function.md) вызывающий объект может также получить доступ к полезной нагрузке.</span><span class="sxs-lookup"><span data-stu-id="0e06b-121">After [**TraceRay**](traceray-function.md) completes, the caller can access the payload as well.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e06b-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e06b-122">Return Value</span></span>

<span data-ttu-id="0e06b-123">**void**</span><span class="sxs-lookup"><span data-stu-id="0e06b-123">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="0e06b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e06b-124">Remarks</span></span>

<span data-ttu-id="0e06b-125">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="0e06b-125">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="0e06b-126">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="0e06b-126">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="0e06b-127">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="0e06b-127">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="0e06b-128">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="0e06b-128">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="0e06b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e06b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e06b-130">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0e06b-130">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




