---
title: mad - функция
description: Выполняет арифметическую операцию умножения или добавления для трех значений.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- Mad, функция HLSL
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487165"
---
# <a name="mad-function"></a><span data-ttu-id="31151-104">mad - функция</span><span class="sxs-lookup"><span data-stu-id="31151-104">mad function</span></span>

<span data-ttu-id="31151-105">Выполняет арифметическую операцию умножения или добавления для трех значений.</span><span class="sxs-lookup"><span data-stu-id="31151-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="31151-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31151-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="31151-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31151-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31151-108">*мвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31151-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31151-109">Тип: **numeric**</span><span class="sxs-lookup"><span data-stu-id="31151-109">Type: **numeric**</span></span>

<span data-ttu-id="31151-110">Значение умножения.</span><span class="sxs-lookup"><span data-stu-id="31151-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="31151-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31151-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31151-112">Тип: **numeric**</span><span class="sxs-lookup"><span data-stu-id="31151-112">Type: **numeric**</span></span>

<span data-ttu-id="31151-113">Первое сложение значения.</span><span class="sxs-lookup"><span data-stu-id="31151-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="31151-114">*bValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31151-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31151-115">Тип: **numeric**</span><span class="sxs-lookup"><span data-stu-id="31151-115">Type: **numeric**</span></span>

<span data-ttu-id="31151-116">Второе сложение.</span><span class="sxs-lookup"><span data-stu-id="31151-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31151-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31151-117">Return value</span></span>

<span data-ttu-id="31151-118">Тип: **numeric**</span><span class="sxs-lookup"><span data-stu-id="31151-118">Type: **numeric**</span></span>

<span data-ttu-id="31151-119">Результат *мвалуе* \* *значение*  +  *bValue*.</span><span class="sxs-lookup"><span data-stu-id="31151-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="31151-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="31151-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="31151-121">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="31151-121">Minimum Shader Model</span></span>

<span data-ttu-id="31151-122">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="31151-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="31151-123">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="31151-123">Shader Model</span></span>                                                                | <span data-ttu-id="31151-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="31151-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="31151-125">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="31151-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="31151-126">да</span><span class="sxs-lookup"><span data-stu-id="31151-126">yes</span></span>       |



 

<span data-ttu-id="31151-127">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="31151-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="31151-128">Вершина</span><span class="sxs-lookup"><span data-stu-id="31151-128">Vertex</span></span> | <span data-ttu-id="31151-129">Поверхности</span><span class="sxs-lookup"><span data-stu-id="31151-129">Hull</span></span> | <span data-ttu-id="31151-130">Домен</span><span class="sxs-lookup"><span data-stu-id="31151-130">Domain</span></span> | <span data-ttu-id="31151-131">Геометрия</span><span class="sxs-lookup"><span data-stu-id="31151-131">Geometry</span></span> | <span data-ttu-id="31151-132">Пиксель</span><span class="sxs-lookup"><span data-stu-id="31151-132">Pixel</span></span> | <span data-ttu-id="31151-133">Вычисления</span><span class="sxs-lookup"><span data-stu-id="31151-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="31151-134">x</span><span class="sxs-lookup"><span data-stu-id="31151-134">x</span></span>      | <span data-ttu-id="31151-135">x</span><span class="sxs-lookup"><span data-stu-id="31151-135">x</span></span>    | <span data-ttu-id="31151-136">x</span><span class="sxs-lookup"><span data-stu-id="31151-136">x</span></span>      | <span data-ttu-id="31151-137">x</span><span class="sxs-lookup"><span data-stu-id="31151-137">x</span></span>        | <span data-ttu-id="31151-138">x</span><span class="sxs-lookup"><span data-stu-id="31151-138">x</span></span>     | <span data-ttu-id="31151-139">x</span><span class="sxs-lookup"><span data-stu-id="31151-139">x</span></span>       |



 

<span data-ttu-id="31151-140">Авторы шейдеров могут использовать **Mad** встроенных для явного указания аппаратной инструкции **Mad** в скомпилированном выводе шейдера, что особенно полезно для шейдеров, помечающих результаты с помощью ключевого слова [точных](dx-graphics-hlsl-appendix-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="31151-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="31151-141">Инструкция **Mad** может быть реализована на оборудовании как "плавкий уровень", что обеспечивает более высокую точность, чем реализация инструкции **mul** , за которой следует инструкция **Add** , или как **mul**  +  **Add**.</span><span class="sxs-lookup"><span data-stu-id="31151-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="31151-142">Если авторы шейдеров используют команду **Mad** встроенных для вычисления результата, который помечается как точный, он указывает оборудованию использовать любую допустимую реализацию инструкции **Mad** (плавким предохранителем), если реализация согласуется для всех вариантов использования этой **Mad** в любом шейдере на этом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="31151-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="31151-143">Шейдер может использовать преимущества потенциального улучшения производительности, используя собственную инструкцию **Mad** (а не **mul**  +  **Add**) на определенном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="31151-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="31151-144">Результат выполнения машинной инструкции **Mad** может отличаться от выполнения **mul** , за которым следует **Add**.</span><span class="sxs-lookup"><span data-stu-id="31151-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="31151-145">Однако что угодно, результат должен быть единообразным для одной и той же операции в нескольких шейдерах или в разных частях шейдера.</span><span class="sxs-lookup"><span data-stu-id="31151-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="31151-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31151-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31151-147">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="31151-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="31151-148">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="31151-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




