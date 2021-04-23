---
title: Функция Интерлоккедксор (Справочник по HLSL)
description: Выполняет гарантированный атомарный XOR.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- Функция Интерлоккедксор HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "103785610"
---
# <a name="interlockedxor-function-hlsl-reference"></a><span data-ttu-id="451b5-104">Функция Интерлоккедксор (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="451b5-104">InterlockedXor function (HLSL reference)</span></span>

<span data-ttu-id="451b5-105">Выполняет гарантированный атомарный XOR.</span><span class="sxs-lookup"><span data-stu-id="451b5-105">Performs a guaranteed atomic xor.</span></span>

## <a name="syntax"></a><span data-ttu-id="451b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="451b5-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="451b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="451b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451b5-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="451b5-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451b5-109">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="451b5-109">Type: **R**</span></span>

<span data-ttu-id="451b5-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="451b5-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="451b5-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="451b5-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451b5-112">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="451b5-112">Type: **T**</span></span>

<span data-ttu-id="451b5-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="451b5-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="451b5-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="451b5-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="451b5-115">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="451b5-115">Type: **T**</span></span>

<span data-ttu-id="451b5-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="451b5-116">Optional.</span></span> <span data-ttu-id="451b5-117">Исходное входное значение.</span><span class="sxs-lookup"><span data-stu-id="451b5-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451b5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="451b5-118">Return value</span></span>

<span data-ttu-id="451b5-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="451b5-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="451b5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="451b5-120">Remarks</span></span>

<span data-ttu-id="451b5-121">Эта операция может выполняться только с типизированными ресурсами типа int или uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="451b5-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="451b5-122">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="451b5-122">There are two possible uses for this function.</span></span> <span data-ttu-id="451b5-123">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="451b5-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="451b5-124">В этом случае функция выполняет атомарное исключающее XOR значения для регистра общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="451b5-124">In this case, the function performs an atomic XOR of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="451b5-125">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="451b5-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="451b5-126">В этом сценарии функция выполняет атомарное значение Ксороф для расположения ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="451b5-126">In this scenario, the function performs an atomic XORof value to the resource location referenced by dest.</span></span> <span data-ttu-id="451b5-127">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="451b5-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="451b5-128">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="451b5-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="451b5-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="451b5-129">Minimum Shader Model</span></span>

<span data-ttu-id="451b5-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="451b5-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="451b5-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="451b5-131">Shader Model</span></span>                                                                | <span data-ttu-id="451b5-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="451b5-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="451b5-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="451b5-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="451b5-134">да</span><span class="sxs-lookup"><span data-stu-id="451b5-134">yes</span></span>       |



 

<span data-ttu-id="451b5-135">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="451b5-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="451b5-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="451b5-136">Vertex</span></span> | <span data-ttu-id="451b5-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="451b5-137">Hull</span></span> | <span data-ttu-id="451b5-138">Домен</span><span class="sxs-lookup"><span data-stu-id="451b5-138">Domain</span></span> | <span data-ttu-id="451b5-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="451b5-139">Geometry</span></span> | <span data-ttu-id="451b5-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="451b5-140">Pixel</span></span> | <span data-ttu-id="451b5-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="451b5-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="451b5-142">x</span><span class="sxs-lookup"><span data-stu-id="451b5-142">x</span></span>     |  <span data-ttu-id="451b5-143">x</span><span class="sxs-lookup"><span data-stu-id="451b5-143">x</span></span>   | <span data-ttu-id="451b5-144">x</span><span class="sxs-lookup"><span data-stu-id="451b5-144">x</span></span>      |  <span data-ttu-id="451b5-145">x</span><span class="sxs-lookup"><span data-stu-id="451b5-145">x</span></span>       | <span data-ttu-id="451b5-146">x</span><span class="sxs-lookup"><span data-stu-id="451b5-146">x</span></span>     | <span data-ttu-id="451b5-147">x</span><span class="sxs-lookup"><span data-stu-id="451b5-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="451b5-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="451b5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451b5-149">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="451b5-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="451b5-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="451b5-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




