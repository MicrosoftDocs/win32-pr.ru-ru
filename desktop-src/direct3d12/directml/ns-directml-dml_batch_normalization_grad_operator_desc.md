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
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804522"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="59b6d-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="59b6d-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="59b6d-104">Вычисляются градиенты обратного распространения для [нормализации пакетной обработки](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="59b6d-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="59b6d-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** выполняет несколько вычислений, которые подробно описаны в отдельных выходных описаниях.</span><span class="sxs-lookup"><span data-stu-id="59b6d-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59b6d-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="59b6d-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="59b6d-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="59b6d-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59b6d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59b6d-108">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="59b6d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="59b6d-109">Members</span></span>

`InputTensor`

<span data-ttu-id="59b6d-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-111">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="59b6d-111">A tensor containing the input data.</span></span> <span data-ttu-id="59b6d-112">Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="59b6d-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="59b6d-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="59b6d-114">The incoming gradient tensor.</span></span> <span data-ttu-id="59b6d-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="59b6d-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="59b6d-116">Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="59b6d-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-118">Объект тензорные, содержащий средние данные.</span><span class="sxs-lookup"><span data-stu-id="59b6d-118">A tensor containing the mean data.</span></span> <span data-ttu-id="59b6d-119">Обычно это те же тензорные, которые были предоставлены в качестве *меантенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="59b6d-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="59b6d-120">Все измерения, размер которых отличается от размера соответствующего измерения *инпуттенсор* , должны иметь размер 1, чтобы их можно было транслировать в соответствии с входными данными.</span><span class="sxs-lookup"><span data-stu-id="59b6d-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="59b6d-121">Например, допустимы следующие размеры.</span><span class="sxs-lookup"><span data-stu-id="59b6d-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="59b6d-122">Ниже приведена ошибка, так как для обеспечения совместимости с широковещательной рассылкой все измерения, которые не соответствуют, должны иметь размер 1.</span><span class="sxs-lookup"><span data-stu-id="59b6d-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="59b6d-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-124">Объект тензорные, содержащий данные дисперсии.</span><span class="sxs-lookup"><span data-stu-id="59b6d-124">A tensor containing the variance data.</span></span> <span data-ttu-id="59b6d-125">Обычно это те же тензорные, которые были предоставлены в качестве *варианцетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="59b6d-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="59b6d-126">Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="59b6d-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-128">Объект тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="59b6d-128">A tensor containing the scale data.</span></span> <span data-ttu-id="59b6d-129">Обычно это те же тензорные, которые были предоставлены в качестве *скалетенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="59b6d-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="59b6d-130">Этот тензорные должен иметь те же размеры измерений, что и *меантенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="59b6d-131">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-132">Для каждого соответствующего значения во входных данных — `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="59b6d-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="59b6d-133">Этот тензорные должен иметь те же размеры измерений, что и *инпуттенсор* / *инпутградиенттенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="59b6d-134">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-135">Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="59b6d-136">Выполняются следующие вычисления или каждое соответствующее значение во входных данных.</span><span class="sxs-lookup"><span data-stu-id="59b6d-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="59b6d-137">`sum`Вычисляются для всех измерений, которые необходимо транслировать.</span><span class="sxs-lookup"><span data-stu-id="59b6d-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="59b6d-138">Если вещание не требуется, сумма не требуется.</span><span class="sxs-lookup"><span data-stu-id="59b6d-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="59b6d-139">Пример приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="59b6d-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="59b6d-140">Элемент [0, **0**, 0, 0] из `OutputScaleGradientTensor` является суммой `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` для всех элементов 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].</span><span class="sxs-lookup"><span data-stu-id="59b6d-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="59b6d-141">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="59b6d-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="59b6d-142">Эти тензорные должны иметь те же размеры измерений, что и *меантенсор* / *варианцетенсор* / *скалетенсор*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="59b6d-143">Выполняются следующие вычисления или каждое соответствующее значение во входных данных.</span><span class="sxs-lookup"><span data-stu-id="59b6d-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="59b6d-144">Значение `sum` вычисляются для всех измерений, которые необходимо транслировать (см. пример для *аутпутскалеградиенттенсор*).</span><span class="sxs-lookup"><span data-stu-id="59b6d-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="59b6d-145">Если вещание не требуется, сумма не требуется.</span><span class="sxs-lookup"><span data-stu-id="59b6d-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="59b6d-146">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="59b6d-146">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="59b6d-147">Небольшое значение, добавляемое к дисперсии, чтобы избежать нулевого значения.</span><span class="sxs-lookup"><span data-stu-id="59b6d-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="59b6d-148">Доступность</span><span class="sxs-lookup"><span data-stu-id="59b6d-148">Availability</span></span>
<span data-ttu-id="59b6d-149">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="59b6d-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="59b6d-150">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="59b6d-150">Tensor constraints</span></span>
<span data-ttu-id="59b6d-151">*Инпутградиенттенсор*, *инпуттенсор*, *меантенсор*, *аутпутбиасградиенттенсор*, *аутпутградиенттенсор*, *OutputScaleGradientTensor*, *ScaleTensor* и *VarianceTensor* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="59b6d-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="59b6d-152">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="59b6d-152">Tensor support</span></span>
| <span data-ttu-id="59b6d-153">Тензорные</span><span class="sxs-lookup"><span data-stu-id="59b6d-153">Tensor</span></span> | <span data-ttu-id="59b6d-154">Вид</span><span class="sxs-lookup"><span data-stu-id="59b6d-154">Kind</span></span> | <span data-ttu-id="59b6d-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="59b6d-155">Supported dimension counts</span></span> | <span data-ttu-id="59b6d-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="59b6d-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="59b6d-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-157">InputTensor</span></span> | <span data-ttu-id="59b6d-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-158">Input</span></span> | <span data-ttu-id="59b6d-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-159">1 to 8</span></span> | <span data-ttu-id="59b6d-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-161">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-161">InputGradientTensor</span></span> | <span data-ttu-id="59b6d-162">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-162">Input</span></span> | <span data-ttu-id="59b6d-163">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-163">1 to 8</span></span> | <span data-ttu-id="59b6d-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-165">меантенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-165">MeanTensor</span></span> | <span data-ttu-id="59b6d-166">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-166">Input</span></span> | <span data-ttu-id="59b6d-167">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-167">1 to 8</span></span> | <span data-ttu-id="59b6d-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-169">варианцетенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-169">VarianceTensor</span></span> | <span data-ttu-id="59b6d-170">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-170">Input</span></span> | <span data-ttu-id="59b6d-171">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-171">1 to 8</span></span> | <span data-ttu-id="59b6d-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-173">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-173">ScaleTensor</span></span> | <span data-ttu-id="59b6d-174">Входные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-174">Input</span></span> | <span data-ttu-id="59b6d-175">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-175">1 to 8</span></span> | <span data-ttu-id="59b6d-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-177">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-177">OutputGradientTensor</span></span> | <span data-ttu-id="59b6d-178">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-178">Output</span></span> | <span data-ttu-id="59b6d-179">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-179">1 to 8</span></span> | <span data-ttu-id="59b6d-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-181">аутпутскалеградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="59b6d-182">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-182">Output</span></span> | <span data-ttu-id="59b6d-183">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-183">1 to 8</span></span> | <span data-ttu-id="59b6d-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="59b6d-185">аутпутбиасградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="59b6d-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="59b6d-186">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="59b6d-186">Output</span></span> | <span data-ttu-id="59b6d-187">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="59b6d-187">1 to 8</span></span> | <span data-ttu-id="59b6d-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="59b6d-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="59b6d-189">Требования</span><span class="sxs-lookup"><span data-stu-id="59b6d-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="59b6d-190">**Header**</span><span class="sxs-lookup"><span data-stu-id="59b6d-190">**Header**</span></span> | <span data-ttu-id="59b6d-191">директмл. h</span><span class="sxs-lookup"><span data-stu-id="59b6d-191">directml.h</span></span> |
