---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для [элемента, ориентированного на элемент](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804493"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="b429f-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="b429f-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="b429f-104">Вычисление градиентов обратного распространения для [элемента, ориентированного на элемент](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b429f-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="b429f-105">Этот оператор поддерживает выполнение на месте, что означает, что в `OutputTensor` процессе привязки допускается псевдоним *инпуттенсор* .</span><span class="sxs-lookup"><span data-stu-id="b429f-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b429f-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="b429f-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="b429f-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b429f-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b429f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b429f-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="b429f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b429f-109">Members</span></span>

`InputTensor`

<span data-ttu-id="b429f-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b429f-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b429f-111">Входная функция тензорные.</span><span class="sxs-lookup"><span data-stu-id="b429f-111">The input feature tensor.</span></span> <span data-ttu-id="b429f-112">Обычно это те же тензорные, которые были предоставлены в качестве *инпуттенсор* для [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="b429f-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="b429f-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b429f-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b429f-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="b429f-114">The incoming gradient tensor.</span></span> <span data-ttu-id="b429f-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="b429f-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b429f-116">Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего **DML_OPERATOR_ELEMENT_WISE_CLIP** в рамках прямого прохода.</span><span class="sxs-lookup"><span data-stu-id="b429f-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b429f-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b429f-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b429f-118">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="b429f-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b429f-119">Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего **DML_OPERATOR_ELEMENT_WISE_CLIP** в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="b429f-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="b429f-120">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b429f-120">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b429f-121">Минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="b429f-121">The minimum value.</span></span> <span data-ttu-id="b429f-122">Если x находится в или ниже этого значения, то результат градиента равен 0.</span><span class="sxs-lookup"><span data-stu-id="b429f-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="b429f-123">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b429f-123">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b429f-124">Максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="b429f-124">The maximum value.</span></span> <span data-ttu-id="b429f-125">Если x находится в или выше этого значения, градиентный результат равен 0.</span><span class="sxs-lookup"><span data-stu-id="b429f-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="b429f-126">Доступность</span><span class="sxs-lookup"><span data-stu-id="b429f-126">Availability</span></span>
<span data-ttu-id="b429f-127">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="b429f-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b429f-128">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="b429f-128">Tensor constraints</span></span>
<span data-ttu-id="b429f-129">*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="b429f-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b429f-130">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="b429f-130">Tensor support</span></span>
| <span data-ttu-id="b429f-131">Тензорные</span><span class="sxs-lookup"><span data-stu-id="b429f-131">Tensor</span></span> | <span data-ttu-id="b429f-132">Вид</span><span class="sxs-lookup"><span data-stu-id="b429f-132">Kind</span></span> | <span data-ttu-id="b429f-133">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="b429f-133">Supported dimension counts</span></span> | <span data-ttu-id="b429f-134">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="b429f-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b429f-135">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="b429f-135">InputTensor</span></span> | <span data-ttu-id="b429f-136">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b429f-136">Input</span></span> | <span data-ttu-id="b429f-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="b429f-137">1 to 8</span></span> | <span data-ttu-id="b429f-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b429f-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b429f-139">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="b429f-139">InputGradientTensor</span></span> | <span data-ttu-id="b429f-140">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b429f-140">Input</span></span> | <span data-ttu-id="b429f-141">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="b429f-141">1 to 8</span></span> | <span data-ttu-id="b429f-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b429f-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b429f-143">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="b429f-143">OutputGradientTensor</span></span> | <span data-ttu-id="b429f-144">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b429f-144">Output</span></span> | <span data-ttu-id="b429f-145">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="b429f-145">1 to 8</span></span> | <span data-ttu-id="b429f-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b429f-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b429f-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b429f-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b429f-148">**Header**</span><span class="sxs-lookup"><span data-stu-id="b429f-148">**Header**</span></span> | <span data-ttu-id="b429f-149">директмл. h</span><span class="sxs-lookup"><span data-stu-id="b429f-149">directml.h</span></span> |
