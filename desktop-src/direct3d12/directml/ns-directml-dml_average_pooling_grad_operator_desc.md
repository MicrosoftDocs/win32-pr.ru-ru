---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Вычисляет градиенты обратного распространения для среднего количества пулов (см. [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 79a43e93f504e8d6f36553a4f672ef7e5845610f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719925"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="030d8-103">Структура DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="030d8-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="030d8-104">Вычисляет градиенты обратного распространения для среднего количества пулов (см. [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="030d8-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="030d8-105">Рассмотрим **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2 без заполнения и шаг 1, который выполняет следующее.</span><span class="sxs-lookup"><span data-stu-id="030d8-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="030d8-106">Каждое окно 2x2 во входном тензорные оценивается как среднее значение для получения одного элемента выходных данных (количество нулей для элементов после края).</span><span class="sxs-lookup"><span data-stu-id="030d8-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="030d8-107">Ниже приведен пример выходных данных **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** , заданных аналогичными параметрами.</span><span class="sxs-lookup"><span data-stu-id="030d8-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="030d8-108">Обратите внимание, что значения в *аутпутградиенттенсор* представляют взвешенные вклады этого элемента в *аутпуттенсор* во время исходного оператора [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) .</span><span class="sxs-lookup"><span data-stu-id="030d8-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="030d8-109">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="030d8-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="030d8-110">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="030d8-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="030d8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="030d8-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="030d8-112">Члены</span><span class="sxs-lookup"><span data-stu-id="030d8-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="030d8-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="030d8-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="030d8-114">The incoming gradient tensor.</span></span> <span data-ttu-id="030d8-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="030d8-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="030d8-116">Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="030d8-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="030d8-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="030d8-118">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="030d8-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="030d8-119">Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="030d8-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="030d8-120">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="030d8-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="030d8-121">Число элементов в массивах *stride*, *WindowSize*, *стартпаддинг* и *ендпаддинг* .</span><span class="sxs-lookup"><span data-stu-id="030d8-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="030d8-122">Это значение должно равняться количеству пространственных измерений.</span><span class="sxs-lookup"><span data-stu-id="030d8-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="030d8-123">Количество пространственных измерений равно 2, если предоставлены десятки или 3, если указаны дополнительные десятки.</span><span class="sxs-lookup"><span data-stu-id="030d8-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="030d8-124">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="030d8-125">См. *шаг* в [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="030d8-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="030d8-126">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="030d8-127">См. раздел *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="030d8-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="030d8-128">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="030d8-129">См. раздел *стартпаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="030d8-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="030d8-130">Тип: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="030d8-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="030d8-131">См. раздел *ендпаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="030d8-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="030d8-132">Тип: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="030d8-132">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="030d8-133">См. раздел *инклудепаддинг* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="030d8-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="030d8-134">Доступность</span><span class="sxs-lookup"><span data-stu-id="030d8-134">Availability</span></span>
<span data-ttu-id="030d8-135">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="030d8-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="030d8-136">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="030d8-136">Tensor constraints</span></span>
<span data-ttu-id="030d8-137">*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="030d8-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="030d8-138">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="030d8-138">Tensor support</span></span>
| <span data-ttu-id="030d8-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="030d8-139">Tensor</span></span> | <span data-ttu-id="030d8-140">Вид</span><span class="sxs-lookup"><span data-stu-id="030d8-140">Kind</span></span> | <span data-ttu-id="030d8-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="030d8-141">Supported dimension counts</span></span> | <span data-ttu-id="030d8-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="030d8-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="030d8-143">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="030d8-143">InputGradientTensor</span></span> | <span data-ttu-id="030d8-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="030d8-144">Input</span></span> | <span data-ttu-id="030d8-145">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="030d8-145">4 to 5</span></span> | <span data-ttu-id="030d8-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="030d8-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="030d8-147">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="030d8-147">OutputGradientTensor</span></span> | <span data-ttu-id="030d8-148">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="030d8-148">Output</span></span> | <span data-ttu-id="030d8-149">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="030d8-149">4 to 5</span></span> | <span data-ttu-id="030d8-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="030d8-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="030d8-151">Требования</span><span class="sxs-lookup"><span data-stu-id="030d8-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="030d8-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="030d8-152">**Header**</span></span> | <span data-ttu-id="030d8-153">директмл. h</span><span class="sxs-lookup"><span data-stu-id="030d8-153">directml.h</span></span> |