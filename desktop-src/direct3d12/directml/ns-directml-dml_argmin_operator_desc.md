---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Выводит индексы элементов с минимальными значениями в одном или нескольких измерениях входного тензорные.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 2e12a81593504a4eb7a0917e545bfa20c70647ff
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804079"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="80bf1-103">Структура DML_ARGMIN_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="80bf1-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="80bf1-104">Выводит индексы элементов с минимальными значениями в одном или нескольких измерениях входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="80bf1-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="80bf1-105">Каждый элемент Output является результатом применения *аргмин* сокращения для подмножества входных тензорные.</span><span class="sxs-lookup"><span data-stu-id="80bf1-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="80bf1-106">Функция *аргмин* выводит индекс элемента с минимальными значениями в наборе входных элементов.</span><span class="sxs-lookup"><span data-stu-id="80bf1-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="80bf1-107">Входные элементы, участвующие в каждом уменьшении, определяются предоставленными осями ввода.</span><span class="sxs-lookup"><span data-stu-id="80bf1-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="80bf1-108">Аналогичным образом, каждый выходной индекс по отношению к предоставленным осям входных данных.</span><span class="sxs-lookup"><span data-stu-id="80bf1-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="80bf1-109">Если указаны все входные оси, оператор применяет одно *аргминное* уменьшение и создает один выходной элемент.</span><span class="sxs-lookup"><span data-stu-id="80bf1-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80bf1-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="80bf1-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="80bf1-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="80bf1-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80bf1-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80bf1-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="80bf1-113">Члены</span><span class="sxs-lookup"><span data-stu-id="80bf1-113">Members</span></span>

`InputTensor`

<span data-ttu-id="80bf1-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="80bf1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="80bf1-115">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="80bf1-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="80bf1-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="80bf1-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="80bf1-117">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="80bf1-117">The tensor to write the results to.</span></span> <span data-ttu-id="80bf1-118">Каждый элемент Output является результатом *аргмин* сокращения для подмножества элементов из *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="80bf1-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="80bf1-119">*DimensionCount* должен соответствовать *инпуттенсор. DimensionCount* (ранг входного тензорные сохраняется).</span><span class="sxs-lookup"><span data-stu-id="80bf1-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="80bf1-120">*Размеры* должны соответствовать *инпуттенсор. sizes*, за исключением измерений, содержащихся в сокращенных *осях*, которые должны иметь размер 1.</span><span class="sxs-lookup"><span data-stu-id="80bf1-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="80bf1-121">Тип: **[uint](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="80bf1-121">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="80bf1-122">Число осей, которые необходимо уменьшить.</span><span class="sxs-lookup"><span data-stu-id="80bf1-122">The number of axes to reduce.</span></span> <span data-ttu-id="80bf1-123">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="80bf1-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="80bf1-124">Тип: \_ Field_size \_ (аксискаунт) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="80bf1-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="80bf1-125">Оси, которые необходимо уменьшить.</span><span class="sxs-lookup"><span data-stu-id="80bf1-125">The axes along which to reduce.</span></span> <span data-ttu-id="80bf1-126">Значения должны находиться в диапазоне `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="80bf1-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="80bf1-127">DML_AXIS_DIRECTION Аксисдиректион;</span><span class="sxs-lookup"><span data-stu-id="80bf1-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="80bf1-128">Тип: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="80bf1-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="80bf1-129">Определяет, какой индекс следует выбрать, если несколько входных элементов имеют одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="80bf1-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="80bf1-130">**DML_AXIS_DIRECTION_INCREASING** возвращает индекс первого элемента с минимальным значением (например, `argmin({1,2,3,2,1}) = 0` ).</span><span class="sxs-lookup"><span data-stu-id="80bf1-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="80bf1-131">**DML_AXIS_DIRECTION_DECREASING** возвращает индекс последнего элемента с минимальным значением (например, `argmin({1,2,3,2,1}) = 4` ).</span><span class="sxs-lookup"><span data-stu-id="80bf1-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="80bf1-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="80bf1-132">Examples</span></span>

<span data-ttu-id="80bf1-133">В примерах в этом разделе используется одинаковый двухмерный входной тензорные.</span><span class="sxs-lookup"><span data-stu-id="80bf1-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="80bf1-134">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="80bf1-134">Example 1.</span></span> <span data-ttu-id="80bf1-135">Применение *аргмин* к столбцам</span><span class="sxs-lookup"><span data-stu-id="80bf1-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="80bf1-136">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="80bf1-136">Example 2.</span></span> <span data-ttu-id="80bf1-137">Применение *аргмин* к строкам</span><span class="sxs-lookup"><span data-stu-id="80bf1-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="80bf1-138">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="80bf1-138">Example 3.</span></span> <span data-ttu-id="80bf1-139">Применение *аргмин* ко всем осям (весь тензорные)</span><span class="sxs-lookup"><span data-stu-id="80bf1-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="80bf1-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80bf1-140">Remarks</span></span>
<span data-ttu-id="80bf1-141">Размеры выходных тензорные должны совпадать с размерами входных тензорные, за исключением осей с меньшими осями, которые должны иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="80bf1-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="80bf1-142">Если *аксисдиректион* имеет [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), этот API эквивалентен [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) с [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="80bf1-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="80bf1-143">Подмножество этой функции предоставляется с помощью оператора [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) и поддерживается на более ранних уровнях функций директмл.</span><span class="sxs-lookup"><span data-stu-id="80bf1-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="80bf1-144">Доступность</span><span class="sxs-lookup"><span data-stu-id="80bf1-144">Availability</span></span>
<span data-ttu-id="80bf1-145">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="80bf1-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="80bf1-146">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="80bf1-146">Tensor constraints</span></span>
<span data-ttu-id="80bf1-147">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="80bf1-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="80bf1-148">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="80bf1-148">Tensor support</span></span>
| <span data-ttu-id="80bf1-149">Тензорные</span><span class="sxs-lookup"><span data-stu-id="80bf1-149">Tensor</span></span> | <span data-ttu-id="80bf1-150">Вид</span><span class="sxs-lookup"><span data-stu-id="80bf1-150">Kind</span></span> | <span data-ttu-id="80bf1-151">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="80bf1-151">Supported dimension counts</span></span> | <span data-ttu-id="80bf1-152">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="80bf1-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="80bf1-153">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="80bf1-153">InputTensor</span></span> | <span data-ttu-id="80bf1-154">Входные данные</span><span class="sxs-lookup"><span data-stu-id="80bf1-154">Input</span></span> | <span data-ttu-id="80bf1-155">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="80bf1-155">1 to 8</span></span> | <span data-ttu-id="80bf1-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="80bf1-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="80bf1-157">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="80bf1-157">OutputTensor</span></span> | <span data-ttu-id="80bf1-158">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="80bf1-158">Output</span></span> | <span data-ttu-id="80bf1-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="80bf1-159">1 to 8</span></span> | <span data-ttu-id="80bf1-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="80bf1-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="80bf1-161">Требования</span><span class="sxs-lookup"><span data-stu-id="80bf1-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="80bf1-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="80bf1-162">**Header**</span></span> | <span data-ttu-id="80bf1-163">директмл. h</span><span class="sxs-lookup"><span data-stu-id="80bf1-163">directml.h</span></span> |