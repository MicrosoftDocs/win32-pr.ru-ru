---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Извлекает одну подобласть (срез) входного тензорные.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803947"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="78075-103">Структура DML_SLICE1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="78075-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="78075-104">Извлекает одну подобласть (срез) входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="78075-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="78075-105">В *окне ввода* описываются границы входных тензорные, которые следует учитывать в срезе.</span><span class="sxs-lookup"><span data-stu-id="78075-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="78075-106">Окно определяется с использованием трех значений для каждого измерения.</span><span class="sxs-lookup"><span data-stu-id="78075-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="78075-107">*Смещение* отмечает *начало окна* в измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="78075-108">*Размер* отмечает область окна в измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="78075-109">В качестве *конца окна* в измерении используется `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="78075-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="78075-110">*Шаг* указывает, как перемещаться по элементам измерения.</span><span class="sxs-lookup"><span data-stu-id="78075-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="78075-111">Величина шага указывает, сколько элементов следует продвинуть при копировании в пределах окна.</span><span class="sxs-lookup"><span data-stu-id="78075-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="78075-112">Если шаг с шагом положительный, элементы копируются начиная с *начала* окна в измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="78075-113">Если шаг по индексу отрицательный, элементы копируются, начиная с *конца* окна в измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="78075-114">В следующем псевдо-коде показано, как копируются элементы с помощью окна ввода.</span><span class="sxs-lookup"><span data-stu-id="78075-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="78075-115">Обратите внимание, как копируются элементы в измерении с начала до конца с положительным шагом и копируются из End в начало с отрицательным шагом.</span><span class="sxs-lookup"><span data-stu-id="78075-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="78075-116">Окно ввода не должны быть пустым в любом измерении, а окно не должны выходит за пределы размера входного тензорные (операции чтения вне границ не разрешены).</span><span class="sxs-lookup"><span data-stu-id="78075-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="78075-117">Размер и шаг окна фактически ограничивают количество элементов, которые могут быть скопированы из каждого измерения `i` входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="78075-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="78075-118">Выходной тензорные не требуется для копирования всех достижимых элементов в окне.</span><span class="sxs-lookup"><span data-stu-id="78075-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="78075-119">Срез допустим, пока `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .</span><span class="sxs-lookup"><span data-stu-id="78075-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78075-120">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="78075-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="78075-121">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="78075-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78075-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78075-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="78075-123">Члены</span><span class="sxs-lookup"><span data-stu-id="78075-123">Members</span></span>

`InputTensor`

