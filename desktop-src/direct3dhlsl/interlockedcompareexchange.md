---
title: Функция Интерлоккедкомпариксчанже (Справочник по HLSL)
description: Атомарно сравнивает назначение со значением сравнения. Если они идентичны, то целевой объект перезаписывается входным значением. Исходное значение устанавливается в исходное значение назначения.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Функция Интерлоккедкомпариксчанже HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "104997026"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="03eaa-106">Функция Интерлоккедкомпариксчанже (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="03eaa-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="03eaa-107">Атомарно сравнивает назначение со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="03eaa-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="03eaa-108">Если они идентичны, то целевой объект перезаписывается входным значением.</span><span class="sxs-lookup"><span data-stu-id="03eaa-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="03eaa-109">Исходное значение устанавливается в исходное значение назначения.</span><span class="sxs-lookup"><span data-stu-id="03eaa-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="03eaa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03eaa-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="03eaa-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="03eaa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03eaa-112">*конечный адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03eaa-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03eaa-113">Тип: **R**</span><span class="sxs-lookup"><span data-stu-id="03eaa-113">Type: **R**</span></span>

<span data-ttu-id="03eaa-114">Адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="03eaa-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="03eaa-115">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="03eaa-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03eaa-116">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="03eaa-116">Type: **T**</span></span>

<span data-ttu-id="03eaa-117">Значение сравнения.</span><span class="sxs-lookup"><span data-stu-id="03eaa-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="03eaa-118">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03eaa-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03eaa-119">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="03eaa-119">Type: **T**</span></span>

<span data-ttu-id="03eaa-120">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="03eaa-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="03eaa-121">*исходное \_ значение* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="03eaa-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03eaa-122">Тип: **T**</span><span class="sxs-lookup"><span data-stu-id="03eaa-122">Type: **T**</span></span>

<span data-ttu-id="03eaa-123">Исходное значение.</span><span class="sxs-lookup"><span data-stu-id="03eaa-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03eaa-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03eaa-124">Return value</span></span>

<span data-ttu-id="03eaa-125">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03eaa-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03eaa-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="03eaa-126">Remarks</span></span>

<span data-ttu-id="03eaa-127">Атомарно сравнивает значение, на которое ссылается *dest* со *\_ значением сравнения*, сохраняет *значение* в расположении, на которое ссылается *dest* , если значения совпадают, возвращает исходное значение *dest* в *исходном \_ значении*.</span><span class="sxs-lookup"><span data-stu-id="03eaa-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="03eaa-128">Эта операция может выполняться только с типизированными ресурсами **типа int** или **uint** и переменными общей памяти.</span><span class="sxs-lookup"><span data-stu-id="03eaa-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="03eaa-129">Существует два возможных использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="03eaa-129">There are two possible uses for this function.</span></span> <span data-ttu-id="03eaa-130">Первый — когда R является переменной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="03eaa-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="03eaa-131">В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="03eaa-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="03eaa-132">Второй сценарий заключается в том, что R является типом переменной ресурса.</span><span class="sxs-lookup"><span data-stu-id="03eaa-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="03eaa-133">В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается *dest*.</span><span class="sxs-lookup"><span data-stu-id="03eaa-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="03eaa-134">Эта операция доступна только в том случае, если R доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="03eaa-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="03eaa-135">Если вы вызываете **интерлоккедкомпариксчанже** в цикле [**for**](dx-graphics-hlsl-for.md) или [**while**](dx-graphics-hlsl-while.md) COMPUTE, для правильной компиляции необходимо использовать атрибут **\[ allow \_ UAV \_ Condition \]** в этом цикле.</span><span class="sxs-lookup"><span data-stu-id="03eaa-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="03eaa-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="03eaa-136">Minimum Shader Model</span></span>

<span data-ttu-id="03eaa-137">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="03eaa-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="03eaa-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="03eaa-138">Shader Model</span></span>                                                                | <span data-ttu-id="03eaa-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="03eaa-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="03eaa-140">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="03eaa-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="03eaa-141">да</span><span class="sxs-lookup"><span data-stu-id="03eaa-141">yes</span></span>       |



 

<span data-ttu-id="03eaa-142">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="03eaa-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="03eaa-143">Вершина</span><span class="sxs-lookup"><span data-stu-id="03eaa-143">Vertex</span></span> | <span data-ttu-id="03eaa-144">Поверхности</span><span class="sxs-lookup"><span data-stu-id="03eaa-144">Hull</span></span> | <span data-ttu-id="03eaa-145">Домен</span><span class="sxs-lookup"><span data-stu-id="03eaa-145">Domain</span></span> | <span data-ttu-id="03eaa-146">Геометрия</span><span class="sxs-lookup"><span data-stu-id="03eaa-146">Geometry</span></span> | <span data-ttu-id="03eaa-147">Пиксель</span><span class="sxs-lookup"><span data-stu-id="03eaa-147">Pixel</span></span> | <span data-ttu-id="03eaa-148">Вычисления</span><span class="sxs-lookup"><span data-stu-id="03eaa-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="03eaa-149">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-149">x</span></span>      |  <span data-ttu-id="03eaa-150">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-150">x</span></span>   |  <span data-ttu-id="03eaa-151">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-151">x</span></span>     |  <span data-ttu-id="03eaa-152">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-152">x</span></span>       | <span data-ttu-id="03eaa-153">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-153">x</span></span>     | <span data-ttu-id="03eaa-154">x</span><span class="sxs-lookup"><span data-stu-id="03eaa-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="03eaa-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03eaa-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03eaa-156">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="03eaa-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="03eaa-157">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="03eaa-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




