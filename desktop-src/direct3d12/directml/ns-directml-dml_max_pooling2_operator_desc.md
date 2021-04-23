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
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803665"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="44244-103">Структура DML_MAX_POOLING2_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="44244-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="44244-104">Вычисление максимального значения для элементов в скользящем окне над входным тензорные и при необходимости возвращает индексы для выбранных максимальных значений.</span><span class="sxs-lookup"><span data-stu-id="44244-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44244-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="44244-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="44244-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="44244-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44244-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44244-107">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="44244-108">Члены</span><span class="sxs-lookup"><span data-stu-id="44244-108">Members</span></span>

`InputTensor`

<span data-ttu-id="44244-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44244-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44244-110">Входной тензорные *размера* `{ BatchCount, ChannelCount, Height, Width }` , если *инпуттенсор. DimensionCount* равен 4, а `{ BatchCount, ChannelCount, Depth, Height, Weight } ` Если *инпуттенсор. DimensionCount* — 5.</span><span class="sxs-lookup"><span data-stu-id="44244-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="44244-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44244-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44244-112">Выходной тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="44244-112">An output tensor to write the results to.</span></span> <span data-ttu-id="44244-113">Размеры выходных тензорные можно вычислить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="44244-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="44244-114">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44244-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44244-115">Необязательный выходной тензорные индексов для входных тензорные *инпуттенсор* максимальных значений, создаваемых и хранимых в *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="44244-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="44244-116">Эти индексные значения отсчитываются от нуля и обрабатывают входные тензорные в виде непрерывного одномерного массива.</span><span class="sxs-lookup"><span data-stu-id="44244-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="44244-117">Если несколько элементов в скользящем окне имеют одинаковое значение, то более поздние значения не учитываются, а индекс указывает на первое обнаруженное значение.</span><span class="sxs-lookup"><span data-stu-id="44244-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="44244-118">*Аутпуттенсор* и *аутпутиндицестенсор* имеют одинаковый размер тензорные.</span><span class="sxs-lookup"><span data-stu-id="44244-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="44244-119">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44244-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44244-120">Количество пространственных измерений входного тензорные *инпуттенсор*, которое также соответствует числу измерений скользящего окна *WindowSize*.</span><span class="sxs-lookup"><span data-stu-id="44244-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="44244-121">Это значение также определяет размер массивов *stride*, *стартпаддинг* и *ендпаддинг* .</span><span class="sxs-lookup"><span data-stu-id="44244-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="44244-122">Он должен иметь значение 2, если *инпуттенсор* — 4d, и 3, если это a 5D тензорные.</span><span class="sxs-lookup"><span data-stu-id="44244-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="44244-123">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="44244-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="44244-124">Шаг для измерений скользящего окна размеров, если для `{ Height, Width }` *DimensionCount* задано значение 2 или `{ Depth, Height, Width }` значение 3.</span><span class="sxs-lookup"><span data-stu-id="44244-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="44244-125">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="44244-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="44244-126">Размеры скользящего окна в, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="44244-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="44244-127">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="44244-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="44244-128">Число элементов заполнения, применяемых к началу каждого пространственного измерения входного тензорные *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="44244-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="44244-129">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="44244-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="44244-130">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="44244-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="44244-131">Количество элементов заполнения, применяемых к концу каждого пространственного измерения входного тензорные *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="44244-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="44244-132">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="44244-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="44244-133">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="44244-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="44244-134">Значения для каждого пространственного измерения входного тензорные *инпуттенсор* , по которому выбирается элемент в скользящем окне для каждого элемента этого значения.</span><span class="sxs-lookup"><span data-stu-id="44244-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="44244-135">Значения находятся в параметре, `{ Height, Width }` Если *DimensionCount* имеет значение 2 или `{ Depth, Height, Width }` Если значение равно 3.</span><span class="sxs-lookup"><span data-stu-id="44244-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="44244-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44244-136">Remarks</span></span>
<span data-ttu-id="44244-137">**DML_MAX_POOLING2_OPERATOR_DESC** заменяет более раннюю версию [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) с дополнительным массивом констант *дилатионс*.</span><span class="sxs-lookup"><span data-stu-id="44244-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="44244-138">Две версии эквивалентны, если для *дилатионс* задано значение `{ 1,1 }` для входных данных 4d или `{ 1,1,1 }` для входных функций 5D.</span><span class="sxs-lookup"><span data-stu-id="44244-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="44244-139">Доступность</span><span class="sxs-lookup"><span data-stu-id="44244-139">Availability</span></span>
<span data-ttu-id="44244-140">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="44244-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="44244-141">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="44244-141">Tensor constraints</span></span>
* <span data-ttu-id="44244-142">*Инпуттенсор*, *аутпутиндицестенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44244-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="44244-143">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="44244-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="44244-144">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="44244-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="44244-145">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="44244-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="44244-146">Тензорные</span><span class="sxs-lookup"><span data-stu-id="44244-146">Tensor</span></span> | <span data-ttu-id="44244-147">Вид</span><span class="sxs-lookup"><span data-stu-id="44244-147">Kind</span></span> | <span data-ttu-id="44244-148">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="44244-148">Supported dimension counts</span></span> | <span data-ttu-id="44244-149">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="44244-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44244-150">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="44244-150">InputTensor</span></span> | <span data-ttu-id="44244-151">Входные данные</span><span class="sxs-lookup"><span data-stu-id="44244-151">Input</span></span> | <span data-ttu-id="44244-152">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-152">4 to 5</span></span> | <span data-ttu-id="44244-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="44244-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="44244-154">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="44244-154">OutputTensor</span></span> | <span data-ttu-id="44244-155">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="44244-155">Output</span></span> | <span data-ttu-id="44244-156">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-156">4 to 5</span></span> | <span data-ttu-id="44244-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="44244-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="44244-158">аутпутиндицестенсор</span><span class="sxs-lookup"><span data-stu-id="44244-158">OutputIndicesTensor</span></span> | <span data-ttu-id="44244-159">Необязательный вывод</span><span class="sxs-lookup"><span data-stu-id="44244-159">Optional output</span></span> | <span data-ttu-id="44244-160">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-160">4 to 5</span></span> | <span data-ttu-id="44244-161">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="44244-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="44244-162">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="44244-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="44244-163">Тензорные</span><span class="sxs-lookup"><span data-stu-id="44244-163">Tensor</span></span> | <span data-ttu-id="44244-164">Вид</span><span class="sxs-lookup"><span data-stu-id="44244-164">Kind</span></span> | <span data-ttu-id="44244-165">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="44244-165">Supported dimension counts</span></span> | <span data-ttu-id="44244-166">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="44244-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44244-167">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="44244-167">InputTensor</span></span> | <span data-ttu-id="44244-168">Входные данные</span><span class="sxs-lookup"><span data-stu-id="44244-168">Input</span></span> | <span data-ttu-id="44244-169">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-169">4 to 5</span></span> | <span data-ttu-id="44244-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="44244-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="44244-171">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="44244-171">OutputTensor</span></span> | <span data-ttu-id="44244-172">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="44244-172">Output</span></span> | <span data-ttu-id="44244-173">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-173">4 to 5</span></span> | <span data-ttu-id="44244-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="44244-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="44244-175">аутпутиндицестенсор</span><span class="sxs-lookup"><span data-stu-id="44244-175">OutputIndicesTensor</span></span> | <span data-ttu-id="44244-176">Необязательный вывод</span><span class="sxs-lookup"><span data-stu-id="44244-176">Optional output</span></span> | <span data-ttu-id="44244-177">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="44244-177">4 to 5</span></span> | <span data-ttu-id="44244-178">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="44244-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="44244-179">Требования</span><span class="sxs-lookup"><span data-stu-id="44244-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="44244-180">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="44244-180">**Minimum supported client**</span></span> | <span data-ttu-id="44244-181">Windows 10, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="44244-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="44244-182">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="44244-182">**Minimum supported server**</span></span> | <span data-ttu-id="44244-183">Windows Server, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="44244-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="44244-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="44244-184">**Header**</span></span> | <span data-ttu-id="44244-185">директмл. h</span><span class="sxs-lookup"><span data-stu-id="44244-185">directml.h</span></span> |