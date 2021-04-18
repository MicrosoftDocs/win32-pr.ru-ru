---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для максимального количества пулов (см. [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720057"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="40590-103">Структура DML_MAX_POOLING_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="40590-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="40590-104">Вычисление градиентов обратного распространения для максимального количества пулов (см. [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="40590-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="40590-105">Рассмотрим **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 без заполнения и дилатионс, а также шаг 1, который выполняет следующее.</span><span class="sxs-lookup"><span data-stu-id="40590-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="40590-106">Самый крупный элемент каждого окна 2x2 во входном тензорные создает один элемент выходных данных.</span><span class="sxs-lookup"><span data-stu-id="40590-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="40590-107">Ниже приведен пример выходных данных **DML_MAX_POOLING_GRAD_OPERATOR_DESC** с учетом аналогичных параметров.</span><span class="sxs-lookup"><span data-stu-id="40590-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="40590-108">Фактически этот оператор использует *инпуттенсор* для определения индекса самого крупного элемента из каждого окна и распространяет значения *инпутградиенттенсор* в *аутпутградиенттенсор* на основе этих индексов.</span><span class="sxs-lookup"><span data-stu-id="40590-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="40590-109">Где индексы перекрываются, значения суммируются.</span><span class="sxs-lookup"><span data-stu-id="40590-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="40590-110">Все элементы вывода, не имеющие ссылки, обнуляются.</span><span class="sxs-lookup"><span data-stu-id="40590-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="40590-111">В случае с привязкум (если более одного элемента в окне имеют одинаковое максимальное значение) выбирается элемент с наименьшим индексом логического элемента.</span><span class="sxs-lookup"><span data-stu-id="40590-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40590-112">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="40590-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="40590-113">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="40590-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40590-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40590-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="40590-115">Члены</span><span class="sxs-lookup"><span data-stu-id="40590-115">Members</span></span>

`InputTensor`

<span data-ttu-id="40590-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="40590-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="40590-117">Входная функция тензорные.</span><span class="sxs-lookup"><span data-stu-id="40590-117">The input feature tensor.</span></span> <span data-ttu-id="40590-118">Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="40590-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="40590-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="40590-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="40590-120">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="40590-120">The incoming gradient tensor.</span></span> <span data-ttu-id="40590-121">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="40590-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="40590-122">Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="40590-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="40590-123">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="40590-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="40590-124">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="40590-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="40590-125">Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="40590-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="40590-126">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="40590-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="40590-127">Число элементов в массивах *stride*, *WindowSize*, *стартпаддинг*, *ендпаддинг* и *дилатионс* .</span><span class="sxs-lookup"><span data-stu-id="40590-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="40590-128">Это значение должно равняться числу пространственных измерений (Инпуттенсор DimensionCount-2).</span><span class="sxs-lookup"><span data-stu-id="40590-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="40590-129">Так как этот оператор поддерживает только не4dные десятки, единственное допустимое значение для этого параметра равно 2.</span><span class="sxs-lookup"><span data-stu-id="40590-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="40590-130">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="40590-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="40590-131">См. *шаг* в [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="40590-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="40590-132">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="40590-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="40590-133">См. раздел *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="40590-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="40590-134">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="40590-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="40590-135">См. раздел *стартпаддинг* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="40590-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="40590-136">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="40590-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="40590-137">См. раздел *ендпаддинг* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="40590-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="40590-138">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="40590-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="40590-139">См. раздел *дилатионс* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="40590-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="40590-140">Доступность</span><span class="sxs-lookup"><span data-stu-id="40590-140">Availability</span></span>
<span data-ttu-id="40590-141">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="40590-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="40590-142">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="40590-142">Tensor constraints</span></span>
* <span data-ttu-id="40590-143">*Инпуттенсор* и *аутпутградиенттенсор* должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="40590-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="40590-144">*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="40590-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="40590-145">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="40590-145">Tensor support</span></span>
| <span data-ttu-id="40590-146">Тензорные</span><span class="sxs-lookup"><span data-stu-id="40590-146">Tensor</span></span> | <span data-ttu-id="40590-147">Вид</span><span class="sxs-lookup"><span data-stu-id="40590-147">Kind</span></span> | <span data-ttu-id="40590-148">Измерения</span><span class="sxs-lookup"><span data-stu-id="40590-148">Dimensions</span></span> | <span data-ttu-id="40590-149">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="40590-149">Supported dimension counts</span></span> | <span data-ttu-id="40590-150">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="40590-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="40590-151">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="40590-151">InputTensor</span></span> | <span data-ttu-id="40590-152">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40590-152">Input</span></span> | <span data-ttu-id="40590-153">{Батчкаунт, Чаннелкаунт, Инпусеигхт, Инпутвидс}</span><span class="sxs-lookup"><span data-stu-id="40590-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="40590-154">4</span><span class="sxs-lookup"><span data-stu-id="40590-154">4</span></span> | <span data-ttu-id="40590-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="40590-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="40590-156">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="40590-156">InputGradientTensor</span></span> | <span data-ttu-id="40590-157">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40590-157">Input</span></span> | <span data-ttu-id="40590-158">{Батчкаунт, Чаннелкаунт, Аутпусеигхт, Аутпутвидс}</span><span class="sxs-lookup"><span data-stu-id="40590-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="40590-159">4</span><span class="sxs-lookup"><span data-stu-id="40590-159">4</span></span> | <span data-ttu-id="40590-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="40590-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="40590-161">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="40590-161">OutputGradientTensor</span></span> | <span data-ttu-id="40590-162">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="40590-162">Output</span></span> | <span data-ttu-id="40590-163">{Батчкаунт, Чаннелкаунт, Инпусеигхт, Инпутвидс}</span><span class="sxs-lookup"><span data-stu-id="40590-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="40590-164">4</span><span class="sxs-lookup"><span data-stu-id="40590-164">4</span></span> | <span data-ttu-id="40590-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="40590-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="40590-166">Требования</span><span class="sxs-lookup"><span data-stu-id="40590-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="40590-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="40590-167">**Header**</span></span> | <span data-ttu-id="40590-168">директмл. h</span><span class="sxs-lookup"><span data-stu-id="40590-168">directml.h</span></span> |