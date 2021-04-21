---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Собирает элементы из входного тензорные вдоль заданной оси, используя индексы тензорные для преобразования во входные данные.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803020"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="e5184-103">Структура DML_GATHER_ELEMENTS_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e5184-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e5184-104">Собирает элементы из входного тензорные вдоль заданной оси, используя индексы тензорные для преобразования во входные данные.</span><span class="sxs-lookup"><span data-stu-id="e5184-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="e5184-105">Этот оператор выполняет следующий псевдокод с точным поведением, зависящим от оси, числа входных измерений и числа измерений индексов.</span><span class="sxs-lookup"><span data-stu-id="e5184-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="e5184-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="e5184-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e5184-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e5184-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5184-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5184-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="e5184-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e5184-109">Members</span></span>

`InputTensor`

<span data-ttu-id="e5184-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e5184-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e5184-111">Тензорные, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="e5184-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="e5184-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e5184-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e5184-113">Индексы для входного тензорные вдоль активной оси.</span><span class="sxs-lookup"><span data-stu-id="e5184-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="e5184-114">*Размеры* должны соответствовать *инпуттенсор. sizes* для каждого измерения, кроме *оси*.</span><span class="sxs-lookup"><span data-stu-id="e5184-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="e5184-115">Начиная с `DML_FEATURE_LEVEL_3_0` , этот оператор поддерживает отрицательные значения индекса при использовании целочисленного типа со знаком с этим тензорные.</span><span class="sxs-lookup"><span data-stu-id="e5184-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="e5184-116">Отрицательные индексы обрабатываются относительно конца измерения оси.</span><span class="sxs-lookup"><span data-stu-id="e5184-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="e5184-117">Например, индекс-1 ссылается на последний элемент в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="e5184-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="e5184-118">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e5184-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e5184-119">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="e5184-119">The tensor to write the results to.</span></span> <span data-ttu-id="e5184-120">*Размеры* должны соответствовать *индицестенсор. sizes*, а *тип данных* должен соответствовать *инпуттенсор. DataType*.</span><span class="sxs-lookup"><span data-stu-id="e5184-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="e5184-121">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e5184-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e5184-122">Измерение оси *инпуттенсор* , которое необходимо собрать вместе, в диапазоне `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="e5184-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="e5184-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="e5184-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="e5184-124">Доступность</span><span class="sxs-lookup"><span data-stu-id="e5184-124">Availability</span></span>
<span data-ttu-id="e5184-125">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e5184-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e5184-126">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e5184-126">Tensor constraints</span></span>
* <span data-ttu-id="e5184-127">`IndicesTensor`, *Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="e5184-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="e5184-128">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="e5184-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e5184-129">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e5184-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="e5184-130">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="e5184-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="e5184-131">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e5184-131">Tensor</span></span> | <span data-ttu-id="e5184-132">Вид</span><span class="sxs-lookup"><span data-stu-id="e5184-132">Kind</span></span> | <span data-ttu-id="e5184-133">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e5184-133">Supported dimension counts</span></span> | <span data-ttu-id="e5184-134">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e5184-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e5184-135">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-135">InputTensor</span></span> | <span data-ttu-id="e5184-136">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-136">Input</span></span> | <span data-ttu-id="e5184-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e5184-137">1 to 8</span></span> | <span data-ttu-id="e5184-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e5184-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e5184-139">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-139">IndicesTensor</span></span> | <span data-ttu-id="e5184-140">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-140">Input</span></span> | <span data-ttu-id="e5184-141">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e5184-141">1 to 8</span></span> | <span data-ttu-id="e5184-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="e5184-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="e5184-143">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-143">OutputTensor</span></span> | <span data-ttu-id="e5184-144">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-144">Output</span></span> | <span data-ttu-id="e5184-145">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e5184-145">1 to 8</span></span> | <span data-ttu-id="e5184-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e5184-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e5184-147">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="e5184-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="e5184-148">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e5184-148">Tensor</span></span> | <span data-ttu-id="e5184-149">Вид</span><span class="sxs-lookup"><span data-stu-id="e5184-149">Kind</span></span> | <span data-ttu-id="e5184-150">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e5184-150">Supported dimension counts</span></span> | <span data-ttu-id="e5184-151">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e5184-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e5184-152">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-152">InputTensor</span></span> | <span data-ttu-id="e5184-153">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-153">Input</span></span> | <span data-ttu-id="e5184-154">4</span><span class="sxs-lookup"><span data-stu-id="e5184-154">4</span></span> | <span data-ttu-id="e5184-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e5184-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e5184-156">индицестенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-156">IndicesTensor</span></span> | <span data-ttu-id="e5184-157">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-157">Input</span></span> | <span data-ttu-id="e5184-158">4</span><span class="sxs-lookup"><span data-stu-id="e5184-158">4</span></span> | <span data-ttu-id="e5184-159">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="e5184-159">UINT32</span></span> |
| <span data-ttu-id="e5184-160">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e5184-160">OutputTensor</span></span> | <span data-ttu-id="e5184-161">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e5184-161">Output</span></span> | <span data-ttu-id="e5184-162">4</span><span class="sxs-lookup"><span data-stu-id="e5184-162">4</span></span> | <span data-ttu-id="e5184-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e5184-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e5184-164">Требования</span><span class="sxs-lookup"><span data-stu-id="e5184-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e5184-165">**Header**</span><span class="sxs-lookup"><span data-stu-id="e5184-165">**Header**</span></span> | <span data-ttu-id="e5184-166">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e5184-166">directml.h</span></span> |