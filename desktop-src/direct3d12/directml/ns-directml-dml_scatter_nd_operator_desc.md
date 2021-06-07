---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Копирует весь входной тензорные в выходные данные, а затем перезаписывает выбранные индексы соответствующими значениями из тензорные обновлений.
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418004"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="65d05-103">Структура DML_SCATTER_ND_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="65d05-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="65d05-104">Копирует весь входной тензорные в выходные данные, а затем перезаписывает выбранные индексы соответствующими значениями из тензорные обновлений.</span><span class="sxs-lookup"><span data-stu-id="65d05-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="65d05-105">Этот оператор выполняет следующий псевдокод, где "..." представляет ряд координат с точным поведением, определяемым осью и размером индексов.</span><span class="sxs-lookup"><span data-stu-id="65d05-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="65d05-106">Если два индекса элементов вывода перекрываются (что недопустимо), последняя запись WINS не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="65d05-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65d05-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="65d05-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="65d05-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="65d05-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="65d05-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65d05-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="65d05-110">Участники</span><span class="sxs-lookup"><span data-stu-id="65d05-110">Members</span></span>

`InputTensor`

<span data-ttu-id="65d05-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="65d05-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="65d05-112">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="65d05-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="65d05-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="65d05-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="65d05-114">Объект тензорные, содержащий индексы.</span><span class="sxs-lookup"><span data-stu-id="65d05-114">A tensor containing the indices.</span></span> <span data-ttu-id="65d05-115">*DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="65d05-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="65d05-116">Последнее измерение *индицестенсор* на самом деле является числом координат на кортеж индекса, и не должны превышает *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="65d05-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="65d05-117">Например, индексы тензорные размера `{1,4,5,2}` с *индицесдименсионкаунт* = 3 означает 4x5 массив кортежей координат из двух значений, которые индексируются в *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="65d05-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="65d05-118">Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные.</span><span class="sxs-lookup"><span data-stu-id="65d05-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="65d05-119">Отрицательные индексы обрабатываются относительно конца соответствующего измерения.</span><span class="sxs-lookup"><span data-stu-id="65d05-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="65d05-120">Например, индекс-1 ссылается на последний элемент в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="65d05-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="65d05-121">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="65d05-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="65d05-122">Объект тензорные, содержащий новые значения для замены существующих входных значений по соответствующим индексам.</span><span class="sxs-lookup"><span data-stu-id="65d05-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="65d05-123">*DimensionCount* этого тензорные должен соответствовать *инпуттенсор. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="65d05-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="65d05-124">Ожидаемый *упдатестенсор. sizes* является объединением *индицестенсор. размеры* ведущих сегментов и *инпуттенсор. sizes* в конце сегмента, чтобы получить следующий результат.</span><span class="sxs-lookup"><span data-stu-id="65d05-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="65d05-125">Размеры вычисляются по правому краю, при этом в начале каждого из них в начале *упдатестенсор. DimensionCount* помещаются начальные значения 1.</span><span class="sxs-lookup"><span data-stu-id="65d05-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="65d05-126">Рассмотрим пример.</span><span class="sxs-lookup"><span data-stu-id="65d05-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="65d05-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="65d05-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="65d05-128">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="65d05-128">The tensor to write the results to.</span></span> <span data-ttu-id="65d05-129">*Размеры* и *тип данных* этого тензорные должны соответствовать *инпуттенсор. sizes*.</span><span class="sxs-lookup"><span data-stu-id="65d05-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="65d05-130">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="65d05-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="65d05-131">Число фактических входных измерений в *инпуттенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *инпуттенсор. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="65d05-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="65d05-132">Например, для заданных *инпуттенсор. sizes* = {1,1,4,6} и *инпутдименсионкаунт* = 3 фактически значимые индексы имеют значение {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="65d05-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="65d05-133">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="65d05-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="65d05-134">Количество фактических измерений индекса в *индицестенсор* после пропуска любых несущественных начальных значений, в диапазоне [1, *индицестенсор. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="65d05-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="65d05-135">Например, для заданных *индицестенсор. sizes* = {1,1,4,6} и *индицесдименсионкаунт* = 3 фактически значимые индексы имеют значение {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="65d05-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="65d05-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="65d05-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="65d05-137">Доступность</span><span class="sxs-lookup"><span data-stu-id="65d05-137">Availability</span></span>
<span data-ttu-id="65d05-138">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="65d05-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="65d05-139">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="65d05-139">Tensor constraints</span></span>
* <span data-ttu-id="65d05-140">*Индицестенсор*, *инпуттенсор*, *Аутпуттенсор* и `UpdatesTensor` должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="65d05-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="65d05-141">*Инпуттенсор*, *аутпуттенсор* и `UpdatesTensor` должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="65d05-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="65d05-142">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="65d05-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="65d05-143">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="65d05-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="65d05-144">Тензорные</span><span class="sxs-lookup"><span data-stu-id="65d05-144">Tensor</span></span> | <span data-ttu-id="65d05-145">Вид</span><span class="sxs-lookup"><span data-stu-id="65d05-145">Kind</span></span> | <span data-ttu-id="65d05-146">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="65d05-146">Supported dimension counts</span></span> | <span data-ttu-id="65d05-147">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="65d05-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="65d05-148">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-148">InputTensor</span></span> | <span data-ttu-id="65d05-149">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-149">Input</span></span> | <span data-ttu-id="65d05-150">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="65d05-150">1 to 8</span></span> | <span data-ttu-id="65d05-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="65d05-152">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-152">IndicesTensor</span></span> | <span data-ttu-id="65d05-153">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-153">Input</span></span> | <span data-ttu-id="65d05-154">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="65d05-154">1 to 8</span></span> | <span data-ttu-id="65d05-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="65d05-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="65d05-156">упдатестенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-156">UpdatesTensor</span></span> | <span data-ttu-id="65d05-157">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-157">Input</span></span> | <span data-ttu-id="65d05-158">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="65d05-158">1 to 8</span></span> | <span data-ttu-id="65d05-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="65d05-160">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-160">OutputTensor</span></span> | <span data-ttu-id="65d05-161">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-161">Output</span></span> | <span data-ttu-id="65d05-162">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="65d05-162">1 to 8</span></span> | <span data-ttu-id="65d05-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="65d05-164">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="65d05-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="65d05-165">Тензорные</span><span class="sxs-lookup"><span data-stu-id="65d05-165">Tensor</span></span> | <span data-ttu-id="65d05-166">Вид</span><span class="sxs-lookup"><span data-stu-id="65d05-166">Kind</span></span> | <span data-ttu-id="65d05-167">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="65d05-167">Supported dimension counts</span></span> | <span data-ttu-id="65d05-168">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="65d05-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="65d05-169">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-169">InputTensor</span></span> | <span data-ttu-id="65d05-170">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-170">Input</span></span> | <span data-ttu-id="65d05-171">4</span><span class="sxs-lookup"><span data-stu-id="65d05-171">4</span></span> | <span data-ttu-id="65d05-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="65d05-173">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-173">IndicesTensor</span></span> | <span data-ttu-id="65d05-174">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-174">Input</span></span> | <span data-ttu-id="65d05-175">4</span><span class="sxs-lookup"><span data-stu-id="65d05-175">4</span></span> | <span data-ttu-id="65d05-176">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="65d05-176">UINT32</span></span> |
| <span data-ttu-id="65d05-177">упдатестенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-177">UpdatesTensor</span></span> | <span data-ttu-id="65d05-178">Входные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-178">Input</span></span> | <span data-ttu-id="65d05-179">4</span><span class="sxs-lookup"><span data-stu-id="65d05-179">4</span></span> | <span data-ttu-id="65d05-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="65d05-181">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="65d05-181">OutputTensor</span></span> | <span data-ttu-id="65d05-182">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="65d05-182">Output</span></span> | <span data-ttu-id="65d05-183">4</span><span class="sxs-lookup"><span data-stu-id="65d05-183">4</span></span> | <span data-ttu-id="65d05-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="65d05-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="65d05-185">Требования</span><span class="sxs-lookup"><span data-stu-id="65d05-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="65d05-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="65d05-186">**Header**</span></span> | <span data-ttu-id="65d05-187">директмл. h</span><span class="sxs-lookup"><span data-stu-id="65d05-187">directml.h</span></span> |