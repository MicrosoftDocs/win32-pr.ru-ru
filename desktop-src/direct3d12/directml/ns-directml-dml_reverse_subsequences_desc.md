---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Меняет местами элементы одной или нескольких вложенных *последовательностей* тензорные. Набор подпоследовательностей, которые должны быть отменены, выбирается на основе указанной оси и длины последовательности.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719992"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="ff4cb-104">Структура DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="ff4cb-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ff4cb-105">Меняет местами элементы одной или нескольких вложенных *последовательностей* тензорные.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="ff4cb-106">Набор подпоследовательностей, которые должны быть отменены, выбирается на основе указанной оси и длины последовательности.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff4cb-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="ff4cb-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ff4cb-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ff4cb-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4cb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff4cb-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="ff4cb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ff4cb-110">Members</span></span>

`InputTensor`

<span data-ttu-id="ff4cb-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ff4cb-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ff4cb-112">Входной тензорные, содержащий элементы для обращения.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="ff4cb-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ff4cb-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ff4cb-114">Объект тензорные, содержащий значение для каждой подпоследовательности, которая должна быть отменена, обозначающая длину в элементах этой вложенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="ff4cb-115">Обращены только элементы в пределах длины вложенной последовательности. остальные элементы вдоль этой оси копируются в выходные данные без изменений.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="ff4cb-116">Этот тензорные должен иметь количество измерений и размеры, равные *инпуттенсор*, *за исключением* измерения, заданного параметром *Axis* .</span><span class="sxs-lookup"><span data-stu-id="ff4cb-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="ff4cb-117">Размер измерения *оси* должен быть равен 1.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="ff4cb-118">Например, если *инпуттенсор* имеет размеры `{2,3,4,5}` , а *ось* — 1, то размеры *секуенцеленгсстенсор* должны быть `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="ff4cb-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="ff4cb-119">Если длина подпоследовательности превышает максимальное количество элементов на этой оси, то этот оператор ведет себя так, как если бы значение было обработано до максимума.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="ff4cb-120">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ff4cb-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ff4cb-121">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-121">The output tensor to write the results to.</span></span> <span data-ttu-id="ff4cb-122">Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="ff4cb-123">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ff4cb-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ff4cb-124">Индекс измерения, по которому нужно обратить элементы.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="ff4cb-125">Это значение должно быть меньше значения параметра DimensionCount *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="ff4cb-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff4cb-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="ff4cb-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff4cb-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="ff4cb-128">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-128">Example 2.</span></span> <span data-ttu-id="ff4cb-129">Реверс вдоль другой оси</span><span class="sxs-lookup"><span data-stu-id="ff4cb-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="ff4cb-130">Доступность</span><span class="sxs-lookup"><span data-stu-id="ff4cb-130">Availability</span></span>
<span data-ttu-id="ff4cb-131">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ff4cb-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ff4cb-132">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-132">Tensor constraints</span></span>
* <span data-ttu-id="ff4cb-133">*Инпуттенсор*, *аутпуттенсор* и *секуенцеленгсстенсор* должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="ff4cb-134">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="ff4cb-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ff4cb-135">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="ff4cb-136">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="ff4cb-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="ff4cb-137">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-137">Tensor</span></span> | <span data-ttu-id="ff4cb-138">Вид</span><span class="sxs-lookup"><span data-stu-id="ff4cb-138">Kind</span></span> | <span data-ttu-id="ff4cb-139">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ff4cb-139">Supported dimension counts</span></span> | <span data-ttu-id="ff4cb-140">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ff4cb-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ff4cb-141">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-141">InputTensor</span></span> | <span data-ttu-id="ff4cb-142">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-142">Input</span></span> | <span data-ttu-id="ff4cb-143">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="ff4cb-143">4 to 5</span></span> | <span data-ttu-id="ff4cb-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ff4cb-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="ff4cb-145">секуенцеленгсстенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="ff4cb-146">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-146">Input</span></span> | <span data-ttu-id="ff4cb-147">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="ff4cb-147">4 to 5</span></span> | <span data-ttu-id="ff4cb-148">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="ff4cb-148">UINT32</span></span> |
| <span data-ttu-id="ff4cb-149">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-149">OutputTensor</span></span> | <span data-ttu-id="ff4cb-150">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-150">Output</span></span> | <span data-ttu-id="ff4cb-151">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="ff4cb-151">4 to 5</span></span> | <span data-ttu-id="ff4cb-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ff4cb-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="ff4cb-153">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="ff4cb-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="ff4cb-154">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-154">Tensor</span></span> | <span data-ttu-id="ff4cb-155">Вид</span><span class="sxs-lookup"><span data-stu-id="ff4cb-155">Kind</span></span> | <span data-ttu-id="ff4cb-156">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ff4cb-156">Supported dimension counts</span></span> | <span data-ttu-id="ff4cb-157">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ff4cb-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ff4cb-158">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-158">InputTensor</span></span> | <span data-ttu-id="ff4cb-159">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-159">Input</span></span> | <span data-ttu-id="ff4cb-160">4</span><span class="sxs-lookup"><span data-stu-id="ff4cb-160">4</span></span> | <span data-ttu-id="ff4cb-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ff4cb-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="ff4cb-162">секуенцеленгсстенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="ff4cb-163">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-163">Input</span></span> | <span data-ttu-id="ff4cb-164">4</span><span class="sxs-lookup"><span data-stu-id="ff4cb-164">4</span></span> | <span data-ttu-id="ff4cb-165">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="ff4cb-165">UINT32</span></span> |
| <span data-ttu-id="ff4cb-166">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ff4cb-166">OutputTensor</span></span> | <span data-ttu-id="ff4cb-167">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ff4cb-167">Output</span></span> | <span data-ttu-id="ff4cb-168">4</span><span class="sxs-lookup"><span data-stu-id="ff4cb-168">4</span></span> | <span data-ttu-id="ff4cb-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="ff4cb-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="ff4cb-170">Требования</span><span class="sxs-lookup"><span data-stu-id="ff4cb-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ff4cb-171">**Header**</span><span class="sxs-lookup"><span data-stu-id="ff4cb-171">**Header**</span></span> | <span data-ttu-id="ff4cb-172">директмл. h</span><span class="sxs-lookup"><span data-stu-id="ff4cb-172">directml.h</span></span> |