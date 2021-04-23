---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803346"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="bbfc1-103">Структура DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bbfc1-104">Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbfc1-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="bbfc1-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bbfc1-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bbfc1-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbfc1-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="bbfc1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bbfc1-108">Members</span></span>

`InputTensor`

<span data-ttu-id="bbfc1-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bbfc1-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bbfc1-110">Входной тензорные, содержащий элементы для суммирования.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="bbfc1-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bbfc1-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bbfc1-112">Выходной тензорные для записи итоговых суммарных сумм в.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="bbfc1-113">Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="bbfc1-114">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bbfc1-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bbfc1-115">Индекс измерения для суммирования элементов.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="bbfc1-116">Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="bbfc1-117">Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="bbfc1-118">Одно из значений перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="bbfc1-119">Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то суммирование выполняется путем просмотра тензорные вдоль указанной оси по возрастанию индекса элементов.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="bbfc1-120">Если задано значение **DML_AXIS_DIRECTION_DECREASING**, обратное значение равно true, а суммирование выполняется путем обхода элементов по убыванию индекса.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="bbfc1-121">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="bbfc1-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="bbfc1-122">Если значение — **true**, значение текущего элемента исключается при записи выполняемого счетчика в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="bbfc1-123">При значении **false** значение текущего элемента включается в счетчик выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="bbfc1-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="bbfc1-124">Examples</span></span>

<span data-ttu-id="bbfc1-125">В примерах в этом разделе используется входной тензорные со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="bbfc1-126">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-126">Example 1.</span></span> <span data-ttu-id="bbfc1-127">Совокупная сумма по горизонтали сливерс</span><span class="sxs-lookup"><span data-stu-id="bbfc1-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="bbfc1-128">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-128">Example 2.</span></span> <span data-ttu-id="bbfc1-129">Эксклюзивные суммы</span><span class="sxs-lookup"><span data-stu-id="bbfc1-129">Exclusive sums</span></span>

<span data-ttu-id="bbfc1-130">Установка параметра *хасексклусивесум* в **значение true** оказывает за исключением значения текущего элемента из счетчика, выполняемого при записи в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="bbfc1-131">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-131">Example 3.</span></span> <span data-ttu-id="bbfc1-132">Направление оси</span><span class="sxs-lookup"><span data-stu-id="bbfc1-132">Axis direction</span></span>

<span data-ttu-id="bbfc1-133">Установка параметра *аксисдиректион* в значение [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) оказывает обратный порядок обхода элементов при вычислении счетчика выполнения.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="bbfc1-134">Пример 4.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-134">Example 4.</span></span> <span data-ttu-id="bbfc1-135">Суммирование по другой оси</span><span class="sxs-lookup"><span data-stu-id="bbfc1-135">Summing along a different axis</span></span>

<span data-ttu-id="bbfc1-136">В этом примере суммирование выполняется вертикально вдоль оси высоты (второе измерение).</span><span class="sxs-lookup"><span data-stu-id="bbfc1-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="bbfc1-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbfc1-137">Remarks</span></span>
<span data-ttu-id="bbfc1-138">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдоним *инпуттенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="bbfc1-139">Доступность</span><span class="sxs-lookup"><span data-stu-id="bbfc1-139">Availability</span></span>
<span data-ttu-id="bbfc1-140">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="bbfc1-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bbfc1-141">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="bbfc1-141">Tensor constraints</span></span>
<span data-ttu-id="bbfc1-142">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="bbfc1-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bbfc1-143">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="bbfc1-143">Tensor support</span></span>
| <span data-ttu-id="bbfc1-144">Тензорные</span><span class="sxs-lookup"><span data-stu-id="bbfc1-144">Tensor</span></span> | <span data-ttu-id="bbfc1-145">Вид</span><span class="sxs-lookup"><span data-stu-id="bbfc1-145">Kind</span></span> | <span data-ttu-id="bbfc1-146">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="bbfc1-146">Supported dimension counts</span></span> | <span data-ttu-id="bbfc1-147">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="bbfc1-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bbfc1-148">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="bbfc1-148">InputTensor</span></span> | <span data-ttu-id="bbfc1-149">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bbfc1-149">Input</span></span> | <span data-ttu-id="bbfc1-150">4</span><span class="sxs-lookup"><span data-stu-id="bbfc1-150">4</span></span> | <span data-ttu-id="bbfc1-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="bbfc1-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="bbfc1-152">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="bbfc1-152">OutputTensor</span></span> | <span data-ttu-id="bbfc1-153">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="bbfc1-153">Output</span></span> | <span data-ttu-id="bbfc1-154">4</span><span class="sxs-lookup"><span data-stu-id="bbfc1-154">4</span></span> | <span data-ttu-id="bbfc1-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="bbfc1-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="bbfc1-156">Требования</span><span class="sxs-lookup"><span data-stu-id="bbfc1-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bbfc1-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="bbfc1-157">**Header**</span></span> | <span data-ttu-id="bbfc1-158">директмл. h</span><span class="sxs-lookup"><span data-stu-id="bbfc1-158">directml.h</span></span> |
