---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Вычисление максимального значения для элементов в скользящем окне над входным тензорные и при необходимости возвращает индексы для выбранных максимальных значений.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719996"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="d3ee1-103">Структура DML_MAX_POOLING2_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="d3ee1-104">Вычисление максимального значения для элементов в скользящем окне над входным тензорные и при необходимости возвращает индексы для выбранных максимальных значений.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3ee1-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="d3ee1-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d3ee1-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d3ee1-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ee1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3ee1-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="d3ee1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d3ee1-108">Members</span></span>

`InputTensor`

<span data-ttu-id="d3ee1-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3ee1-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3ee1-110">Входной тензорные *размера* `{ BatchCount, ChannelCount, Height, Width }` , если *инпуттенсор. DimensionCount* равен 4, а `{ BatchCount, ChannelCount, Depth, Height, Weight } ` Если *инпуттенсор. DimensionCount* — 5.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="d3ee1-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3ee1-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3ee1-112">Выходной тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-112">An output tensor to write the results to.</span></span> <span data-ttu-id="d3ee1-113">Размеры выходных тензорные можно вычислить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="d3ee1-114">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3ee1-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3ee1-115">Необязательный выходной тензорные индексов для входных тензорные *инпуттенсор* максимальных значений, создаваемых и хранимых в *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="d3ee1-116">Эти индексные значения отсчитываются от нуля и обрабатывают входные тензорные в виде непрерывного одномерного массива.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="d3ee1-117">Если несколько элементов в скользящем окне имеют одинаковое значение, то более поздние значения не учитываются, а индекс указывает на первое обнаруженное значение.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="d3ee1-118">*Аутпуттенсор* и *аутпутиндицестенсор* имеют одинаковый размер тензорные.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="d3ee1-119">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d3ee1-120">Количество пространственных измерений входного тензорные *инпуттенсор*, которое также соответствует числу измерений скользящего окна *WindowSize*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="d3ee1-121">Это значение также определяет размер массивов *stride*, *стартпаддинг* и *ендпаддинг* .</span><span class="sxs-lookup"><span data-stu-id="d3ee1-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="d3ee1-122">Он должен иметь значение 2, если *инпуттенсор* — 4d, и 3, если это a 5D тензорные.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="d3ee1-123">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="d3ee1-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="d3ee1-124">Шаг для измерений скользящего окна размеров, если для `{ Height, Width }` *DimensionCount* задано значение 2 или `{ Depth, Height, Width }` значение 3.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="d3ee1-125">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="d3ee1-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="d3ee1-126">Размеры скользящего окна в, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="d3ee1-127">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="d3ee1-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="d3ee1-128">Число элементов заполнения, применяемых к началу каждого пространственного измерения входного тензорные *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="d3ee1-129">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="d3ee1-130">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="d3ee1-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="d3ee1-131">Количество элементов заполнения, применяемых к концу каждого пространственного измерения входного тензорные *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="d3ee1-132">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="d3ee1-133">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="d3ee1-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="d3ee1-134">Значения для каждого пространственного измерения входного тензорные *инпуттенсор* , по которому выбирается элемент в скользящем окне для каждого элемента этого значения.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="d3ee1-135">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="d3ee1-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3ee1-136">Remarks</span></span>
<span data-ttu-id="d3ee1-137">**DML_MAX_POOLING2_OPERATOR_DESC** заменяет более раннюю версию [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) с дополнительным массивом констант *дилатионс*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="d3ee1-138">Две версии эквивалентны, если для *дилатионс* задано значение `{ 1,1 }` для входных данных 4d или `{ 1,1,1 }` для входных функций 5D.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="d3ee1-139">Доступность</span><span class="sxs-lookup"><span data-stu-id="d3ee1-139">Availability</span></span>
<span data-ttu-id="d3ee1-140">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d3ee1-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d3ee1-141">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-141">Tensor constraints</span></span>
* <span data-ttu-id="d3ee1-142">*Инпуттенсор*, *аутпутиндицестенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="d3ee1-143">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="d3ee1-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d3ee1-144">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="d3ee1-145">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="d3ee1-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="d3ee1-146">Тензорные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-146">Tensor</span></span> | <span data-ttu-id="d3ee1-147">Вид</span><span class="sxs-lookup"><span data-stu-id="d3ee1-147">Kind</span></span> | <span data-ttu-id="d3ee1-148">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="d3ee1-148">Supported dimension counts</span></span> | <span data-ttu-id="d3ee1-149">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="d3ee1-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d3ee1-150">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-150">InputTensor</span></span> | <span data-ttu-id="d3ee1-151">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-151">Input</span></span> | <span data-ttu-id="d3ee1-152">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-152">4 to 5</span></span> | <span data-ttu-id="d3ee1-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3ee1-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="d3ee1-154">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-154">OutputTensor</span></span> | <span data-ttu-id="d3ee1-155">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-155">Output</span></span> | <span data-ttu-id="d3ee1-156">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-156">4 to 5</span></span> | <span data-ttu-id="d3ee1-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3ee1-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="d3ee1-158">аутпутиндицестенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-158">OutputIndicesTensor</span></span> | <span data-ttu-id="d3ee1-159">Необязательный вывод</span><span class="sxs-lookup"><span data-stu-id="d3ee1-159">Optional output</span></span> | <span data-ttu-id="d3ee1-160">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-160">4 to 5</span></span> | <span data-ttu-id="d3ee1-161">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="d3ee1-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="d3ee1-162">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="d3ee1-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="d3ee1-163">Тензорные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-163">Tensor</span></span> | <span data-ttu-id="d3ee1-164">Вид</span><span class="sxs-lookup"><span data-stu-id="d3ee1-164">Kind</span></span> | <span data-ttu-id="d3ee1-165">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="d3ee1-165">Supported dimension counts</span></span> | <span data-ttu-id="d3ee1-166">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="d3ee1-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d3ee1-167">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-167">InputTensor</span></span> | <span data-ttu-id="d3ee1-168">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-168">Input</span></span> | <span data-ttu-id="d3ee1-169">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-169">4 to 5</span></span> | <span data-ttu-id="d3ee1-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d3ee1-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d3ee1-171">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-171">OutputTensor</span></span> | <span data-ttu-id="d3ee1-172">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="d3ee1-172">Output</span></span> | <span data-ttu-id="d3ee1-173">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-173">4 to 5</span></span> | <span data-ttu-id="d3ee1-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="d3ee1-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="d3ee1-175">аутпутиндицестенсор</span><span class="sxs-lookup"><span data-stu-id="d3ee1-175">OutputIndicesTensor</span></span> | <span data-ttu-id="d3ee1-176">Необязательный вывод</span><span class="sxs-lookup"><span data-stu-id="d3ee1-176">Optional output</span></span> | <span data-ttu-id="d3ee1-177">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="d3ee1-177">4 to 5</span></span> | <span data-ttu-id="d3ee1-178">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="d3ee1-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="d3ee1-179">Требования</span><span class="sxs-lookup"><span data-stu-id="d3ee1-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d3ee1-180">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-180">**Minimum supported client**</span></span> | <span data-ttu-id="d3ee1-181">Windows 10, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="d3ee1-182">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-182">**Minimum supported server**</span></span> | <span data-ttu-id="d3ee1-183">Windows Server, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="d3ee1-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="d3ee1-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-184">**Header**</span></span> | <span data-ttu-id="d3ee1-185">директмл. h</span><span class="sxs-lookup"><span data-stu-id="d3ee1-185">directml.h</span></span> |