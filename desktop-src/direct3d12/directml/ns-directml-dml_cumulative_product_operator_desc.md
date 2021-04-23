---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Умножает элементы тензорные вдоль оси, записывая выполняющийся высокий коэффициент произведения в выходном тензорные.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 2f0c6a6b6f12792a245027a7f8e86c05f7e85192
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804515"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="00ac4-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="00ac4-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="00ac4-104">Умножает элементы тензорные вдоль оси, записывая выполняющийся высокий коэффициент произведения в выходном тензорные.</span><span class="sxs-lookup"><span data-stu-id="00ac4-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00ac4-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="00ac4-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="00ac4-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="00ac4-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="00ac4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00ac4-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="00ac4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="00ac4-108">Members</span></span>

`InputTensor`

<span data-ttu-id="00ac4-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="00ac4-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="00ac4-110">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="00ac4-110">A tensor containing the input data.</span></span> <span data-ttu-id="00ac4-111">Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="00ac4-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="00ac4-112">Входной тензорные, содержащий элементы для умножения.</span><span class="sxs-lookup"><span data-stu-id="00ac4-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="00ac4-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="00ac4-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="00ac4-114">Выходной тензорные для записи итоговых совокупных продуктов в.</span><span class="sxs-lookup"><span data-stu-id="00ac4-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="00ac4-115">Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="00ac4-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="00ac4-116">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="00ac4-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="00ac4-117">Индекс измерения, по которому необходимо умножить элементы.</span><span class="sxs-lookup"><span data-stu-id="00ac4-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="00ac4-118">Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="00ac4-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="00ac4-119">Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="00ac4-119">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="00ac4-120">Одно из значений перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="00ac4-120">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="00ac4-121">Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то продукт выполняется путем просмотра тензорные вдоль указанной оси по возрастанию индекса элементов.</span><span class="sxs-lookup"><span data-stu-id="00ac4-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="00ac4-122">Если задано значение **DML_AXIS_DIRECTION_DECREASING**, возвращается обратное значение true, а продукт выполняется путем обхода элементов по убыванию индекса.</span><span class="sxs-lookup"><span data-stu-id="00ac4-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="00ac4-123">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="00ac4-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="00ac4-124">Если значение — **true**, значение текущего элемента исключается при записи выполняемого счетчика в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="00ac4-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="00ac4-125">При значении **false** значение текущего элемента включается в счетчик выполняется.</span><span class="sxs-lookup"><span data-stu-id="00ac4-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="00ac4-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="00ac4-126">Examples</span></span>

<span data-ttu-id="00ac4-127">В примерах в этом разделе используются те же входные тензорные.</span><span class="sxs-lookup"><span data-stu-id="00ac4-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="00ac4-128">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="00ac4-128">Example 1.</span></span> <span data-ttu-id="00ac4-129">Совокупный продукт по горизонтали сливерс</span><span class="sxs-lookup"><span data-stu-id="00ac4-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="00ac4-130">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="00ac4-130">Example 2.</span></span> <span data-ttu-id="00ac4-131">Эксклюзивные продукты</span><span class="sxs-lookup"><span data-stu-id="00ac4-131">Exclusive products</span></span>

<span data-ttu-id="00ac4-132">Установка параметра *хасексклусивепродукт* в **значение true** оказывает за исключением значения текущего элемента из счетчика, выполняемого при записи в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="00ac4-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="00ac4-133">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="00ac4-133">Example 3.</span></span> <span data-ttu-id="00ac4-134">Направление оси</span><span class="sxs-lookup"><span data-stu-id="00ac4-134">Axis direction</span></span>

<span data-ttu-id="00ac4-135">Установка параметра *аксисдиректион* в значение [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/direct3d12/directml/ne-directml-dml_axis_direction) оказывает обратный порядок обхода элементов при вычислении счетчика выполнения.</span><span class="sxs-lookup"><span data-stu-id="00ac4-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/direct3d12/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="00ac4-136">Пример 4.</span><span class="sxs-lookup"><span data-stu-id="00ac4-136">Example 4.</span></span> <span data-ttu-id="00ac4-137">Умножение вдоль другой оси</span><span class="sxs-lookup"><span data-stu-id="00ac4-137">Multiplying along a different axis</span></span>

<span data-ttu-id="00ac4-138">В этом примере продукт выполняется вертикально вдоль оси высоты (второе измерение).</span><span class="sxs-lookup"><span data-stu-id="00ac4-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="00ac4-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00ac4-139">Remarks</span></span>
<span data-ttu-id="00ac4-140">Этот оператор поддерживает выполнение на месте. Это означает, что тензорные вывода может иметь псевдоним *инпуттенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="00ac4-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="00ac4-141">Доступность</span><span class="sxs-lookup"><span data-stu-id="00ac4-141">Availability</span></span>
<span data-ttu-id="00ac4-142">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="00ac4-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="00ac4-143">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="00ac4-143">Tensor constraints</span></span>
<span data-ttu-id="00ac4-144">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="00ac4-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="00ac4-145">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="00ac4-145">Tensor support</span></span>
| <span data-ttu-id="00ac4-146">Тензорные</span><span class="sxs-lookup"><span data-stu-id="00ac4-146">Tensor</span></span> | <span data-ttu-id="00ac4-147">Вид</span><span class="sxs-lookup"><span data-stu-id="00ac4-147">Kind</span></span> | <span data-ttu-id="00ac4-148">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="00ac4-148">Supported dimension counts</span></span> | <span data-ttu-id="00ac4-149">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="00ac4-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="00ac4-150">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="00ac4-150">InputTensor</span></span> | <span data-ttu-id="00ac4-151">Входные данные</span><span class="sxs-lookup"><span data-stu-id="00ac4-151">Input</span></span> | <span data-ttu-id="00ac4-152">4</span><span class="sxs-lookup"><span data-stu-id="00ac4-152">4</span></span> | <span data-ttu-id="00ac4-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="00ac4-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="00ac4-154">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="00ac4-154">OutputTensor</span></span> | <span data-ttu-id="00ac4-155">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="00ac4-155">Output</span></span> | <span data-ttu-id="00ac4-156">4</span><span class="sxs-lookup"><span data-stu-id="00ac4-156">4</span></span> | <span data-ttu-id="00ac4-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="00ac4-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="00ac4-158">Требования</span><span class="sxs-lookup"><span data-stu-id="00ac4-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="00ac4-159">**Header**</span><span class="sxs-lookup"><span data-stu-id="00ac4-159">**Header**</span></span> | <span data-ttu-id="00ac4-160">директмл. h</span><span class="sxs-lookup"><span data-stu-id="00ac4-160">directml.h</span></span> |
