---
title: Функция Интерлоккедкомпаресторе (Справочник по HLSL)
description: Атомарно сравнивает назначение со значением сравнения. Если они идентичны, то целевой объект перезаписывается входным значением.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Функция Интерлоккедкомпаресторе HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "104412406"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="cd214-105">Функция Интерлоккедкомпаресторе (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="cd214-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="cd214-106">Атомарно сравнивает назначение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="cd214-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="cd214-107">Если они идентичны, то целевой объект перезаписывается входным значением.</span><span class="sxs-lookup"><span data-stu-id="cd214-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd214-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd214-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="cd214-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd214-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd214-110">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd214-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd214-111">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="cd214-111">Type: **R**</span></span>

<span data-ttu-id="cd214-112">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="cd214-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="cd214-113">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cd214-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd214-114">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="cd214-114">Type: **T**</span></span>

<span data-ttu-id="cd214-115">Значение сравнения.</span><span class="sxs-lookup"><span data-stu-id="cd214-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="cd214-116">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd214-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd214-117">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="cd214-117">Type: **T**</span></span>

<span data-ttu-id="cd214-118">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="cd214-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd214-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd214-119">Return value</span></span>

<span data-ttu-id="cd214-120">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cd214-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd214-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd214-121">Remarks</span></span>

<span data-ttu-id="cd214-122">Атомарно сравнивает значение, на которое ссылается *dest* , *со \_ значением Compare* , и сохраняет *значение* в расположении, на которое ссылается *dest* , если значения совпадают.</span><span class="sxs-lookup"><span data-stu-id="cd214-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="cd214-123">Эта операция может выполняться только с типизированными ресурсами **типа int** или **uint** и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="cd214-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="cd214-124">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="cd214-124">There are two possible uses for this function.</span></span> <span data-ttu-id="cd214-125">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="cd214-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="cd214-126">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="cd214-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="cd214-127">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="cd214-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="cd214-128">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="cd214-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="cd214-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cd214-129">Minimum Shader Model</span></span>

<span data-ttu-id="cd214-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="cd214-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cd214-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cd214-131">Shader Model</span></span>                                                                | <span data-ttu-id="cd214-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd214-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cd214-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="cd214-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cd214-134">да</span><span class="sxs-lookup"><span data-stu-id="cd214-134">yes</span></span>       |



 

<span data-ttu-id="cd214-135">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="cd214-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cd214-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="cd214-136">Vertex</span></span> | <span data-ttu-id="cd214-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="cd214-137">Hull</span></span> | <span data-ttu-id="cd214-138">Домен</span><span class="sxs-lookup"><span data-stu-id="cd214-138">Domain</span></span> | <span data-ttu-id="cd214-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="cd214-139">Geometry</span></span> | <span data-ttu-id="cd214-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="cd214-140">Pixel</span></span> | <span data-ttu-id="cd214-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="cd214-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="cd214-142">x</span><span class="sxs-lookup"><span data-stu-id="cd214-142">x</span></span>     | <span data-ttu-id="cd214-143">x</span><span class="sxs-lookup"><span data-stu-id="cd214-143">x</span></span>    |  <span data-ttu-id="cd214-144">x</span><span class="sxs-lookup"><span data-stu-id="cd214-144">x</span></span>     |  <span data-ttu-id="cd214-145">x</span><span class="sxs-lookup"><span data-stu-id="cd214-145">x</span></span>       | <span data-ttu-id="cd214-146">x</span><span class="sxs-lookup"><span data-stu-id="cd214-146">x</span></span>     | <span data-ttu-id="cd214-147">x</span><span class="sxs-lookup"><span data-stu-id="cd214-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cd214-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd214-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd214-149">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="cd214-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="cd214-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="cd214-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




