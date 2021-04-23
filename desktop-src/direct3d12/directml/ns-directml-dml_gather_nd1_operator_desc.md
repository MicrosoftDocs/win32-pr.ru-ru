---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802856"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="54042-104">Структура DML_GATHER_ND1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="54042-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="54042-105">Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных.</span><span class="sxs-lookup"><span data-stu-id="54042-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="54042-106">Этот оператор выполняет следующий псевдокод, где "..." представляет ряд координат с точным поведением, зависящим от количества измерений Batch, input и Indices.</span><span class="sxs-lookup"><span data-stu-id="54042-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="54042-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="54042-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="54042-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="54042-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="54042-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54042-109">Syntax</span></span>

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a><span data-ttu-id="54042-110">Члены</span><span class="sxs-lookup"><span data-stu-id="54042-110">Members</span></span>

`InputTensor`

<span data-ttu-id="54042-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="54042-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="54042-112">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="54042-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="54042-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="54042-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="54042-114">Тензорные, содержащий индексы.</span><span class="sxs-lookup"><span data-stu-id="54042-114">The tensor containing the indices.</span></span> <span data-ttu-id="54042-115">*DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="54042-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="54042-116">Последнее измерение *индицестенсор* на самом деле является числом координат на кортеж индекса и не может превышать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="54042-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="54042-117">Например, индексы тензорные *размеров* `{1,4,5,2}` с *индицесдименсионкаунт* = 3 означает 4x5 массив из 2-координатных кортежей, которые индексируются в *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="54042-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="54042-118">Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные.</span><span class="sxs-lookup"><span data-stu-id="54042-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="54042-119">Отрицательные индексы обрабатываются относительно конца соответствующего измерения.</span><span class="sxs-lookup"><span data-stu-id="54042-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="54042-120">Например, индекс-1 ссылается на последний элемент в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="54042-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="54042-121">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="54042-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="54042-122">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="54042-122">The tensor to write the results to.</span></span> <span data-ttu-id="54042-123">*DimensionCount* и *DataType* этого тензорные должны соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="54042-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="54042-124">Ожидаемый *аутпуттенсор. sizes* является объединением *индицестенсор. размеры* ведущих сегментов и *инпуттенсор. sizes* замыкающий сегмент, что приводит к следующему результату.</span><span class="sxs-lookup"><span data-stu-id="54042-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="54042-125">Размеры вычисляются по правому краю, при этом в начале каждого из них в начале *аутпуттенсор. DimensionCount* помещаются начальные значения 1.</span><span class="sxs-lookup"><span data-stu-id="54042-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="54042-126">Пример приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="54042-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

<span data-ttu-id="54042-127">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54042-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="54042-128">Число фактических входных измерений в *инпуттенсор* после пропуска любых несущественных начальных значений, в диапазоне от `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="54042-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="54042-129">Например, для заданных *инпуттенсор. sizes*  =  `{1,1,4,6}` и `InputDimensionCount` = 3 фактически значимые индексы имеют значение `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="54042-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="54042-130">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54042-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="54042-131">Количество фактических измерений индекса в *индицестенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *индицестенсор. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="54042-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="54042-132">Например, для заданных *индицестенсор. sizes*  =  `{1,1,4,6}` и *индицесдименсионкаунт* = 3 фактически значимые индексы имеют значение `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="54042-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="54042-133">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54042-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="54042-134">Количество измерений в каждом тензорные (*инпуттенсор*, *индицестенсор*, *аутпуттенсор*), которые считаются независимыми пакетами, в диапазоне между [0, *инпуттенсор. DimensionCount*) и [0, *индицестенсор. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="54042-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="54042-135">Число пакетов может быть равно 0, что подразумевает наличие одного пакета.</span><span class="sxs-lookup"><span data-stu-id="54042-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="54042-136">Например, для заданных *индицестенсор. sizes*  =  `{1,3,4,5,6,7}` и *индицесдименсионкаунт* = 5 и `BatchDimensionCount` = 2 существуют пакеты `{3,4}` и осмысленные индексы `{5,6,7}` .</span><span class="sxs-lookup"><span data-stu-id="54042-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="54042-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54042-137">Remarks</span></span>
<span data-ttu-id="54042-138">**DML_GATHER_ND1_OPERATOR_DESC** добавляет *батчдименсионкаунт* и эквивалентен [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) , если *батчдименсионкаунт* = 0.</span><span class="sxs-lookup"><span data-stu-id="54042-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="54042-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="54042-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="54042-140">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="54042-140">Example 1.</span></span> <span data-ttu-id="54042-141">повторное сопоставление 1D</span><span class="sxs-lookup"><span data-stu-id="54042-141">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="54042-142">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="54042-142">Example 2.</span></span> <span data-ttu-id="54042-143">Преобразование 2D с помощью счетчика пакетов</span><span class="sxs-lookup"><span data-stu-id="54042-143">2D remapping with batch count</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a><span data-ttu-id="54042-144">Доступность</span><span class="sxs-lookup"><span data-stu-id="54042-144">Availability</span></span>
<span data-ttu-id="54042-145">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="54042-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="54042-146">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="54042-146">Tensor constraints</span></span>
* <span data-ttu-id="54042-147">*Индицестенсор*, *инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="54042-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="54042-148">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="54042-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="54042-149">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="54042-149">Tensor support</span></span>
| <span data-ttu-id="54042-150">Тензорные</span><span class="sxs-lookup"><span data-stu-id="54042-150">Tensor</span></span> | <span data-ttu-id="54042-151">Вид</span><span class="sxs-lookup"><span data-stu-id="54042-151">Kind</span></span> | <span data-ttu-id="54042-152">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="54042-152">Supported dimension counts</span></span> | <span data-ttu-id="54042-153">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="54042-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="54042-154">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="54042-154">InputTensor</span></span> | <span data-ttu-id="54042-155">Входные данные</span><span class="sxs-lookup"><span data-stu-id="54042-155">Input</span></span> | <span data-ttu-id="54042-156">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="54042-156">1 to 8</span></span> | <span data-ttu-id="54042-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="54042-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="54042-158">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="54042-158">IndicesTensor</span></span> | <span data-ttu-id="54042-159">Входные данные</span><span class="sxs-lookup"><span data-stu-id="54042-159">Input</span></span> | <span data-ttu-id="54042-160">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="54042-160">1 to 8</span></span> | <span data-ttu-id="54042-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="54042-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="54042-162">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="54042-162">OutputTensor</span></span> | <span data-ttu-id="54042-163">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="54042-163">Output</span></span> | <span data-ttu-id="54042-164">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="54042-164">1 to 8</span></span> | <span data-ttu-id="54042-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="54042-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="54042-166">Требования</span><span class="sxs-lookup"><span data-stu-id="54042-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="54042-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="54042-167">**Header**</span></span> | <span data-ttu-id="54042-168">директмл. h</span><span class="sxs-lookup"><span data-stu-id="54042-168">directml.h</span></span> |
