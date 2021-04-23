---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку данных квантования. Этот оператор математически эквивалентен декуантизинг входным данным, включающим, а затем куантизинг выходные данные.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803876"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="ee856-105">Структура DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="ee856-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ee856-106">Выполняет свертывание *филтертенсор* с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="ee856-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="ee856-107">Этот оператор выполняет пересылку данных квантования.</span><span class="sxs-lookup"><span data-stu-id="ee856-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="ee856-108">Этот оператор математически эквивалентен декуантизинг входным данным, включающим, а затем куантизинг выходные данные.</span><span class="sxs-lookup"><span data-stu-id="ee856-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="ee856-109">К линейным функциям квантуем, используемым этим оператором, относятся линейные функции дискретизация</span><span class="sxs-lookup"><span data-stu-id="ee856-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="ee856-110">Функция декуантизе</span><span class="sxs-lookup"><span data-stu-id="ee856-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="ee856-111">Функция квантуем</span><span class="sxs-lookup"><span data-stu-id="ee856-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="ee856-112">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="ee856-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ee856-113">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ee856-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee856-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee856-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="ee856-115">Члены</span><span class="sxs-lookup"><span data-stu-id="ee856-115">Members</span></span>

`InputTensor`

<span data-ttu-id="ee856-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-117">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="ee856-117">A tensor containing the input data.</span></span> <span data-ttu-id="ee856-118">Ожидаемые размеры *инпуттенсор* : `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="ee856-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-120">Объект тензорные, содержащий входные данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="ee856-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="ee856-121">Ожидаемые размеры `InputScaleTensor` — `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ee856-122">Это значение шкалы используется для декуантизинг входных значений.</span><span class="sxs-lookup"><span data-stu-id="ee856-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="ee856-123">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-124">Необязательный тензорные, содержащий входные данные нулевой точки.</span><span class="sxs-lookup"><span data-stu-id="ee856-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="ee856-125">Ожидаемые размеры *инпутзеропоинттенсор* : `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ee856-126">Это значение нулевой точки используется для декуантизинг входных значений.</span><span class="sxs-lookup"><span data-stu-id="ee856-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="ee856-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-128">Объект тензорные, содержащий данные фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-128">A tensor containing the filter data.</span></span> <span data-ttu-id="ee856-129">Ожидаемые размеры *филтертенсор* : `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="ee856-130">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-131">Объект тензорные, содержащий данные шкалы фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="ee856-132">Ожидаемыми размерами `FilterScaleTensor` являются, `{ 1, 1, 1, 1 }` Если требуется для каждого тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация на канал.</span><span class="sxs-lookup"><span data-stu-id="ee856-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="ee856-133">Это значение шкалы используется для декуантизинг значений фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="ee856-134">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-135">Необязательный тензорные, содержащий данные нулевой точки фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="ee856-136">Ожидаемые размеры *филтерзеропоинттенсор* , `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация по каналу.</span><span class="sxs-lookup"><span data-stu-id="ee856-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="ee856-137">Это значение нулевой точки используется для декуантизинг значений фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="ee856-138">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-139">Объект тензорные, содержащий данные смещения.</span><span class="sxs-lookup"><span data-stu-id="ee856-139">A tensor containing the bias data.</span></span> <span data-ttu-id="ee856-140">Тензорные смещения — это тензорные, содержащий данные, которые рассылаются по выходным тензорные в конце свертки, который добавляется к результату.</span><span class="sxs-lookup"><span data-stu-id="ee856-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="ee856-141">Ожидаемые размеры Биастенсор `{ 1, OutputChannelCount, 1, 1 }` для 4d.</span><span class="sxs-lookup"><span data-stu-id="ee856-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="ee856-142">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-143">Объект тензорные, содержащий данные шкалы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ee856-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="ee856-144">Ожидаемые размеры Аутпутскалетенсор: `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ee856-145">Это значение входной шкалы используется для куантизинг выходных значений свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="ee856-146">Тип: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-147">Необязательный тензорные, содержащий данные нулевой точки фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="ee856-148">Ожидаемые размеры Аутпутзеропоинттенсор: `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ee856-149">Это значение ввода нулевой точки используется для куантизинг для свертки выходных значений.</span><span class="sxs-lookup"><span data-stu-id="ee856-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="ee856-150">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ee856-151">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="ee856-151">A tensor to write the results to.</span></span> <span data-ttu-id="ee856-152">Ожидаемые размеры Аутпуттенсор: `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ee856-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="ee856-153">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ee856-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ee856-154">Количество пространственных измерений для операции свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="ee856-155">Пространственные измерения — это нижние измерения фильтра свертки тензорные *филтертенсор*.</span><span class="sxs-lookup"><span data-stu-id="ee856-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="ee856-156">Это значение также определяет размер массивов *stride*, *дилатионс*, *стартпаддинг* и *ендпаддинг* .</span><span class="sxs-lookup"><span data-stu-id="ee856-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="ee856-157">Поддерживается только значение 2.</span><span class="sxs-lookup"><span data-stu-id="ee856-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="ee856-158">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="ee856-159">Шаг операции свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-159">The strides of the convolution operation.</span></span> <span data-ttu-id="ee856-160">Эти шаг применяются к фильтру свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="ee856-161">Они отделены от тензорные STRIDE, которые включены в [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="ee856-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="ee856-162">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="ee856-163">Дилатионс операции свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="ee856-164">Дилатионс — это шаг, примененный к элементам ядра фильтра.</span><span class="sxs-lookup"><span data-stu-id="ee856-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="ee856-165">Это влияет на моделирование ядра более крупного фильтра, добавляя внутренние элементы ядра фильтрации с нулями.</span><span class="sxs-lookup"><span data-stu-id="ee856-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="ee856-166">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="ee856-167">Значения заполнения, применяемые к началу каждого пространственного измерения фильтра и входного тензорные операции свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="ee856-168">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="ee856-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="ee856-169">Значения заполнения, применяемые к концу каждого пространственного измерения фильтра и входного тензорные операции свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="ee856-170">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ee856-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ee856-171">Число групп, в которые следует разделить операцию свертки.</span><span class="sxs-lookup"><span data-stu-id="ee856-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="ee856-172">*Граупкаунт* можно использовать для достижения более глубокого свертки, задав *граупкаунт* равным количеству входных каналов.</span><span class="sxs-lookup"><span data-stu-id="ee856-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="ee856-173">Это делит свертывание в отдельное свертка на входной канал.</span><span class="sxs-lookup"><span data-stu-id="ee856-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="ee856-174">Доступность</span><span class="sxs-lookup"><span data-stu-id="ee856-174">Availability</span></span>
<span data-ttu-id="ee856-175">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ee856-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ee856-176">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="ee856-176">Tensor constraints</span></span>
* <span data-ttu-id="ee856-177">*Филтертенсор* и *филтерзеропоинттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="ee856-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="ee856-178">*Инпуттенсор* и *инпутзеропоинттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="ee856-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="ee856-179">*Аутпуттенсор* и `OutputZeroPointTensor` должны иметь один и тот же *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="ee856-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ee856-180">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="ee856-180">Tensor support</span></span>
| <span data-ttu-id="ee856-181">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ee856-181">Tensor</span></span> | <span data-ttu-id="ee856-182">Вид</span><span class="sxs-lookup"><span data-stu-id="ee856-182">Kind</span></span> | <span data-ttu-id="ee856-183">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ee856-183">Supported dimension counts</span></span> | <span data-ttu-id="ee856-184">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ee856-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ee856-185">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-185">InputTensor</span></span> | <span data-ttu-id="ee856-186">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-186">Input</span></span> | <span data-ttu-id="ee856-187">4</span><span class="sxs-lookup"><span data-stu-id="ee856-187">4</span></span> | <span data-ttu-id="ee856-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-188">INT8, UINT8</span></span> |
| <span data-ttu-id="ee856-189">инпутскалетенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-189">InputScaleTensor</span></span> | <span data-ttu-id="ee856-190">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-190">Input</span></span> | <span data-ttu-id="ee856-191">4</span><span class="sxs-lookup"><span data-stu-id="ee856-191">4</span></span> | <span data-ttu-id="ee856-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ee856-192">FLOAT32</span></span> |
| <span data-ttu-id="ee856-193">инпутзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-193">InputZeroPointTensor</span></span> | <span data-ttu-id="ee856-194">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="ee856-194">Optional input</span></span> | <span data-ttu-id="ee856-195">4</span><span class="sxs-lookup"><span data-stu-id="ee856-195">4</span></span> | <span data-ttu-id="ee856-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-196">INT8, UINT8</span></span> |
| <span data-ttu-id="ee856-197">филтертенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-197">FilterTensor</span></span> | <span data-ttu-id="ee856-198">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-198">Input</span></span> | <span data-ttu-id="ee856-199">4</span><span class="sxs-lookup"><span data-stu-id="ee856-199">4</span></span> | <span data-ttu-id="ee856-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-200">INT8, UINT8</span></span> |
| <span data-ttu-id="ee856-201">филтерскалетенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-201">FilterScaleTensor</span></span> | <span data-ttu-id="ee856-202">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-202">Input</span></span> | <span data-ttu-id="ee856-203">4</span><span class="sxs-lookup"><span data-stu-id="ee856-203">4</span></span> | <span data-ttu-id="ee856-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ee856-204">FLOAT32</span></span> |
| <span data-ttu-id="ee856-205">филтерзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="ee856-206">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="ee856-206">Optional input</span></span> | <span data-ttu-id="ee856-207">4</span><span class="sxs-lookup"><span data-stu-id="ee856-207">4</span></span> | <span data-ttu-id="ee856-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-208">INT8, UINT8</span></span> |
| <span data-ttu-id="ee856-209">биастенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-209">BiasTensor</span></span> | <span data-ttu-id="ee856-210">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="ee856-210">Optional input</span></span> | <span data-ttu-id="ee856-211">4</span><span class="sxs-lookup"><span data-stu-id="ee856-211">4</span></span> | <span data-ttu-id="ee856-212">INT32</span><span class="sxs-lookup"><span data-stu-id="ee856-212">INT32</span></span> |
| <span data-ttu-id="ee856-213">аутпутскалетенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-213">OutputScaleTensor</span></span> | <span data-ttu-id="ee856-214">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-214">Input</span></span> | <span data-ttu-id="ee856-215">4</span><span class="sxs-lookup"><span data-stu-id="ee856-215">4</span></span> | <span data-ttu-id="ee856-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ee856-216">FLOAT32</span></span> |
| <span data-ttu-id="ee856-217">аутпутзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="ee856-218">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="ee856-218">Optional input</span></span> | <span data-ttu-id="ee856-219">4</span><span class="sxs-lookup"><span data-stu-id="ee856-219">4</span></span> | <span data-ttu-id="ee856-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-220">INT8, UINT8</span></span> |
| <span data-ttu-id="ee856-221">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ee856-221">OutputTensor</span></span> | <span data-ttu-id="ee856-222">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ee856-222">Output</span></span> | <span data-ttu-id="ee856-223">4</span><span class="sxs-lookup"><span data-stu-id="ee856-223">4</span></span> | <span data-ttu-id="ee856-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ee856-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="ee856-225">Требования</span><span class="sxs-lookup"><span data-stu-id="ee856-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ee856-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="ee856-226">**Header**</span></span> | <span data-ttu-id="ee856-227">директмл. h</span><span class="sxs-lookup"><span data-stu-id="ee856-227">directml.h</span></span> |