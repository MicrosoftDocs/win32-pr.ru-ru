---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802897"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="f6614-104">Структура DML_GATHER_ND_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="f6614-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f6614-105">Собирает элементы из входного тензорные, используя индексы тензорные для сопоставления индексов со всеми подблоками входных данных.</span><span class="sxs-lookup"><span data-stu-id="f6614-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="f6614-106">Этот оператор выполняет следующий псевдокод, где "..." представляет ряд координат с точным поведением, зависящим от количества измерений input и Indices.</span><span class="sxs-lookup"><span data-stu-id="f6614-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="f6614-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="f6614-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f6614-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f6614-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6614-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6614-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="f6614-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f6614-110">Members</span></span>

`InputTensor`

<span data-ttu-id="f6614-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f6614-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f6614-112">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="f6614-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="f6614-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f6614-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f6614-114">Тензорные, содержащий индексы.</span><span class="sxs-lookup"><span data-stu-id="f6614-114">The tensor containing the indices.</span></span> <span data-ttu-id="f6614-115">*DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f6614-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f6614-116">Последнее измерение *индицестенсор* на самом деле является числом координат на кортеж индекса и не может превышать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f6614-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f6614-117">Например, индексы тензорные *размеров* `{1,4,5,2}` с *индицесдименсионкаунт* = 3 означает 4x5 массив из 2-координатных кортежей, которые индексируются в *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="f6614-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="f6614-118">Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные.</span><span class="sxs-lookup"><span data-stu-id="f6614-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="f6614-119">Отрицательные индексы обрабатываются относительно конца соответствующего измерения.</span><span class="sxs-lookup"><span data-stu-id="f6614-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="f6614-120">Например, индекс-1 ссылается на последний элемент в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="f6614-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="f6614-121">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f6614-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f6614-122">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="f6614-122">The tensor to write the results to.</span></span> <span data-ttu-id="f6614-123">*DimensionCount* и *DataType* этого тензорные должны соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f6614-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f6614-124">Ожидаемый *аутпуттенсор. sizes* является объединением *индицестенсор. размеры* ведущих сегментов и *инпуттенсор. размеры* сегмента в конце:</span><span class="sxs-lookup"><span data-stu-id="f6614-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="f6614-125">Выходные измерения вычисляются по правому краю, при этом начальные значения 1 добавляются в начало, если это необходимо для *аутпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f6614-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="f6614-126">Пример приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="f6614-126">Here's an example.</span></span>

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

<span data-ttu-id="f6614-127">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f6614-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f6614-128">Число фактических входных измерений в *инпуттенсор* после пропуска любых несущественных начальных значений, в диапазоне от `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="f6614-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="f6614-129">Например, для заданных *инпуттенсор. sizes*  =  `{1,1,4,6}` и `InputDimensionCount` = 3 фактически значимые индексы имеют значение `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="f6614-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="f6614-130">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f6614-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f6614-131">Количество фактических измерений индекса в *индицестенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *индицестенсор. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="f6614-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="f6614-132">Например, для заданных *индицестенсор. sizes*  =  `{1,1,4,6}` и *индицесдименсионкаунт* = 3 фактически значимые индексы имеют значение `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="f6614-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="f6614-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="f6614-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="f6614-134">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="f6614-134">Example 1.</span></span> <span data-ttu-id="f6614-135">повторное сопоставление 1D</span><span class="sxs-lookup"><span data-stu-id="f6614-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="f6614-136">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="f6614-136">Example 2.</span></span> <span data-ttu-id="f6614-137">Преобразование 2D</span><span class="sxs-lookup"><span data-stu-id="f6614-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="f6614-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6614-138">Remarks</span></span>
<span data-ttu-id="f6614-139">Более новая версия этого оператора, `DML_OPERATOR_GATHER_ND1` , была введена в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f6614-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="f6614-140">Доступность</span><span class="sxs-lookup"><span data-stu-id="f6614-140">Availability</span></span>
<span data-ttu-id="f6614-141">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f6614-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f6614-142">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="f6614-142">Tensor constraints</span></span>
* <span data-ttu-id="f6614-143">*Индицестенсор*, *инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f6614-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="f6614-144">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="f6614-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f6614-145">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="f6614-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="f6614-146">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="f6614-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="f6614-147">Тензорные</span><span class="sxs-lookup"><span data-stu-id="f6614-147">Tensor</span></span> | <span data-ttu-id="f6614-148">Вид</span><span class="sxs-lookup"><span data-stu-id="f6614-148">Kind</span></span> | <span data-ttu-id="f6614-149">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="f6614-149">Supported dimension counts</span></span> | <span data-ttu-id="f6614-150">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="f6614-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f6614-151">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-151">InputTensor</span></span> | <span data-ttu-id="f6614-152">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-152">Input</span></span> | <span data-ttu-id="f6614-153">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="f6614-153">1 to 8</span></span> | <span data-ttu-id="f6614-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f6614-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f6614-155">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-155">IndicesTensor</span></span> | <span data-ttu-id="f6614-156">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-156">Input</span></span> | <span data-ttu-id="f6614-157">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="f6614-157">1 to 8</span></span> | <span data-ttu-id="f6614-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="f6614-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="f6614-159">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-159">OutputTensor</span></span> | <span data-ttu-id="f6614-160">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-160">Output</span></span> | <span data-ttu-id="f6614-161">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="f6614-161">1 to 8</span></span> | <span data-ttu-id="f6614-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f6614-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="f6614-163">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="f6614-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="f6614-164">Тензорные</span><span class="sxs-lookup"><span data-stu-id="f6614-164">Tensor</span></span> | <span data-ttu-id="f6614-165">Вид</span><span class="sxs-lookup"><span data-stu-id="f6614-165">Kind</span></span> | <span data-ttu-id="f6614-166">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="f6614-166">Supported dimension counts</span></span> | <span data-ttu-id="f6614-167">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="f6614-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f6614-168">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-168">InputTensor</span></span> | <span data-ttu-id="f6614-169">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-169">Input</span></span> | <span data-ttu-id="f6614-170">4</span><span class="sxs-lookup"><span data-stu-id="f6614-170">4</span></span> | <span data-ttu-id="f6614-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f6614-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f6614-172">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-172">IndicesTensor</span></span> | <span data-ttu-id="f6614-173">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-173">Input</span></span> | <span data-ttu-id="f6614-174">4</span><span class="sxs-lookup"><span data-stu-id="f6614-174">4</span></span> | <span data-ttu-id="f6614-175">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="f6614-175">UINT32</span></span> |
| <span data-ttu-id="f6614-176">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="f6614-176">OutputTensor</span></span> | <span data-ttu-id="f6614-177">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="f6614-177">Output</span></span> | <span data-ttu-id="f6614-178">4</span><span class="sxs-lookup"><span data-stu-id="f6614-178">4</span></span> | <span data-ttu-id="f6614-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f6614-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="f6614-180">Требования</span><span class="sxs-lookup"><span data-stu-id="f6614-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f6614-181">**Header**</span><span class="sxs-lookup"><span data-stu-id="f6614-181">**Header**</span></span> | <span data-ttu-id="f6614-182">директмл. h</span><span class="sxs-lookup"><span data-stu-id="f6614-182">directml.h</span></span> |
