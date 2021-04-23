---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Выполняет функцию умножения матриц для целочисленных данных.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802834"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="207b9-103">Структура DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="207b9-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="207b9-104">Выполняет функцию умножения матриц для целочисленных данных.</span><span class="sxs-lookup"><span data-stu-id="207b9-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="207b9-105">Этот оператор требует, чтобы матрица ввода данных с десятков входов в значение 4D, отформатированная как `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="207b9-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="207b9-106">Оператор умножения матрицы выполняет Батчкаунт \* Чаннелкаунт число независимых матричных матриц.</span><span class="sxs-lookup"><span data-stu-id="207b9-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="207b9-107">Например, если *атенсор* имеет *размеры* `{ BatchCount, ChannelCount, M, K }` , а *бтенсор* имеет размеры,  `{ BatchCount, ChannelCount, K, N }` а *аутпуттенсор* имеет *размеры* , `{ BatchCount, ChannelCount, M, N }` то оператор умножения матрицы будет выполнять батчкаунт \* чаннелкаунт независимых матричных умножений измерений {m, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="207b9-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="207b9-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="207b9-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="207b9-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="207b9-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="207b9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="207b9-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="207b9-111">Члены</span><span class="sxs-lookup"><span data-stu-id="207b9-111">Members</span></span>

`ATensor`

<span data-ttu-id="207b9-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="207b9-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="207b9-113">Объект тензорные, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="207b9-113">A tensor containing the A data.</span></span> <span data-ttu-id="207b9-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="207b9-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="207b9-115">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="207b9-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="207b9-116">Необязательный тензорные, содержащий данные нулевой точки Атенсор.</span><span class="sxs-lookup"><span data-stu-id="207b9-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="207b9-117">Ожидаемые размеры объекта `AZeroPointTensor` : `{ 1, 1, 1, 1 }` Если для каждого тензорные дискретизация требуется или `{ 1, 1, M, 1 }` Если требуется дискретизация для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="207b9-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="207b9-118">Эти значения нулевых точек используются для декуантизинг значений *атенсор* .</span><span class="sxs-lookup"><span data-stu-id="207b9-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="207b9-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="207b9-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="207b9-120">Объект тензорные, содержащий данные B.</span><span class="sxs-lookup"><span data-stu-id="207b9-120">A tensor containing the B data.</span></span> <span data-ttu-id="207b9-121">Размеры тензорные должны быть `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="207b9-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="207b9-122">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="207b9-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="207b9-123">Необязательный тензорные, содержащий данные нулевой точки *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="207b9-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="207b9-124">Ожидаемые размеры элемента `BZeroPointTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация.</span><span class="sxs-lookup"><span data-stu-id="207b9-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="207b9-125">Эти значения нулевых точек используются для декуантизинг значений Бтенсор.</span><span class="sxs-lookup"><span data-stu-id="207b9-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="207b9-126">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="207b9-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="207b9-127">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="207b9-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="207b9-128">Это тензорные измерения `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="207b9-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="207b9-129">Доступность</span><span class="sxs-lookup"><span data-stu-id="207b9-129">Availability</span></span>
<span data-ttu-id="207b9-130">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="207b9-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="207b9-131">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="207b9-131">Tensor constraints</span></span>
* <span data-ttu-id="207b9-132">*Атенсор* и `AZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="207b9-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="207b9-133">*Бтенсор* и `BZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="207b9-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="207b9-134">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="207b9-134">Tensor support</span></span>
| <span data-ttu-id="207b9-135">Тензорные</span><span class="sxs-lookup"><span data-stu-id="207b9-135">Tensor</span></span> | <span data-ttu-id="207b9-136">Вид</span><span class="sxs-lookup"><span data-stu-id="207b9-136">Kind</span></span> | <span data-ttu-id="207b9-137">Измерения</span><span class="sxs-lookup"><span data-stu-id="207b9-137">Dimensions</span></span> | <span data-ttu-id="207b9-138">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="207b9-138">Supported dimension counts</span></span> | <span data-ttu-id="207b9-139">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="207b9-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="207b9-140">атенсор</span><span class="sxs-lookup"><span data-stu-id="207b9-140">ATensor</span></span> | <span data-ttu-id="207b9-141">Входные данные</span><span class="sxs-lookup"><span data-stu-id="207b9-141">Input</span></span> | <span data-ttu-id="207b9-142">{Батчкаунт, Чаннелкаунт, M, K}</span><span class="sxs-lookup"><span data-stu-id="207b9-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="207b9-143">4</span><span class="sxs-lookup"><span data-stu-id="207b9-143">4</span></span> | <span data-ttu-id="207b9-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="207b9-144">INT8, UINT8</span></span> |
| <span data-ttu-id="207b9-145">азеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="207b9-145">AZeroPointTensor</span></span> | <span data-ttu-id="207b9-146">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="207b9-146">Optional input</span></span> | <span data-ttu-id="207b9-147">{1, 1, Азеропоинткаунт, 1}</span><span class="sxs-lookup"><span data-stu-id="207b9-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="207b9-148">4</span><span class="sxs-lookup"><span data-stu-id="207b9-148">4</span></span> | <span data-ttu-id="207b9-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="207b9-149">INT8, UINT8</span></span> |
| <span data-ttu-id="207b9-150">бтенсор</span><span class="sxs-lookup"><span data-stu-id="207b9-150">BTensor</span></span> | <span data-ttu-id="207b9-151">Входные данные</span><span class="sxs-lookup"><span data-stu-id="207b9-151">Input</span></span> | <span data-ttu-id="207b9-152">{Батчкаунт, Чаннелкаунт, K, N}</span><span class="sxs-lookup"><span data-stu-id="207b9-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="207b9-153">4</span><span class="sxs-lookup"><span data-stu-id="207b9-153">4</span></span> | <span data-ttu-id="207b9-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="207b9-154">INT8, UINT8</span></span> |
| <span data-ttu-id="207b9-155">бзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="207b9-155">BZeroPointTensor</span></span> | <span data-ttu-id="207b9-156">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="207b9-156">Optional input</span></span> | <span data-ttu-id="207b9-157">{1, 1, 1, Бзеропоинткаунт}</span><span class="sxs-lookup"><span data-stu-id="207b9-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="207b9-158">4</span><span class="sxs-lookup"><span data-stu-id="207b9-158">4</span></span> | <span data-ttu-id="207b9-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="207b9-159">INT8, UINT8</span></span> |
| <span data-ttu-id="207b9-160">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="207b9-160">OutputTensor</span></span> | <span data-ttu-id="207b9-161">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="207b9-161">Output</span></span> | <span data-ttu-id="207b9-162">{Батчкаунт, Чаннелкаунт, M, N}</span><span class="sxs-lookup"><span data-stu-id="207b9-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="207b9-163">4</span><span class="sxs-lookup"><span data-stu-id="207b9-163">4</span></span> | <span data-ttu-id="207b9-164">INT32</span><span class="sxs-lookup"><span data-stu-id="207b9-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="207b9-165">Требования</span><span class="sxs-lookup"><span data-stu-id="207b9-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="207b9-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="207b9-166">**Header**</span></span> | <span data-ttu-id="207b9-167">директмл. h</span><span class="sxs-lookup"><span data-stu-id="207b9-167">directml.h</span></span> |