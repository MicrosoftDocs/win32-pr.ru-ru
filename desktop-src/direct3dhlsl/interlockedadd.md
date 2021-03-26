---
title: Функция Интерлоккедадд (Справочник по HLSL)
description: Выполняет гарантированное атомарное Добавление значения в переменную ресурса-приемника.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- Функция Интерлоккедадд HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d58965ea47fcad8452979a8c8ffe5b289392850
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "104412402"
---
# <a name="interlockedadd-function-hlsl-reference"></a><span data-ttu-id="71aca-104">Функция Интерлоккедадд (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="71aca-104">InterlockedAdd function (HLSL reference)</span></span>

<span data-ttu-id="71aca-105">Выполняет гарантированное атомарное Добавление значения в переменную ресурса-приемника.</span><span class="sxs-lookup"><span data-stu-id="71aca-105">Performs a guaranteed atomic add of value to the dest resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="71aca-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71aca-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="71aca-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71aca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71aca-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71aca-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71aca-109">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="71aca-109">Type: **R**</span></span>

<span data-ttu-id="71aca-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="71aca-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="71aca-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71aca-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71aca-112">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="71aca-112">Type: **T**</span></span>

<span data-ttu-id="71aca-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="71aca-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="71aca-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71aca-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71aca-115">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="71aca-115">Type: **T**</span></span>

<span data-ttu-id="71aca-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="71aca-116">Optional.</span></span> <span data-ttu-id="71aca-117">Исходное входное значение.</span><span class="sxs-lookup"><span data-stu-id="71aca-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71aca-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71aca-118">Return value</span></span>

<span data-ttu-id="71aca-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71aca-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71aca-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="71aca-120">Remarks</span></span>

<span data-ttu-id="71aca-121">Эта операция может выполняться только с типизированными ресурсами типа int или uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="71aca-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="71aca-122">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="71aca-122">There are two possible uses for this function.</span></span> <span data-ttu-id="71aca-123">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="71aca-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="71aca-124">В этом случае функция выполняет атомарное Добавление значения в регистр общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="71aca-124">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="71aca-125">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="71aca-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="71aca-126">В этом сценарии функция выполняет атомарное Добавление значения в расположение ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="71aca-126">In this scenario, the function performs an atomic add of value to the resource location referenced by dest.</span></span> <span data-ttu-id="71aca-127">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="71aca-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="71aca-128">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="71aca-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="71aca-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="71aca-129">Minimum Shader Model</span></span>

<span data-ttu-id="71aca-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="71aca-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71aca-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="71aca-131">Shader Model</span></span>                                                                | <span data-ttu-id="71aca-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="71aca-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="71aca-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="71aca-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="71aca-134">да</span><span class="sxs-lookup"><span data-stu-id="71aca-134">yes</span></span>       |



 

<span data-ttu-id="71aca-135">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="71aca-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="71aca-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="71aca-136">Vertex</span></span> | <span data-ttu-id="71aca-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="71aca-137">Hull</span></span> | <span data-ttu-id="71aca-138">Домен</span><span class="sxs-lookup"><span data-stu-id="71aca-138">Domain</span></span> | <span data-ttu-id="71aca-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="71aca-139">Geometry</span></span> | <span data-ttu-id="71aca-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="71aca-140">Pixel</span></span> | <span data-ttu-id="71aca-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="71aca-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="71aca-142">x</span><span class="sxs-lookup"><span data-stu-id="71aca-142">x</span></span>      | <span data-ttu-id="71aca-143">x</span><span class="sxs-lookup"><span data-stu-id="71aca-143">x</span></span>    | <span data-ttu-id="71aca-144">x</span><span class="sxs-lookup"><span data-stu-id="71aca-144">x</span></span>      | <span data-ttu-id="71aca-145">x</span><span class="sxs-lookup"><span data-stu-id="71aca-145">x</span></span>        | <span data-ttu-id="71aca-146">x</span><span class="sxs-lookup"><span data-stu-id="71aca-146">x</span></span>     | <span data-ttu-id="71aca-147">x</span><span class="sxs-lookup"><span data-stu-id="71aca-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71aca-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71aca-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aca-149">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="71aca-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="71aca-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="71aca-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




