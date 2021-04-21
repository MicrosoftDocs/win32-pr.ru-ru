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
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804473"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="ce345-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="ce345-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="ce345-104">Вычисление градиентов обратного распространения для [нормализации локальных ответов](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="ce345-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="ce345-105">Тип данных и размер всех десятков должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="ce345-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce345-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="ce345-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="ce345-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ce345-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce345-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce345-108">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="ce345-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ce345-109">Members</span></span>

`InputTensor`

<span data-ttu-id="ce345-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ce345-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ce345-111">Тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="ce345-111">The tensor containing the input data.</span></span> <span data-ttu-id="ce345-112">*Размеры* тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ce345-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="ce345-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ce345-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ce345-114">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="ce345-114">The incoming gradient tensor.</span></span> <span data-ttu-id="ce345-115">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="ce345-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="ce345-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ce345-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ce345-117">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="ce345-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="ce345-118">Тип: **[bool](/windows/win32/winprog/windows-data-types) .**</span><span class="sxs-lookup"><span data-stu-id="ce345-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ce345-119">**Значение true** , если уровень ЛРН по каналам; **Значение false** , если ЛРН уровень в пространственных измерениях.</span><span class="sxs-lookup"><span data-stu-id="ce345-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="ce345-120">Тип: **[uint](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce345-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ce345-121">Максимальное число элементов для суммирования по измерению (локальная область обрезается таким образом, что все элементы находятся в границах).</span><span class="sxs-lookup"><span data-stu-id="ce345-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="ce345-122">Если *кроссчаннел* имеет **значение true**, то это ширина и высота локальной области.</span><span class="sxs-lookup"><span data-stu-id="ce345-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="ce345-123">Если *кроссчаннел* имеет **значение false**, то это число элементов в локальном регионе.</span><span class="sxs-lookup"><span data-stu-id="ce345-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="ce345-124">Минимальное значение — 1.</span><span class="sxs-lookup"><span data-stu-id="ce345-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="ce345-125">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce345-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ce345-126">Значение параметра масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ce345-126">The value of the scaling parameter.</span></span> <span data-ttu-id="ce345-127">В качестве значения по умолчанию рекомендуется использовать значение 0,0001.</span><span class="sxs-lookup"><span data-stu-id="ce345-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="ce345-128">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce345-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ce345-129">Значение экспоненты.</span><span class="sxs-lookup"><span data-stu-id="ce345-129">The value of the exponent.</span></span> <span data-ttu-id="ce345-130">В качестве значения по умолчанию рекомендуется использовать значение 0,75.</span><span class="sxs-lookup"><span data-stu-id="ce345-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="ce345-131">Тип: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce345-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="ce345-132">Значение смещения.</span><span class="sxs-lookup"><span data-stu-id="ce345-132">The value of bias.</span></span> <span data-ttu-id="ce345-133">В качестве значения по умолчанию рекомендуется использовать значение 1.</span><span class="sxs-lookup"><span data-stu-id="ce345-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="ce345-134">Доступность</span><span class="sxs-lookup"><span data-stu-id="ce345-134">Availability</span></span>
<span data-ttu-id="ce345-135">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="ce345-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ce345-136">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="ce345-136">Tensor constraints</span></span>
<span data-ttu-id="ce345-137">*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="ce345-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ce345-138">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="ce345-138">Tensor support</span></span>
| <span data-ttu-id="ce345-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ce345-139">Tensor</span></span> | <span data-ttu-id="ce345-140">Вид</span><span class="sxs-lookup"><span data-stu-id="ce345-140">Kind</span></span> | <span data-ttu-id="ce345-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ce345-141">Supported dimension counts</span></span> | <span data-ttu-id="ce345-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ce345-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ce345-143">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ce345-143">InputTensor</span></span> | <span data-ttu-id="ce345-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce345-144">Input</span></span> | <span data-ttu-id="ce345-145">4</span><span class="sxs-lookup"><span data-stu-id="ce345-145">4</span></span> | <span data-ttu-id="ce345-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ce345-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ce345-147">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="ce345-147">InputGradientTensor</span></span> | <span data-ttu-id="ce345-148">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce345-148">Input</span></span> | <span data-ttu-id="ce345-149">4</span><span class="sxs-lookup"><span data-stu-id="ce345-149">4</span></span> | <span data-ttu-id="ce345-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ce345-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ce345-151">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="ce345-151">OutputGradientTensor</span></span> | <span data-ttu-id="ce345-152">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ce345-152">Output</span></span> | <span data-ttu-id="ce345-153">4</span><span class="sxs-lookup"><span data-stu-id="ce345-153">4</span></span> | <span data-ttu-id="ce345-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ce345-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="ce345-155">Требования</span><span class="sxs-lookup"><span data-stu-id="ce345-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ce345-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="ce345-156">**Header**</span></span> | <span data-ttu-id="ce345-157">директмл. h</span><span class="sxs-lookup"><span data-stu-id="ce345-157">directml.h</span></span> |
