---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Вычисляются градиенты обратного распространения для [нормализации пакетной обработки](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550439"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="cd065-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="cd065-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="cd065-104">Вычисляются градиенты обратного распространения для [нормализации пакетной обработки](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cd065-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="cd065-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** выполняет несколько вычислений, которые подробно описаны в отдельных выходных описаниях.</span><span class="sxs-lookup"><span data-stu-id="cd065-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd065-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="cd065-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="cd065-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cd065-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd065-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd065-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="cd065-109">Участники</span><span class="sxs-lookup"><span data-stu-id="cd065-109">Members</span></span>

`InputTensor`

<span data-ttu-id="cd065-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-111">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="cd065-111">A tensor containing the input data.</span></span> <span data-ttu-id="cd065-112">Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="cd065-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="cd065-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="cd065-114">The incoming gradient tensor.</span></span> <span data-ttu-id="cd065-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="cd065-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="cd065-116">Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="cd065-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-118">Объект тензорные, содержащий средние данные.</span><span class="sxs-lookup"><span data-stu-id="cd065-118">A tensor containing the mean data.</span></span> <span data-ttu-id="cd065-119">Обычно это те же тензорные, которые были предоставлены в качестве *меантенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="cd065-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="cd065-120">Все измерения, размер которых отличается от размера соответствующего измерения *инпуттенсор* , должны иметь размер 1, чтобы их можно было транслировать в соответствии с входными данными.</span><span class="sxs-lookup"><span data-stu-id="cd065-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="cd065-121">Например, допустимы следующие размеры.</span><span class="sxs-lookup"><span data-stu-id="cd065-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="cd065-122">Ниже приведена ошибка, так как для обеспечения совместимости с широковещательной рассылкой все измерения, которые не соответствуют, должны иметь размер 1.</span><span class="sxs-lookup"><span data-stu-id="cd065-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="cd065-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-124">Объект тензорные, содержащий данные дисперсии.</span><span class="sxs-lookup"><span data-stu-id="cd065-124">A tensor containing the variance data.</span></span> <span data-ttu-id="cd065-125">Обычно это те же тензорные, которые были предоставлены в качестве *варианцетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="cd065-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="cd065-126">Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="cd065-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-128">Объект тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="cd065-128">A tensor containing the scale data.</span></span> <span data-ttu-id="cd065-129">Обычно это те же тензорные, которые были предоставлены в качестве *скалетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="cd065-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="cd065-130">Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="cd065-131">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-132">Для каждого соответствующего значения во входных данных — `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="cd065-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="cd065-133">Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор* / *инпутградиенттенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="cd065-134">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-135">Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="cd065-136">Выполняются следующие вычисления или каждое соответствующее значение во входных данных.</span><span class="sxs-lookup"><span data-stu-id="cd065-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="cd065-137">`sum`Вычисляются для всех измерений, которые необходимо транслировать.</span><span class="sxs-lookup"><span data-stu-id="cd065-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="cd065-138">Если вещание не требуется, сумма не требуется.</span><span class="sxs-lookup"><span data-stu-id="cd065-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="cd065-139">Пример приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="cd065-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="cd065-140">Элемент [0, **0**, 0, 0] из `OutputScaleGradientTensor` является суммой `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` для всех элементов 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].</span><span class="sxs-lookup"><span data-stu-id="cd065-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="cd065-141">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd065-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd065-142">Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.</span><span class="sxs-lookup"><span data-stu-id="cd065-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="cd065-143">Выполняются следующие вычисления или каждое соответствующее значение во входных данных.</span><span class="sxs-lookup"><span data-stu-id="cd065-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="cd065-144">Значение `sum` вычисляются для всех измерений, которые необходимо транслировать (см. пример для *аутпутскалеградиенттенсор*).</span><span class="sxs-lookup"><span data-stu-id="cd065-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="cd065-145">Если вещание не требуется, сумма не требуется.</span><span class="sxs-lookup"><span data-stu-id="cd065-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="cd065-146">Тип: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd065-146">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd065-147">Небольшое значение, добавляемое к дисперсии, чтобы избежать нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="cd065-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="cd065-148">Доступность</span><span class="sxs-lookup"><span data-stu-id="cd065-148">Availability</span></span>
<span data-ttu-id="cd065-149">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="cd065-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cd065-150">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="cd065-150">Tensor constraints</span></span>
<span data-ttu-id="cd065-151">*Инпутградиенттенсор*, *инпуттенсор*, *меантенсор*, *аутпутбиасградиенттенсор*, *аутпутградиенттенсор*, *OutputScaleGradientTensor*, *ScaleTensor* и *VarianceTensor* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="cd065-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cd065-152">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="cd065-152">Tensor support</span></span>
| <span data-ttu-id="cd065-153">Тензорные</span><span class="sxs-lookup"><span data-stu-id="cd065-153">Tensor</span></span> | <span data-ttu-id="cd065-154">Вид</span><span class="sxs-lookup"><span data-stu-id="cd065-154">Kind</span></span> | <span data-ttu-id="cd065-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="cd065-155">Supported dimension counts</span></span> | <span data-ttu-id="cd065-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="cd065-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd065-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-157">InputTensor</span></span> | <span data-ttu-id="cd065-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-158">Input</span></span> | <span data-ttu-id="cd065-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-159">1 to 8</span></span> | <span data-ttu-id="cd065-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-161">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-161">InputGradientTensor</span></span> | <span data-ttu-id="cd065-162">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-162">Input</span></span> | <span data-ttu-id="cd065-163">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-163">1 to 8</span></span> | <span data-ttu-id="cd065-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-165">меантенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-165">MeanTensor</span></span> | <span data-ttu-id="cd065-166">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-166">Input</span></span> | <span data-ttu-id="cd065-167">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-167">1 to 8</span></span> | <span data-ttu-id="cd065-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-169">варианцетенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-169">VarianceTensor</span></span> | <span data-ttu-id="cd065-170">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-170">Input</span></span> | <span data-ttu-id="cd065-171">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-171">1 to 8</span></span> | <span data-ttu-id="cd065-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-173">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-173">ScaleTensor</span></span> | <span data-ttu-id="cd065-174">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-174">Input</span></span> | <span data-ttu-id="cd065-175">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-175">1 to 8</span></span> | <span data-ttu-id="cd065-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-177">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-177">OutputGradientTensor</span></span> | <span data-ttu-id="cd065-178">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-178">Output</span></span> | <span data-ttu-id="cd065-179">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-179">1 to 8</span></span> | <span data-ttu-id="cd065-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-181">аутпутскалеградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="cd065-182">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-182">Output</span></span> | <span data-ttu-id="cd065-183">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-183">1 to 8</span></span> | <span data-ttu-id="cd065-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cd065-185">аутпутбиасградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="cd065-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="cd065-186">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="cd065-186">Output</span></span> | <span data-ttu-id="cd065-187">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="cd065-187">1 to 8</span></span> | <span data-ttu-id="cd065-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cd065-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="cd065-189">Требования</span><span class="sxs-lookup"><span data-stu-id="cd065-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd065-190">**Header**</span><span class="sxs-lookup"><span data-stu-id="cd065-190">**Header**</span></span> | <span data-ttu-id="cd065-191">директмл. h</span><span class="sxs-lookup"><span data-stu-id="cd065-191">directml.h</span></span> |