---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Выполняет свертывание *филтертенсор* с *инпуттенсор*. Этот оператор выполняет пересылку по целочисленным данным.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550420"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="67660-104">Структура DML_CONVOLUTION_INTEGER_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="67660-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="67660-105">Выполняет свертывание *филтертенсор* с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="67660-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="67660-106">Этот оператор выполняет пересылку по целочисленным данным.</span><span class="sxs-lookup"><span data-stu-id="67660-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="67660-107">Необязательные десятки точек нулевой точки также можно использовать для вычитания значений нулевой точки из входных данных и фильтра тензорные.</span><span class="sxs-lookup"><span data-stu-id="67660-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67660-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="67660-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="67660-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="67660-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="67660-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67660-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="67660-111">Участники</span><span class="sxs-lookup"><span data-stu-id="67660-111">Members</span></span>

`InputTensor`

<span data-ttu-id="67660-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="67660-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="67660-113">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="67660-113">A tensor containing the input data.</span></span> <span data-ttu-id="67660-114">Ожидаемые размеры *инпуттенсор* : `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="67660-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="67660-115">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="67660-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="67660-116">Необязательный тензорные, содержащий входные данные нулевой точки.</span><span class="sxs-lookup"><span data-stu-id="67660-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="67660-117">Ожидаемые размеры *инпутзеропоинттенсор* : `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="67660-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="67660-118">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="67660-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="67660-119">Объект тензорные, содержащий данные фильтра.</span><span class="sxs-lookup"><span data-stu-id="67660-119">A tensor containing the filter data.</span></span> <span data-ttu-id="67660-120">Ожидаемые размеры *филтертенсор* : `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="67660-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="67660-121">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="67660-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="67660-122">Необязательный тензорные, содержащий данные нулевой точки фильтра.</span><span class="sxs-lookup"><span data-stu-id="67660-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="67660-123">Ожидаемые размеры *филтерзеропоинттенсор* , `{ 1, 1, 1, 1 }` Если требуется по тензорные дискретизация, или `{ 1, OutputChannelCount, 1, 1 }` Если требуется дискретизация для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="67660-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="67660-124">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="67660-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="67660-125">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="67660-125">The tensor to write the results to.</span></span> <span data-ttu-id="67660-126">Ожидаемые размеры *аутпуттенсор* : `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="67660-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="67660-127">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="67660-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="67660-128">Количество пространственных измерений для операции свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="67660-129">Пространственные измерения — это нижние измерения *филтертенсор* свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="67660-130">Это значение также определяет размер массивов *stride*, *дилатионс*, *стартпаддинг* и *ендпаддинг* .</span><span class="sxs-lookup"><span data-stu-id="67660-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="67660-131">Поддерживается только значение 2.</span><span class="sxs-lookup"><span data-stu-id="67660-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="67660-132">Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="67660-132">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67660-133">Массив, содержащий шаг операции свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="67660-134">Эти шаг применяются к фильтру свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="67660-135">Они отделены от тензорные STRIDE, которые включены в [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="67660-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="67660-136">Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="67660-136">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67660-137">Массив, содержащий дилатионс операции свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="67660-138">Дилатионс — это шаг, примененный к элементам ядра фильтра.</span><span class="sxs-lookup"><span data-stu-id="67660-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="67660-139">Это влияет на моделирование ядра более крупного фильтра, добавляя внутренние элементы ядра фильтрации с нулями.</span><span class="sxs-lookup"><span data-stu-id="67660-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="67660-140">Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="67660-140">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67660-141">Массив, содержащий значения заполнения, применяемые к началу каждого пространственного измерения фильтра и входного тензорные операции свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="67660-142">Тип: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="67660-142">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="67660-143">Массив, содержащий значения заполнения, применяемые к концу каждого пространственного измерения фильтра и входного тензорные операции свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="67660-144">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="67660-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="67660-145">Число групп, в которые необходимо разделить операцию свертки.</span><span class="sxs-lookup"><span data-stu-id="67660-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="67660-146">*Граупкаунт* можно использовать для достижения более глубокого свертки, задав *граупкаунт* равным количеству входных каналов.</span><span class="sxs-lookup"><span data-stu-id="67660-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="67660-147">Это делит свертывание в отдельное свертка на входной канал.</span><span class="sxs-lookup"><span data-stu-id="67660-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="67660-148">Доступность</span><span class="sxs-lookup"><span data-stu-id="67660-148">Availability</span></span>
<span data-ttu-id="67660-149">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="67660-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="67660-150">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="67660-150">Tensor constraints</span></span>
* <span data-ttu-id="67660-151">*Филтертенсор* и *филтерзеропоинттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="67660-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="67660-152">*Инпуттенсор* и *инпутзеропоинттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="67660-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="67660-153">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="67660-153">Tensor support</span></span>
| <span data-ttu-id="67660-154">Тензорные</span><span class="sxs-lookup"><span data-stu-id="67660-154">Tensor</span></span> | <span data-ttu-id="67660-155">Вид</span><span class="sxs-lookup"><span data-stu-id="67660-155">Kind</span></span> | <span data-ttu-id="67660-156">Измерения</span><span class="sxs-lookup"><span data-stu-id="67660-156">Dimensions</span></span> | <span data-ttu-id="67660-157">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="67660-157">Supported dimension counts</span></span> | <span data-ttu-id="67660-158">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="67660-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="67660-159">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="67660-159">InputTensor</span></span> | <span data-ttu-id="67660-160">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67660-160">Input</span></span> | <span data-ttu-id="67660-161">{Батчкаунт, Инпутчаннелкаунт, Инпусеигхт, Инпутвидс}</span><span class="sxs-lookup"><span data-stu-id="67660-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="67660-162">4</span><span class="sxs-lookup"><span data-stu-id="67660-162">4</span></span> | <span data-ttu-id="67660-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="67660-163">INT8, UINT8</span></span> |
| <span data-ttu-id="67660-164">инпутзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="67660-164">InputZeroPointTensor</span></span> | <span data-ttu-id="67660-165">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="67660-165">Optional input</span></span> | <span data-ttu-id="67660-166">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="67660-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="67660-167">4</span><span class="sxs-lookup"><span data-stu-id="67660-167">4</span></span> | <span data-ttu-id="67660-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="67660-168">INT8, UINT8</span></span> |
| <span data-ttu-id="67660-169">филтертенсор</span><span class="sxs-lookup"><span data-stu-id="67660-169">FilterTensor</span></span> | <span data-ttu-id="67660-170">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67660-170">Input</span></span> | <span data-ttu-id="67660-171">{Филтербатчкаунт, Филтерчаннелкаунт, Филтерхеигхт, Филтервидс}</span><span class="sxs-lookup"><span data-stu-id="67660-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="67660-172">4</span><span class="sxs-lookup"><span data-stu-id="67660-172">4</span></span> | <span data-ttu-id="67660-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="67660-173">INT8, UINT8</span></span> |
| <span data-ttu-id="67660-174">филтерзеропоинттенсор</span><span class="sxs-lookup"><span data-stu-id="67660-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="67660-175">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="67660-175">Optional input</span></span> | <span data-ttu-id="67660-176">{1, Филтерзеропоинтчаннелкаунт, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="67660-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="67660-177">4</span><span class="sxs-lookup"><span data-stu-id="67660-177">4</span></span> | <span data-ttu-id="67660-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="67660-178">INT8, UINT8</span></span> |
| <span data-ttu-id="67660-179">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="67660-179">OutputTensor</span></span> | <span data-ttu-id="67660-180">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="67660-180">Output</span></span> | <span data-ttu-id="67660-181">{Батчкаунт, Аутпутчаннелкаунт, Аутпусеигхт, Аутпутвидс}</span><span class="sxs-lookup"><span data-stu-id="67660-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="67660-182">4</span><span class="sxs-lookup"><span data-stu-id="67660-182">4</span></span> | <span data-ttu-id="67660-183">INT32</span><span class="sxs-lookup"><span data-stu-id="67660-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="67660-184">Требования</span><span class="sxs-lookup"><span data-stu-id="67660-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="67660-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="67660-185">**Header**</span></span> | <span data-ttu-id="67660-186">директмл. h</span><span class="sxs-lookup"><span data-stu-id="67660-186">directml.h</span></span> |