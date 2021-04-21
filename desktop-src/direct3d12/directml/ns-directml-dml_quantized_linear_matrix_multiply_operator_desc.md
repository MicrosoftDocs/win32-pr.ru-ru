---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Выполняет функцию умножения матрицы для данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, затем выполняет умножение матрицы и затем куантизинг выходные данные.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803565"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="34338-104">Структура DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="34338-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="34338-105">Выполняет функцию умножения матрицы для данных квантования.</span><span class="sxs-lookup"><span data-stu-id="34338-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="34338-106">Этот оператор математически эквивалентен декуантизинг входным данным, затем выполняет умножение матрицы и затем куантизинг выходные данные.</span><span class="sxs-lookup"><span data-stu-id="34338-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="34338-107">Этот оператор требует, чтобы матрица ввода данных с десятков входов в значение 4D была отформатирована как `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="34338-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="34338-108">Оператор умножения матрицы выполняет Батчкаунт \* Чаннелкаунт число независимых матричных матриц.</span><span class="sxs-lookup"><span data-stu-id="34338-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="34338-109">Например, если *атенсор* имеет *размеры* `{ BatchCount, ChannelCount, M, K }` , а *бтенсор* имеет размеры,  `{ BatchCount, ChannelCount, K, N }` а *аутпуттенсор* имеет *размеры* , `{ BatchCount, ChannelCount, M, N }` то оператор умножения матрицы будет выполнять батчкаунт \* чаннелкаунт независимых матричных умножений измерений {m, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="34338-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="34338-110">Функция декуантизе</span><span class="sxs-lookup"><span data-stu-id="34338-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="34338-111">Функция квантуем</span><span class="sxs-lookup"><span data-stu-id="34338-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="34338-112">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="34338-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="34338-113">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="34338-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34338-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34338-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="34338-115">Члены</span><span class="sxs-lookup"><span data-stu-id="34338-115">Members</span></span>

`ATensor`

<span data-ttu-id="34338-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-117">Объект тензорные, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="34338-117">A tensor containing the A data.</span></span> <span data-ttu-id="34338-118">Размеры тензорные должны быть `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="34338-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="34338-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-120">Объект тензорные, содержащий данные шкалы Атенсор.</span><span class="sxs-lookup"><span data-stu-id="34338-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="34338-121">Ожидаемые размеры элемента `AScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется дискретизация строки.</span><span class="sxs-lookup"><span data-stu-id="34338-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="34338-122">Эти значения масштаба используются для декуантизинг значений.</span><span class="sxs-lookup"><span data-stu-id="34338-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="34338-123">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-124">Необязательный тензорные, содержащий данные нулевой точки *атенсор* .</span><span class="sxs-lookup"><span data-stu-id="34338-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="34338-125">Ожидаемые размеры Азеропоинттенсор, `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется строка дискретизация.</span><span class="sxs-lookup"><span data-stu-id="34338-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="34338-126">Эти значения нулевых точек используются для декуантизинг значений Атенсор.</span><span class="sxs-lookup"><span data-stu-id="34338-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="34338-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-128">Объект тензорные, содержащий данные B.</span><span class="sxs-lookup"><span data-stu-id="34338-128">A tensor containing the B data.</span></span> <span data-ttu-id="34338-129">Размеры тензорные должны быть `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="34338-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="34338-130">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-131">Объект тензорные, содержащий данные шкалы *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="34338-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="34338-132">Ожидаемые размеры элемента `BScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация.</span><span class="sxs-lookup"><span data-stu-id="34338-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="34338-133">Эти значения масштаба используются для декуантизинг значений *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="34338-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="34338-134">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-135">Необязательный тензорные, содержащий данные нулевой точки *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="34338-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="34338-136">Ожидаемые размеры элемента `BZeroPointTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация.</span><span class="sxs-lookup"><span data-stu-id="34338-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="34338-137">Эти значения нулевых точек используются для декуантизинг значений *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="34338-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="34338-138">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-139">Объект тензорные, содержащий данные шкалы фильтра.</span><span class="sxs-lookup"><span data-stu-id="34338-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="34338-140">Ожидаемые размеры элемента `OutputScaleTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, M, 1 }` Если требуется дискретизация строки.</span><span class="sxs-lookup"><span data-stu-id="34338-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="34338-141">Это значение шкалы используется для декуантизинг значений фильтра.</span><span class="sxs-lookup"><span data-stu-id="34338-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="34338-142">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-143">Необязательный тензорные, содержащий данные нулевой точки фильтра.</span><span class="sxs-lookup"><span data-stu-id="34338-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="34338-144">Ожидаемые размеры объекта `OutputZeroPointTensor` — `{ 1, 1, 1, 1 }` Если для каждого тензорные дискретизация требуется или `{ 1, 1, M, 1 }` Если требуется дискретизация строки.</span><span class="sxs-lookup"><span data-stu-id="34338-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="34338-145">Это значение нулевой точки используется для декуантизинг значений фильтра.</span><span class="sxs-lookup"><span data-stu-id="34338-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="34338-146">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34338-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34338-147">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="34338-147">A tensor to write the results to.</span></span> <span data-ttu-id="34338-148">Это тензорные измерения `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="34338-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="34338-149">Доступность</span><span class="sxs-lookup"><span data-stu-id="34338-149">Availability</span></span>
<span data-ttu-id="34338-150">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="34338-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="34338-151">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="34338-151">Tensor constraints</span></span>
* <span data-ttu-id="34338-152">*Атенсор* и `AZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="34338-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="34338-153">*Бтенсор* и `BZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="34338-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="34338-154">*Аутпуттенсор* и `OutputZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="34338-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="34338-155">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="34338-155">Tensor support</span></span>
| <span data-ttu-id="34338-156">Тензорные</span><span class="sxs-lookup"><span data-stu-id="34338-156">Tensor</span></span> | <span data-ttu-id="34338-157">Вид</span><span class="sxs-lookup"><span data-stu-id="34338-157">Kind</span></span> | <span data-ttu-id="34338-158">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="34338-158">Supported dimension counts</span></span> | <span data-ttu-id="34338-159">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="34338-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="34338-160">атенсор</span><span class="sxs-lookup"><span data-stu-id="34338-160">ATensor</span></span> | <span data-ttu-id="34338-161">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34338-161">Input</span></span> | <span data-ttu-id="34338-162">4</span><span class="sxs-lookup"><span data-stu-id="34338-162">4</span></span> | <span data-ttu-id="34338-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-163">INT8, UINT8</span></span> |
| <span data-ttu-id="34338-164">аскалетенсор</span><span class="sxs-lookup"><span data-stu-id="34338-164">AScaleTensor</span></span> | <span data-ttu-id="34338-165">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34338-165">Input</span></span> | <span data-ttu-id="34338-166">4</span><span class="sxs-lookup"><span data-stu-id="34338-166">4</span></span> | <span data-ttu-id="34338-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="34338-167">FLOAT32</span></span> |
| <span data-ttu-id="34338-168">азеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="34338-168">AZeroPointTensor</span></span> | <span data-ttu-id="34338-169">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="34338-169">Optional input</span></span> | <span data-ttu-id="34338-170">4</span><span class="sxs-lookup"><span data-stu-id="34338-170">4</span></span> | <span data-ttu-id="34338-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-171">INT8, UINT8</span></span> |
| <span data-ttu-id="34338-172">бтенсор</span><span class="sxs-lookup"><span data-stu-id="34338-172">BTensor</span></span> | <span data-ttu-id="34338-173">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34338-173">Input</span></span> | <span data-ttu-id="34338-174">4</span><span class="sxs-lookup"><span data-stu-id="34338-174">4</span></span> | <span data-ttu-id="34338-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-175">INT8, UINT8</span></span> |
| <span data-ttu-id="34338-176">бскалетенсор</span><span class="sxs-lookup"><span data-stu-id="34338-176">BScaleTensor</span></span> | <span data-ttu-id="34338-177">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34338-177">Input</span></span> | <span data-ttu-id="34338-178">4</span><span class="sxs-lookup"><span data-stu-id="34338-178">4</span></span> | <span data-ttu-id="34338-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="34338-179">FLOAT32</span></span> |
| <span data-ttu-id="34338-180">бзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="34338-180">BZeroPointTensor</span></span> | <span data-ttu-id="34338-181">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="34338-181">Optional input</span></span> | <span data-ttu-id="34338-182">4</span><span class="sxs-lookup"><span data-stu-id="34338-182">4</span></span> | <span data-ttu-id="34338-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-183">INT8, UINT8</span></span> |
| <span data-ttu-id="34338-184">аутпутскалетенсор</span><span class="sxs-lookup"><span data-stu-id="34338-184">OutputScaleTensor</span></span> | <span data-ttu-id="34338-185">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34338-185">Input</span></span> | <span data-ttu-id="34338-186">4</span><span class="sxs-lookup"><span data-stu-id="34338-186">4</span></span> | <span data-ttu-id="34338-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="34338-187">FLOAT32</span></span> |
| <span data-ttu-id="34338-188">аутпутзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="34338-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="34338-189">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="34338-189">Optional input</span></span> | <span data-ttu-id="34338-190">4</span><span class="sxs-lookup"><span data-stu-id="34338-190">4</span></span> | <span data-ttu-id="34338-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-191">INT8, UINT8</span></span> |
| <span data-ttu-id="34338-192">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="34338-192">OutputTensor</span></span> | <span data-ttu-id="34338-193">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="34338-193">Output</span></span> | <span data-ttu-id="34338-194">4</span><span class="sxs-lookup"><span data-stu-id="34338-194">4</span></span> | <span data-ttu-id="34338-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="34338-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="34338-196">Требования</span><span class="sxs-lookup"><span data-stu-id="34338-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="34338-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="34338-197">**Header**</span></span> | <span data-ttu-id="34338-198">директмл. h</span><span class="sxs-lookup"><span data-stu-id="34338-198">directml.h</span></span> |