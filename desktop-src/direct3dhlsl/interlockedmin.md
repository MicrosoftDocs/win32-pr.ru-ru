---
title: Функция Интерлоккедмин (Справочник по HLSL)
description: Выполняет гарантированную атомарную минуту.
ms.assetid: a6d3d81c-45d7-4e15-b8ec-fa2e30f854ce
keywords:
- Функция Интерлоккедмин HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c85be82f87ce62d03c824e8cd895166c18c262c
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "104412404"
---
# <a name="interlockedmin-function-hlsl-reference"></a><span data-ttu-id="ffad7-104">Функция Интерлоккедмин (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffad7-104">InterlockedMin function (HLSL reference)</span></span>

<span data-ttu-id="ffad7-105">Выполняет гарантированную атомарную минуту.</span><span class="sxs-lookup"><span data-stu-id="ffad7-105">Performs a guaranteed atomic min.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffad7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffad7-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="ffad7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffad7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffad7-108">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffad7-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad7-109">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="ffad7-109">Type: **R**</span></span>

<span data-ttu-id="ffad7-110">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="ffad7-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ffad7-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffad7-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad7-112">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="ffad7-112">Type: **T**</span></span>

<span data-ttu-id="ffad7-113">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="ffad7-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ffad7-114">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ffad7-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffad7-115">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="ffad7-115">Type: **T**</span></span>

<span data-ttu-id="ffad7-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ffad7-116">Optional.</span></span> <span data-ttu-id="ffad7-117">Исходное входное значение.</span><span class="sxs-lookup"><span data-stu-id="ffad7-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffad7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffad7-118">Return value</span></span>

<span data-ttu-id="ffad7-119">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ffad7-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffad7-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ffad7-120">Remarks</span></span>

<span data-ttu-id="ffad7-121">Эта операция может выполняться только с типизированными ресурсами int и uint и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="ffad7-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="ffad7-122">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="ffad7-122">There are two possible uses for this function.</span></span> <span data-ttu-id="ffad7-123">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="ffad7-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="ffad7-124">В этом случае функция выполняет атомарный минимум значения в регистр общей памяти, на который ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="ffad7-124">In this case, the function performs an atomic min of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="ffad7-125">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="ffad7-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="ffad7-126">В этом сценарии функция выполняет атомарную минуту значения в расположении ресурса, на которое ссылается dest.</span><span class="sxs-lookup"><span data-stu-id="ffad7-126">In this scenario, the function performs an atomic min of value to the resource location referenced by dest.</span></span> <span data-ttu-id="ffad7-127">Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest.</span><span class="sxs-lookup"><span data-stu-id="ffad7-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="ffad7-128">Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ffad7-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="ffad7-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ffad7-129">Minimum Shader Model</span></span>

<span data-ttu-id="ffad7-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ffad7-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ffad7-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ffad7-131">Shader Model</span></span>                                                                | <span data-ttu-id="ffad7-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ffad7-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ffad7-133">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="ffad7-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ffad7-134">да</span><span class="sxs-lookup"><span data-stu-id="ffad7-134">yes</span></span>       |



 

<span data-ttu-id="ffad7-135">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ffad7-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ffad7-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="ffad7-136">Vertex</span></span> | <span data-ttu-id="ffad7-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ffad7-137">Hull</span></span> | <span data-ttu-id="ffad7-138">Домен</span><span class="sxs-lookup"><span data-stu-id="ffad7-138">Domain</span></span> | <span data-ttu-id="ffad7-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ffad7-139">Geometry</span></span> | <span data-ttu-id="ffad7-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ffad7-140">Pixel</span></span> | <span data-ttu-id="ffad7-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ffad7-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ffad7-142">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-142">x</span></span>      |  <span data-ttu-id="ffad7-143">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-143">x</span></span>   |  <span data-ttu-id="ffad7-144">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-144">x</span></span>     |  <span data-ttu-id="ffad7-145">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-145">x</span></span>       | <span data-ttu-id="ffad7-146">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-146">x</span></span>     | <span data-ttu-id="ffad7-147">x</span><span class="sxs-lookup"><span data-stu-id="ffad7-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ffad7-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffad7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffad7-149">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="ffad7-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="ffad7-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ffad7-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




