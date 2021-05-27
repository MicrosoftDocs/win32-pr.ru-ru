---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для [нормализации локальных ответов](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: e858b8ce20df4b1bf12ac9efe360941eb93c54d1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550409"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="5b8e9-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="5b8e9-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="5b8e9-104">Вычисление градиентов обратного распространения для [нормализации локальных ответов](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5b8e9-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="5b8e9-105">Тип данных и размер всех десятков должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b8e9-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="5b8e9-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="5b8e9-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e9-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8e9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b8e9-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="5b8e9-109">Участники</span><span class="sxs-lookup"><span data-stu-id="5b8e9-109">Members</span></span>

`InputTensor`

<span data-ttu-id="5b8e9-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b8e9-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b8e9-111">Тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-111">The tensor containing the input data.</span></span> <span data-ttu-id="5b8e9-112">*Размеры* тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="5b8e9-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="5b8e9-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b8e9-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b8e9-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-114">The incoming gradient tensor.</span></span> <span data-ttu-id="5b8e9-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="5b8e9-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b8e9-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b8e9-117">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="5b8e9-118">Тип: **[bool](../../winprog/windows-data-types.md) .**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-118">Type: **[BOOL](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b8e9-119">**Значение true** , если уровень ЛРН по каналам; **Значение false** , если ЛРН уровень в пространственных измерениях.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="5b8e9-120">Тип: **[uint](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-120">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b8e9-121">Максимальное число элементов для суммирования по измерению (локальная область обрезается таким образом, что все элементы находятся в границах).</span><span class="sxs-lookup"><span data-stu-id="5b8e9-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="5b8e9-122">Если *кроссчаннел* имеет **значение true**, то это ширина и высота локальной области.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="5b8e9-123">Если *кроссчаннел* имеет **значение false**, то это число элементов в локальном регионе.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="5b8e9-124">Минимальное значение — 1.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="5b8e9-125">Тип: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-125">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b8e9-126">Значение параметра масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-126">The value of the scaling parameter.</span></span> <span data-ttu-id="5b8e9-127">В качестве значения по умолчанию рекомендуется использовать значение 0,0001.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="5b8e9-128">Тип: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-128">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b8e9-129">Значение экспоненты.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-129">The value of the exponent.</span></span> <span data-ttu-id="5b8e9-130">В качестве значения по умолчанию рекомендуется использовать значение 0,75.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="5b8e9-131">Тип: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-131">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b8e9-132">Значение смещения.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-132">The value of bias.</span></span> <span data-ttu-id="5b8e9-133">В качестве значения по умолчанию рекомендуется использовать значение 1.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="5b8e9-134">Доступность</span><span class="sxs-lookup"><span data-stu-id="5b8e9-134">Availability</span></span>
<span data-ttu-id="5b8e9-135">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="5b8e9-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5b8e9-136">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-136">Tensor constraints</span></span>
<span data-ttu-id="5b8e9-137">*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="5b8e9-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5b8e9-138">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-138">Tensor support</span></span>
| <span data-ttu-id="5b8e9-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-139">Tensor</span></span> | <span data-ttu-id="5b8e9-140">Вид</span><span class="sxs-lookup"><span data-stu-id="5b8e9-140">Kind</span></span> | <span data-ttu-id="5b8e9-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="5b8e9-141">Supported dimension counts</span></span> | <span data-ttu-id="5b8e9-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="5b8e9-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5b8e9-143">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="5b8e9-143">InputTensor</span></span> | <span data-ttu-id="5b8e9-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-144">Input</span></span> | <span data-ttu-id="5b8e9-145">4</span><span class="sxs-lookup"><span data-stu-id="5b8e9-145">4</span></span> | <span data-ttu-id="5b8e9-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5b8e9-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5b8e9-147">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="5b8e9-147">InputGradientTensor</span></span> | <span data-ttu-id="5b8e9-148">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-148">Input</span></span> | <span data-ttu-id="5b8e9-149">4</span><span class="sxs-lookup"><span data-stu-id="5b8e9-149">4</span></span> | <span data-ttu-id="5b8e9-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5b8e9-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5b8e9-151">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="5b8e9-151">OutputGradientTensor</span></span> | <span data-ttu-id="5b8e9-152">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="5b8e9-152">Output</span></span> | <span data-ttu-id="5b8e9-153">4</span><span class="sxs-lookup"><span data-stu-id="5b8e9-153">4</span></span> | <span data-ttu-id="5b8e9-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5b8e9-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="5b8e9-155">Требования</span><span class="sxs-lookup"><span data-stu-id="5b8e9-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b8e9-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="5b8e9-156">**Header**</span></span> | <span data-ttu-id="5b8e9-157">директмл. h</span><span class="sxs-lookup"><span data-stu-id="5b8e9-157">directml.h</span></span> |