---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Выводит индексы элементов с максимальным значением в одном или нескольких измерениях входного тензорные.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719953"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="0df9d-103">Структура DML_ARGMAX_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="0df9d-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0df9d-104">Выводит индексы элементов с максимальным значением в одном или нескольких измерениях входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="0df9d-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="0df9d-105">Каждый элемент Output является результатом применения *аргмакс* сокращения для подмножества входных тензорные.</span><span class="sxs-lookup"><span data-stu-id="0df9d-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="0df9d-106">Функция *аргмакс* выводит индекс элемента с максимальным значением в наборе входных элементов.</span><span class="sxs-lookup"><span data-stu-id="0df9d-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="0df9d-107">Входные элементы, участвующие в каждом уменьшении, определяются предоставленными осями ввода.</span><span class="sxs-lookup"><span data-stu-id="0df9d-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="0df9d-108">Аналогичным образом, каждый выходной индекс по отношению к предоставленным осям входных данных.</span><span class="sxs-lookup"><span data-stu-id="0df9d-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="0df9d-109">Если указаны все входные оси, оператор применяет одно *аргмаксное* уменьшение и создает один выходной элемент.</span><span class="sxs-lookup"><span data-stu-id="0df9d-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0df9d-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="0df9d-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0df9d-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0df9d-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0df9d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0df9d-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="0df9d-113">Члены</span><span class="sxs-lookup"><span data-stu-id="0df9d-113">Members</span></span>

`InputTensor`

<span data-ttu-id="0df9d-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0df9d-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0df9d-115">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="0df9d-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="0df9d-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0df9d-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0df9d-117">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="0df9d-117">The tensor to write the results to.</span></span> <span data-ttu-id="0df9d-118">Каждый элемент Output является результатом *аргмакс* сокращения для подмножества элементов из *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="0df9d-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="0df9d-119">*DimensionCount* должен соответствовать *инпуттенсор. DimensionCount* (ранг входного тензорные сохраняется).</span><span class="sxs-lookup"><span data-stu-id="0df9d-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="0df9d-120">*Размеры* должны соответствовать *инпуттенсор. sizes*, за исключением измерений, содержащихся в сокращенных *осях*, которые должны иметь размер 1.</span><span class="sxs-lookup"><span data-stu-id="0df9d-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="0df9d-121">Тип: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0df9d-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0df9d-122">Число осей, которые необходимо уменьшить.</span><span class="sxs-lookup"><span data-stu-id="0df9d-122">The number of axes to reduce.</span></span> <span data-ttu-id="0df9d-123">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="0df9d-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="0df9d-124">Тип: \_ Field_size \_ (аксискаунт) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="0df9d-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0df9d-125">Оси, которые необходимо уменьшить.</span><span class="sxs-lookup"><span data-stu-id="0df9d-125">The axes along which to reduce.</span></span> <span data-ttu-id="0df9d-126">Значения должны находиться в диапазоне `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="0df9d-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="0df9d-127">Тип: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="0df9d-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="0df9d-128">Определяет, какой индекс следует выбрать, если несколько входных элементов имеют одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="0df9d-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="0df9d-129">**DML_AXIS_DIRECTION_INCREASING** возвращает индекс первого элемента с максимальным значением (например, `argmax({3,2,1,2,3}) = 0` ).</span><span class="sxs-lookup"><span data-stu-id="0df9d-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="0df9d-130">**DML_AXIS_DIRECTION_DECREASING** возвращает индекс последнего элемента с максимальным значением (например, `argmax({3,2,1,2,3}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="0df9d-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="0df9d-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="0df9d-131">Examples</span></span>

<span data-ttu-id="0df9d-132">В примерах в этом разделе используется одинаковый двухмерный входной тензорные.</span><span class="sxs-lookup"><span data-stu-id="0df9d-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="0df9d-133">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="0df9d-133">Example 1.</span></span> <span data-ttu-id="0df9d-134">Применение *аргмакс* к столбцам</span><span class="sxs-lookup"><span data-stu-id="0df9d-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="0df9d-135">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="0df9d-135">Example 2.</span></span> <span data-ttu-id="0df9d-136">Применение *аргмакс* к строкам</span><span class="sxs-lookup"><span data-stu-id="0df9d-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="0df9d-137">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="0df9d-137">Example 3.</span></span> <span data-ttu-id="0df9d-138">Применение *аргмакс* ко всем осям (весь тензорные)</span><span class="sxs-lookup"><span data-stu-id="0df9d-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="0df9d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0df9d-139">Remarks</span></span>
<span data-ttu-id="0df9d-140">Размеры выходных тензорные должны совпадать с размерами входных тензорные, за исключением осей с меньшими осями, которые должны иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="0df9d-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="0df9d-141">Если *аксисдиректион* имеет [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), этот API эквивалентен [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) с [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="0df9d-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="0df9d-142">Подмножество этой функции предоставляется с помощью оператора [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) и поддерживается на более ранних уровнях функций директмл.</span><span class="sxs-lookup"><span data-stu-id="0df9d-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="0df9d-143">Доступность</span><span class="sxs-lookup"><span data-stu-id="0df9d-143">Availability</span></span>
<span data-ttu-id="0df9d-144">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="0df9d-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0df9d-145">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="0df9d-145">Tensor constraints</span></span>
<span data-ttu-id="0df9d-146">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="0df9d-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0df9d-147">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="0df9d-147">Tensor support</span></span>
| <span data-ttu-id="0df9d-148">Тензорные</span><span class="sxs-lookup"><span data-stu-id="0df9d-148">Tensor</span></span> | <span data-ttu-id="0df9d-149">Вид</span><span class="sxs-lookup"><span data-stu-id="0df9d-149">Kind</span></span> | <span data-ttu-id="0df9d-150">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="0df9d-150">Supported dimension counts</span></span> | <span data-ttu-id="0df9d-151">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="0df9d-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0df9d-152">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="0df9d-152">InputTensor</span></span> | <span data-ttu-id="0df9d-153">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0df9d-153">Input</span></span> | <span data-ttu-id="0df9d-154">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="0df9d-154">1 to 8</span></span> | <span data-ttu-id="0df9d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0df9d-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0df9d-156">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="0df9d-156">OutputTensor</span></span> | <span data-ttu-id="0df9d-157">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="0df9d-157">Output</span></span> | <span data-ttu-id="0df9d-158">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="0df9d-158">1 to 8</span></span> | <span data-ttu-id="0df9d-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="0df9d-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="0df9d-160">Требования</span><span class="sxs-lookup"><span data-stu-id="0df9d-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0df9d-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="0df9d-161">**Header**</span></span> | <span data-ttu-id="0df9d-162">директмл. h</span><span class="sxs-lookup"><span data-stu-id="0df9d-162">directml.h</span></span> |