<span data-ttu-id="78075-124">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78075-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78075-125">Тензорные, из которого извлекаются срезы.</span><span class="sxs-lookup"><span data-stu-id="78075-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="78075-126">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="78075-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="78075-127">Объект тензорные, в который записываются результаты среза данных.</span><span class="sxs-lookup"><span data-stu-id="78075-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="78075-128">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="78075-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="78075-129">Число измерений.</span><span class="sxs-lookup"><span data-stu-id="78075-129">The number of dimensions.</span></span> <span data-ttu-id="78075-130">Это поле определяет размер массивов *инпутвиндовоффсетс*, *инпутвиндовсизес* и *инпутвиндовстридес* .</span><span class="sxs-lookup"><span data-stu-id="78075-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="78075-131">Это значение должно соответствовать *DimensionCountным* десяткам входных и выходных данных.</span><span class="sxs-lookup"><span data-stu-id="78075-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="78075-132">Это значение должно находиться в диапазоне от 1 до 8 включительно, начиная с `DML_FEATURE_LEVEL_3_0` версии. для более ранних уровней компонентов требуется значение 4 или 5.</span><span class="sxs-lookup"><span data-stu-id="78075-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="78075-133">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="78075-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="78075-134">Массив, содержащий начало (в элементах) окна ввода в каждом измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="78075-135">Значения в массиве должны соответствовать ограничению `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="78075-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="78075-136">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="78075-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="78075-137">Массив, содержащий экстент (в элементах) окна ввода в каждом измерении.</span><span class="sxs-lookup"><span data-stu-id="78075-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="78075-138">Значения в массиве должны соответствовать ограничению `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="78075-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="78075-139">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="78075-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="78075-140">Массив, содержащий шаг среза по каждому измерению входного тензорные в элементах.</span><span class="sxs-lookup"><span data-stu-id="78075-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="78075-141">Величина шага указывает, сколько элементов следует продвинуть при копировании в окне ввода.</span><span class="sxs-lookup"><span data-stu-id="78075-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="78075-142">Знак шага определяет, копируются ли элементы, начиная с начала окна (положительный шаг) или заканчивая окном (отрицательный шаг).</span><span class="sxs-lookup"><span data-stu-id="78075-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="78075-143">Шаг не может быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="78075-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="78075-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="78075-144">Examples</span></span>

<span data-ttu-id="78075-145">В следующих примерах используется такой же входной тензорные.</span><span class="sxs-lookup"><span data-stu-id="78075-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="78075-146">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="78075-146">Example 1.</span></span> <span data-ttu-id="78075-147">Срез с шагом с положительным шагом</span><span class="sxs-lookup"><span data-stu-id="78075-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="78075-148">Скопированные элементы рассчитываются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="78075-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="78075-149">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="78075-149">Example 2.</span></span> <span data-ttu-id="78075-150">Срез с шагом с отрицательным шагом</span><span class="sxs-lookup"><span data-stu-id="78075-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="78075-151">Помните, что измерения с отрицательным шагом окна начинают копирование в конец окна ввода для этого измерения; Это делается путем добавления `InputWindowSize[i] - 1` к смещению окна.</span><span class="sxs-lookup"><span data-stu-id="78075-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="78075-152">Измерения с положительным шагом просто начинаются с `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="78075-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="78075-153">Ось 0 ( `+1` Window STRIDE) начинает копирование в `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="78075-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="78075-154">Ось 1 ( `+1` Window STRIDE) начинает копирование в `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="78075-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="78075-155">Ось 2 ( `-2` Window STRIDE) начинает копирование в `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="78075-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="78075-156">Ось 3 ( `+2` Window STRIDE) начинает копирование в `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="78075-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="78075-157">Скопированные элементы рассчитываются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="78075-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="78075-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78075-158">Remarks</span></span>
<span data-ttu-id="78075-159">Этот оператор аналогичен [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), но он отличается двумя важными способами.</span><span class="sxs-lookup"><span data-stu-id="78075-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="78075-160">Шаг среза может быть отрицательным, что позволяет реверсировать значения по измерениям.</span><span class="sxs-lookup"><span data-stu-id="78075-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="78075-161">Размеры окна ввода не обязательно должны совпадать с размерами выходных тензорные.</span><span class="sxs-lookup"><span data-stu-id="78075-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="78075-162">Доступность</span><span class="sxs-lookup"><span data-stu-id="78075-162">Availability</span></span>
<span data-ttu-id="78075-163">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="78075-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="78075-164">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="78075-164">Tensor constraints</span></span>
<span data-ttu-id="78075-165">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="78075-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="78075-166">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="78075-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="78075-167">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="78075-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="78075-168">Тензорные</span><span class="sxs-lookup"><span data-stu-id="78075-168">Tensor</span></span> | <span data-ttu-id="78075-169">Вид</span><span class="sxs-lookup"><span data-stu-id="78075-169">Kind</span></span> | <span data-ttu-id="78075-170">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="78075-170">Supported dimension counts</span></span> | <span data-ttu-id="78075-171">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="78075-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="78075-172">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78075-172">InputTensor</span></span> | <span data-ttu-id="78075-173">Входные данные</span><span class="sxs-lookup"><span data-stu-id="78075-173">Input</span></span> | <span data-ttu-id="78075-174">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="78075-174">1 to 8</span></span> | <span data-ttu-id="78075-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78075-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="78075-176">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78075-176">OutputTensor</span></span> | <span data-ttu-id="78075-177">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="78075-177">Output</span></span> | <span data-ttu-id="78075-178">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="78075-178">1 to 8</span></span> | <span data-ttu-id="78075-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78075-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="78075-180">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="78075-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="78075-181">Тензорные</span><span class="sxs-lookup"><span data-stu-id="78075-181">Tensor</span></span> | <span data-ttu-id="78075-182">Вид</span><span class="sxs-lookup"><span data-stu-id="78075-182">Kind</span></span> | <span data-ttu-id="78075-183">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="78075-183">Supported dimension counts</span></span> | <span data-ttu-id="78075-184">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="78075-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="78075-185">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78075-185">InputTensor</span></span> | <span data-ttu-id="78075-186">Входные данные</span><span class="sxs-lookup"><span data-stu-id="78075-186">Input</span></span> | <span data-ttu-id="78075-187">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="78075-187">4 to 5</span></span> | <span data-ttu-id="78075-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78075-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="78075-189">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="78075-189">OutputTensor</span></span> | <span data-ttu-id="78075-190">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="78075-190">Output</span></span> | <span data-ttu-id="78075-191">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="78075-191">4 to 5</span></span> | <span data-ttu-id="78075-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="78075-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="78075-193">Требования</span><span class="sxs-lookup"><span data-stu-id="78075-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="78075-194">**Header**</span><span class="sxs-lookup"><span data-stu-id="78075-194">**Header**</span></span> | <span data-ttu-id="78075-195">директмл. h</span><span class="sxs-lookup"><span data-stu-id="78075-195">directml.h</span></span> |