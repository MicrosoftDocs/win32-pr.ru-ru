---
title: Функция Интерлоккедексчанже (Справочник по HLSL)
description: Присваивает значение dest и возвращает исходное значение.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Функция Интерлоккедексчанже HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "104983952"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="113c9-104">Функция Интерлоккедексчанже (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="113c9-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="113c9-105">Присваивает значение dest и возвращает исходное значение.</span><span class="sxs-lookup"><span data-stu-id="113c9-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="113c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="113c9-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="113c9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="113c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113c9-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="113c9-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113c9-109">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="113c9-109">Type: **R**</span></span>

<span data-ttu-id="113c9-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="113c9-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="113c9-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="113c9-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113c9-112">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="113c9-112">Type: **T**</span></span>

<span data-ttu-id="113c9-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="113c9-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="113c9-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="113c9-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="113c9-115">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="113c9-115">Type: **T**</span></span>

<span data-ttu-id="113c9-116">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="113c9-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113c9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="113c9-117">Return value</span></span>

<span data-ttu-id="113c9-118">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="113c9-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="113c9-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="113c9-119">Remarks</span></span>

<span data-ttu-id="113c9-120">Эта операция может выполняться только с скалярными ресурсами и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="113c9-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="113c9-121">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="113c9-121">There are two possible uses for this function.</span></span> <span data-ttu-id="113c9-122">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="113c9-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="113c9-123">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="113c9-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="113c9-124">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="113c9-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="113c9-125">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="113c9-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="113c9-126">Эта операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="113c9-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="113c9-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="113c9-127">Minimum Shader Model</span></span>

<span data-ttu-id="113c9-128">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="113c9-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="113c9-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="113c9-129">Shader Model</span></span>                                                                | <span data-ttu-id="113c9-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="113c9-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="113c9-131">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="113c9-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="113c9-132">да</span><span class="sxs-lookup"><span data-stu-id="113c9-132">yes</span></span>       |



 

<span data-ttu-id="113c9-133">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="113c9-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="113c9-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="113c9-134">Vertex</span></span> | <span data-ttu-id="113c9-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="113c9-135">Hull</span></span> | <span data-ttu-id="113c9-136">Домен</span><span class="sxs-lookup"><span data-stu-id="113c9-136">Domain</span></span> | <span data-ttu-id="113c9-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="113c9-137">Geometry</span></span> | <span data-ttu-id="113c9-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="113c9-138">Pixel</span></span> | <span data-ttu-id="113c9-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="113c9-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="113c9-140">x</span><span class="sxs-lookup"><span data-stu-id="113c9-140">x</span></span>      |  <span data-ttu-id="113c9-141">x</span><span class="sxs-lookup"><span data-stu-id="113c9-141">x</span></span>   | <span data-ttu-id="113c9-142">x</span><span class="sxs-lookup"><span data-stu-id="113c9-142">x</span></span>      |  <span data-ttu-id="113c9-143">x</span><span class="sxs-lookup"><span data-stu-id="113c9-143">x</span></span>       | <span data-ttu-id="113c9-144">x</span><span class="sxs-lookup"><span data-stu-id="113c9-144">x</span></span>     | <span data-ttu-id="113c9-145">x</span><span class="sxs-lookup"><span data-stu-id="113c9-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="113c9-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="113c9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113c9-147">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="113c9-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="113c9-148">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="113c9-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




