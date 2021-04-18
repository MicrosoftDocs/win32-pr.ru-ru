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
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719939"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="d78f2-103">Структура DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="d78f2-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="d78f2-104">Выполняет функцию умножения матриц для целочисленных данных.</span><span class="sxs-lookup"><span data-stu-id="d78f2-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="d78f2-105">Этот оператор требует, чтобы матрица ввода данных с десятков входов в значение 4D, отформатированная как `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="d78f2-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="d78f2-106">Оператор умножения матрицы выполняет Батчкаунт \* Чаннелкаунт число независимых матричных матриц.</span><span class="sxs-lookup"><span data-stu-id="d78f2-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="d78f2-107">Например, если *атенсор* имеет *размеры* `{ BatchCount, ChannelCount, M, K }` , а *бтенсор* имеет размеры,  `{ BatchCount, ChannelCount, K, N }` а *аутпуттенсор* имеет *размеры* , `{ BatchCount, ChannelCount, M, N }` то оператор умножения матрицы будет выполнять батчкаунт \* чаннелкаунт независимых матричных умножений измерений {m, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="d78f2-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d78f2-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="d78f2-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d78f2-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d78f2-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d78f2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d78f2-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="d78f2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d78f2-111">Members</span></span>

`ATensor`

<span data-ttu-id="d78f2-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d78f2-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d78f2-113">Объект тензорные, содержащий данные.</span><span class="sxs-lookup"><span data-stu-id="d78f2-113">A tensor containing the A data.</span></span> <span data-ttu-id="d78f2-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="d78f2-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="d78f2-115">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d78f2-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d78f2-116">Необязательный тензорные, содержащий данные нулевой точки Атенсор.</span><span class="sxs-lookup"><span data-stu-id="d78f2-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="d78f2-117">Ожидаемые размеры объекта `AZeroPointTensor` : `{ 1, 1, 1, 1 }` Если для каждого тензорные дискретизация требуется или `{ 1, 1, M, 1 }` Если требуется дискретизация для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="d78f2-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="d78f2-118">Эти значения нулевых точек используются для декуантизинг значений *атенсор* .</span><span class="sxs-lookup"><span data-stu-id="d78f2-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="d78f2-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d78f2-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d78f2-120">Объект тензорные, содержащий данные B.</span><span class="sxs-lookup"><span data-stu-id="d78f2-120">A tensor containing the B data.</span></span> <span data-ttu-id="d78f2-121">Размеры тензорные должны быть `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="d78f2-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="d78f2-122">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d78f2-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d78f2-123">Необязательный тензорные, содержащий данные нулевой точки *бтенсор* .</span><span class="sxs-lookup"><span data-stu-id="d78f2-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="d78f2-124">Ожидаемые размеры элемента `BZeroPointTensor` —, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, 1, 1, N }` Если требуется для каждого столбца дискретизация.</span><span class="sxs-lookup"><span data-stu-id="d78f2-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="d78f2-125">Эти значения нулевых точек используются для декуантизинг значений Бтенсор.</span><span class="sxs-lookup"><span data-stu-id="d78f2-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="d78f2-126">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d78f2-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d78f2-127">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="d78f2-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="d78f2-128">Это тензорные измерения `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="d78f2-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="d78f2-129">Доступность</span><span class="sxs-lookup"><span data-stu-id="d78f2-129">Availability</span></span>
<span data-ttu-id="d78f2-130">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d78f2-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d78f2-131">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="d78f2-131">Tensor constraints</span></span>
* <span data-ttu-id="d78f2-132">*Атенсор* и `AZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="d78f2-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="d78f2-133">*Бтенсор* и `BZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="d78f2-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d78f2-134">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="d78f2-134">Tensor support</span></span>
| <span data-ttu-id="d78f2-135">Тензорные</span><span class="sxs-lookup"><span data-stu-id="d78f2-135">Tensor</span></span> | <span data-ttu-id="d78f2-136">Вид</span><span class="sxs-lookup"><span data-stu-id="d78f2-136">Kind</span></span> | <span data-ttu-id="d78f2-137">Измерения</span><span class="sxs-lookup"><span data-stu-id="d78f2-137">Dimensions</span></span> | <span data-ttu-id="d78f2-138">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="d78f2-138">Supported dimension counts</span></span> | <span data-ttu-id="d78f2-139">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="d78f2-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="d78f2-140">атенсор</span><span class="sxs-lookup"><span data-stu-id="d78f2-140">ATensor</span></span> | <span data-ttu-id="d78f2-141">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d78f2-141">Input</span></span> | <span data-ttu-id="d78f2-142">{Батчкаунт, Чаннелкаунт, M, K}</span><span class="sxs-lookup"><span data-stu-id="d78f2-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="d78f2-143">4</span><span class="sxs-lookup"><span data-stu-id="d78f2-143">4</span></span> | <span data-ttu-id="d78f2-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d78f2-144">INT8, UINT8</span></span> |
| <span data-ttu-id="d78f2-145">азеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="d78f2-145">AZeroPointTensor</span></span> | <span data-ttu-id="d78f2-146">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="d78f2-146">Optional input</span></span> | <span data-ttu-id="d78f2-147">{1, 1, Азеропоинткаунт, 1}</span><span class="sxs-lookup"><span data-stu-id="d78f2-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="d78f2-148">4</span><span class="sxs-lookup"><span data-stu-id="d78f2-148">4</span></span> | <span data-ttu-id="d78f2-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d78f2-149">INT8, UINT8</span></span> |
| <span data-ttu-id="d78f2-150">бтенсор</span><span class="sxs-lookup"><span data-stu-id="d78f2-150">BTensor</span></span> | <span data-ttu-id="d78f2-151">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d78f2-151">Input</span></span> | <span data-ttu-id="d78f2-152">{Батчкаунт, Чаннелкаунт, K, N}</span><span class="sxs-lookup"><span data-stu-id="d78f2-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="d78f2-153">4</span><span class="sxs-lookup"><span data-stu-id="d78f2-153">4</span></span> | <span data-ttu-id="d78f2-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d78f2-154">INT8, UINT8</span></span> |
| <span data-ttu-id="d78f2-155">бзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="d78f2-155">BZeroPointTensor</span></span> | <span data-ttu-id="d78f2-156">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="d78f2-156">Optional input</span></span> | <span data-ttu-id="d78f2-157">{1, 1, 1, Бзеропоинткаунт}</span><span class="sxs-lookup"><span data-stu-id="d78f2-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="d78f2-158">4</span><span class="sxs-lookup"><span data-stu-id="d78f2-158">4</span></span> | <span data-ttu-id="d78f2-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d78f2-159">INT8, UINT8</span></span> |
| <span data-ttu-id="d78f2-160">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="d78f2-160">OutputTensor</span></span> | <span data-ttu-id="d78f2-161">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="d78f2-161">Output</span></span> | <span data-ttu-id="d78f2-162">{Батчкаунт, Чаннелкаунт, M, N}</span><span class="sxs-lookup"><span data-stu-id="d78f2-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="d78f2-163">4</span><span class="sxs-lookup"><span data-stu-id="d78f2-163">4</span></span> | <span data-ttu-id="d78f2-164">INT32</span><span class="sxs-lookup"><span data-stu-id="d78f2-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="d78f2-165">Требования</span><span class="sxs-lookup"><span data-stu-id="d78f2-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d78f2-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="d78f2-166">**Header**</span></span> | <span data-ttu-id="d78f2-167">директмл. h</span><span class="sxs-lookup"><span data-stu-id="d78f2-167">directml.h</span></span> |