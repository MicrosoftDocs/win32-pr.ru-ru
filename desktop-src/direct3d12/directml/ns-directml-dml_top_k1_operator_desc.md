---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Выбирает из каждой последовательности элементы с максимальным или наименьшим числом элементов на *оси инпуттенсор* и возвращает значения и индексы *этих элементов в* *аутпутвалуетенсор* и *аутпутиндекстенсор* соответственно.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
f1_keywords:
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719961"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="93f49-103">Структура DML_TOP_K1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="93f49-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="93f49-104">Выбирает из каждой последовательности элементы с максимальным или наименьшим числом элементов на *оси инпуттенсор* и возвращает значения и индексы *этих элементов в* *аутпутвалуетенсор* и *аутпутиндекстенсор* соответственно.</span><span class="sxs-lookup"><span data-stu-id="93f49-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="93f49-105">*Последовательность* ссылается на один из наборов элементов, которые существуют вдоль измерения *оси* *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="93f49-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="93f49-106">Выбор из большего числа элементов K или наименьших элементов K можно контролировать с помощью *аксисдиректион*.</span><span class="sxs-lookup"><span data-stu-id="93f49-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93f49-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="93f49-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="93f49-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="93f49-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93f49-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93f49-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```



## <a name="members"></a><span data-ttu-id="93f49-110">Члены</span><span class="sxs-lookup"><span data-stu-id="93f49-110">Members</span></span>

`InputTensor`

<span data-ttu-id="93f49-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="93f49-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="93f49-112">Входной тензорные, содержащий элементы для выбора.</span><span class="sxs-lookup"><span data-stu-id="93f49-112">The input tensor containing elements to select.</span></span>


`OutputValueTensor`

<span data-ttu-id="93f49-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="93f49-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="93f49-114">Выходной тензорные для записи значений верхних элементов *K* в.</span><span class="sxs-lookup"><span data-stu-id="93f49-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="93f49-115">Верхние элементы *K* выбираются в зависимости от того, являются ли они наибольшими или наименьшими, в зависимости от значения *аксисдиректион*.</span><span class="sxs-lookup"><span data-stu-id="93f49-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="93f49-116">Размер этого тензорные должен равняться *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* , который должен иметь значение, равное *K*.</span><span class="sxs-lookup"><span data-stu-id="93f49-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="93f49-117">Значения *K* , выбранные для каждой входной последовательности, гарантированно сортируются по убыванию (от большего к меньшему), если *аксисдиректион* [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="93f49-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="93f49-118">В противном случае обратное значение равно true, а выбранные значения гарантированно сортируются по возрастанию (от наименьшего к большему).</span><span class="sxs-lookup"><span data-stu-id="93f49-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>


`OutputIndexTensor`

<span data-ttu-id="93f49-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="93f49-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="93f49-120">Выходной тензорные для записи индексов верхних элементов *K* в.</span><span class="sxs-lookup"><span data-stu-id="93f49-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="93f49-121">Размер этого тензорные должен равняться *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* , который должен иметь значение, равное *K*.</span><span class="sxs-lookup"><span data-stu-id="93f49-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="93f49-122">Индексы, возвращаемые в этом тензорные, измеряются относительно начала последовательности (в отличие от начала тензорные).</span><span class="sxs-lookup"><span data-stu-id="93f49-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="93f49-123">Например, индекс 0 всегда ссылается на первый элемент для всех последовательностей на оси.</span><span class="sxs-lookup"><span data-stu-id="93f49-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="93f49-124">В случаях, когда два или более элемента в верхнем-K имеют одинаковое значение (т. е. при наличии связи), индексы обоих элементов включаются и гарантированно упорядочиваются по возрастанию индекса элементов.</span><span class="sxs-lookup"><span data-stu-id="93f49-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="93f49-125">Обратите внимание, что это справедливо независимо от значения *аксисдиректион*.</span><span class="sxs-lookup"><span data-stu-id="93f49-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>


`Axis`

<span data-ttu-id="93f49-126">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="93f49-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="93f49-127">Индекс измерения, по которому должны быть выбраны элементы.</span><span class="sxs-lookup"><span data-stu-id="93f49-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="93f49-128">Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="93f49-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`K`

<span data-ttu-id="93f49-129">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="93f49-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="93f49-130">Число выбираемых элементов.</span><span class="sxs-lookup"><span data-stu-id="93f49-130">The number of elements to select.</span></span> <span data-ttu-id="93f49-131">Значение *K* должно быть больше 0, но меньше числа элементов в *инпуттенсор* вдоль измерения, заданного *осью*.</span><span class="sxs-lookup"><span data-stu-id="93f49-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>


`AxisDirection`

<span data-ttu-id="93f49-132">Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="93f49-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="93f49-133">Значение из перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="93f49-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="93f49-134">Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то этот оператор возвращает *наименьшие* элементы *K* в порядке возрастания значения.</span><span class="sxs-lookup"><span data-stu-id="93f49-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="93f49-135">В противном случае он возвращает *самые большие* элементы *K* в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="93f49-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="93f49-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="93f49-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="93f49-137">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93f49-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="93f49-138">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="93f49-138">Example 2.</span></span> <span data-ttu-id="93f49-139">Использование другой оси</span><span class="sxs-lookup"><span data-stu-id="93f49-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="93f49-140">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="93f49-140">Example 3.</span></span> <span data-ttu-id="93f49-141">Связанные значения</span><span class="sxs-lookup"><span data-stu-id="93f49-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="93f49-142">Пример 4.</span><span class="sxs-lookup"><span data-stu-id="93f49-142">Example 4.</span></span> <span data-ttu-id="93f49-143">Увеличение направления оси</span><span class="sxs-lookup"><span data-stu-id="93f49-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="93f49-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93f49-144">Remarks</span></span>
<span data-ttu-id="93f49-145">Если *аксисдиректион* имеет значение [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), этот оператор эквивалентен [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="93f49-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="93f49-146">Доступность</span><span class="sxs-lookup"><span data-stu-id="93f49-146">Availability</span></span>
<span data-ttu-id="93f49-147">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="93f49-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="93f49-148">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="93f49-148">Tensor constraints</span></span>
* <span data-ttu-id="93f49-149">*Инпуттенсор* и *аутпутвалуетенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="93f49-149">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="93f49-150">*Аутпутиндекстенсор* и *аутпутвалуетенсор* должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="93f49-150">*OutputIndexTensor* and *OutputValueTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="93f49-151">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="93f49-151">Tensor support</span></span>
| <span data-ttu-id="93f49-152">Тензорные</span><span class="sxs-lookup"><span data-stu-id="93f49-152">Tensor</span></span> | <span data-ttu-id="93f49-153">Вид</span><span class="sxs-lookup"><span data-stu-id="93f49-153">Kind</span></span> | <span data-ttu-id="93f49-154">Измерения</span><span class="sxs-lookup"><span data-stu-id="93f49-154">Dimensions</span></span> | <span data-ttu-id="93f49-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="93f49-155">Supported dimension counts</span></span> | <span data-ttu-id="93f49-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="93f49-156">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="93f49-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="93f49-157">InputTensor</span></span> | <span data-ttu-id="93f49-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="93f49-158">Input</span></span> | <span data-ttu-id="93f49-159">{ In0, In1, In2, In3 }</span><span class="sxs-lookup"><span data-stu-id="93f49-159">{ In0, In1, In2, In3 }</span></span> | <span data-ttu-id="93f49-160">4</span><span class="sxs-lookup"><span data-stu-id="93f49-160">4</span></span> | <span data-ttu-id="93f49-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="93f49-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="93f49-162">аутпутвалуетенсор</span><span class="sxs-lookup"><span data-stu-id="93f49-162">OutputValueTensor</span></span> | <span data-ttu-id="93f49-163">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="93f49-163">Output</span></span> | <span data-ttu-id="93f49-164">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="93f49-164">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="93f49-165">4</span><span class="sxs-lookup"><span data-stu-id="93f49-165">4</span></span> | <span data-ttu-id="93f49-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="93f49-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="93f49-167">аутпутиндекстенсор</span><span class="sxs-lookup"><span data-stu-id="93f49-167">OutputIndexTensor</span></span> | <span data-ttu-id="93f49-168">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="93f49-168">Output</span></span> | <span data-ttu-id="93f49-169">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="93f49-169">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="93f49-170">4</span><span class="sxs-lookup"><span data-stu-id="93f49-170">4</span></span> | <span data-ttu-id="93f49-171">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="93f49-171">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="93f49-172">Требования</span><span class="sxs-lookup"><span data-stu-id="93f49-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="93f49-173">**Header**</span><span class="sxs-lookup"><span data-stu-id="93f49-173">**Header**</span></span> | <span data-ttu-id="93f49-174">директмл. h</span><span class="sxs-lookup"><span data-stu-id="93f49-174">directml.h</span></span> |