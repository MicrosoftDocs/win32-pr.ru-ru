---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для повторной выборки (см. [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804052"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="05364-103">Структура DML_RESAMPLE_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="05364-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="05364-104">Вычисление градиентов обратного распространения для повторной выборки (см. [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="05364-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="05364-105">**DML_RESAMPLE1_OPERATOR_DESC** выполняет масштабирование произвольных измерений входного тензорные, используя либо ближайшую выборку, либо билинейной интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="05364-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="05364-106">При наличии *инпутградиенттенсор* с теми же размерами, что и в *выходных данных* эквивалентного **DML_RESAMPLE1_OPERATOR_DESC**, этот оператор создает *аутпутградиенттенсор* с теми же размерами, что и *входные данные* **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="05364-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="05364-107">В качестве примера рассмотрим **DML_RESAMPLE1_OPERATOR_DESC** , которая выполняет масштабирование по ширине в 1,5 x в ширину, а 0,5 x — по высоте.</span><span class="sxs-lookup"><span data-stu-id="05364-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="05364-108">Обратите внимание, что элемент 0-ом входного тензорные (со значением 1) участвует в двух элементах в выходных данных, первый элемент (со значением 2) участвует в одном элементе выходных данных, а второй и третий элементы (со значениями 3 и 4) не вносят элементов в выходные данные.</span><span class="sxs-lookup"><span data-stu-id="05364-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="05364-109">Соответствующий **DML_RESAMPLE_GRAD_OPERATOR_DESC** будет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="05364-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="05364-110">Обратите внимание, что значения в *аутпутградиенттенсор* представляют взвешенные вклады этого элемента в *аутпуттенсор* во время исходного оператора **DML_RESAMPLE1_OPERATOR_DESC** .</span><span class="sxs-lookup"><span data-stu-id="05364-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05364-111">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="05364-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="05364-112">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="05364-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05364-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05364-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="05364-114">Члены</span><span class="sxs-lookup"><span data-stu-id="05364-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="05364-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05364-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05364-116">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="05364-116">The incoming gradient tensor.</span></span> <span data-ttu-id="05364-117">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="05364-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="05364-118">Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="05364-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="05364-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="05364-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="05364-120">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="05364-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="05364-121">Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="05364-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="05364-122">Тип: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="05364-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="05364-123">См. раздел *интерполатионмоде* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05364-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="05364-124">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="05364-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="05364-125">Число *элементов в массивах Scale,* *инпутпикселоффсетс* и *аутпутпикселоффсетс* .</span><span class="sxs-lookup"><span data-stu-id="05364-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="05364-126">Это значение должно равняться *DimensionCount* , указанному в *инпутградиенттенсор* и *аутпутградиенттенсор*.</span><span class="sxs-lookup"><span data-stu-id="05364-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="05364-127">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05364-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05364-128">См. раздел *масштабирование* в [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05364-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="05364-129">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05364-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05364-130">См. раздел *инпутпикселоффсетс* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05364-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="05364-131">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="05364-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="05364-132">См. раздел *аутпутпикселоффсетс* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="05364-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="05364-133">Доступность</span><span class="sxs-lookup"><span data-stu-id="05364-133">Availability</span></span>
<span data-ttu-id="05364-134">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="05364-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="05364-135">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="05364-135">Tensor constraints</span></span>
<span data-ttu-id="05364-136">*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="05364-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="05364-137">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="05364-137">Tensor support</span></span>
| <span data-ttu-id="05364-138">Тензорные</span><span class="sxs-lookup"><span data-stu-id="05364-138">Tensor</span></span> | <span data-ttu-id="05364-139">Вид</span><span class="sxs-lookup"><span data-stu-id="05364-139">Kind</span></span> | <span data-ttu-id="05364-140">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="05364-140">Supported dimension counts</span></span> | <span data-ttu-id="05364-141">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="05364-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="05364-142">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="05364-142">InputGradientTensor</span></span> | <span data-ttu-id="05364-143">Входные данные</span><span class="sxs-lookup"><span data-stu-id="05364-143">Input</span></span> | <span data-ttu-id="05364-144">4</span><span class="sxs-lookup"><span data-stu-id="05364-144">4</span></span> | <span data-ttu-id="05364-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05364-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="05364-146">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="05364-146">OutputGradientTensor</span></span> | <span data-ttu-id="05364-147">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="05364-147">Output</span></span> | <span data-ttu-id="05364-148">4</span><span class="sxs-lookup"><span data-stu-id="05364-148">4</span></span> | <span data-ttu-id="05364-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="05364-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="05364-150">Требования</span><span class="sxs-lookup"><span data-stu-id="05364-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="05364-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="05364-151">**Header**</span></span> | <span data-ttu-id="05364-152">директмл. h</span><span class="sxs-lookup"><span data-stu-id="05364-152">directml.h</span></span> |