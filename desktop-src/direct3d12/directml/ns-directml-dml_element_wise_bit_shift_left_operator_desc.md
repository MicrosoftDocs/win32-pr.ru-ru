---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
description: Выполняет логическую операцию сдвига влево каждого элемента *атенсор* на количество битов, заданное соответствующим элементом *бтенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_left_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC
ms.openlocfilehash: 993e8f2969752c8e2133f685685d69942c77b506
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417629"
---
# <a name="dml_element_wise_bit_shift_left_operator_desc-structure-directmlh"></a><span data-ttu-id="bfa45-103">Структура DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="bfa45-103">DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bfa45-104">Выполняет логическую операцию сдвига влево каждого элемента *атенсор* на количество битов, заданное соответствующим элементом *бтенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="bfa45-104">Performs a logical left shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a << b)
```

<span data-ttu-id="bfa45-105">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="bfa45-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfa45-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="bfa45-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bfa45-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bfa45-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa45-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfa45-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_LEFT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="bfa45-109">Участники</span><span class="sxs-lookup"><span data-stu-id="bfa45-109">Members</span></span>

`ATensor`

<span data-ttu-id="bfa45-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bfa45-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bfa45-111">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="bfa45-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="bfa45-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bfa45-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bfa45-113">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="bfa45-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="bfa45-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bfa45-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bfa45-115">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="bfa45-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="bfa45-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="bfa45-116">Availability</span></span>
<span data-ttu-id="bfa45-117">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="bfa45-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bfa45-118">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="bfa45-118">Tensor constraints</span></span>
<span data-ttu-id="bfa45-119">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="bfa45-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bfa45-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="bfa45-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="bfa45-121">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="bfa45-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="bfa45-122">Тензорные</span><span class="sxs-lookup"><span data-stu-id="bfa45-122">Tensor</span></span> | <span data-ttu-id="bfa45-123">Вид</span><span class="sxs-lookup"><span data-stu-id="bfa45-123">Kind</span></span> | <span data-ttu-id="bfa45-124">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="bfa45-124">Supported dimension counts</span></span> | <span data-ttu-id="bfa45-125">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="bfa45-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bfa45-126">атенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-126">ATensor</span></span> | <span data-ttu-id="bfa45-127">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-127">Input</span></span> | <span data-ttu-id="bfa45-128">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="bfa45-128">1 to 8</span></span> | <span data-ttu-id="bfa45-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bfa45-130">бтенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-130">BTensor</span></span> | <span data-ttu-id="bfa45-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-131">Input</span></span> | <span data-ttu-id="bfa45-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="bfa45-132">1 to 8</span></span> | <span data-ttu-id="bfa45-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bfa45-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-134">OutputTensor</span></span> | <span data-ttu-id="bfa45-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-135">Output</span></span> | <span data-ttu-id="bfa45-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="bfa45-136">1 to 8</span></span> | <span data-ttu-id="bfa45-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="bfa45-138">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="bfa45-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="bfa45-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="bfa45-139">Tensor</span></span> | <span data-ttu-id="bfa45-140">Вид</span><span class="sxs-lookup"><span data-stu-id="bfa45-140">Kind</span></span> | <span data-ttu-id="bfa45-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="bfa45-141">Supported dimension counts</span></span> | <span data-ttu-id="bfa45-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="bfa45-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bfa45-143">атенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-143">ATensor</span></span> | <span data-ttu-id="bfa45-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-144">Input</span></span> | <span data-ttu-id="bfa45-145">4</span><span class="sxs-lookup"><span data-stu-id="bfa45-145">4</span></span> | <span data-ttu-id="bfa45-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bfa45-147">бтенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-147">BTensor</span></span> | <span data-ttu-id="bfa45-148">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-148">Input</span></span> | <span data-ttu-id="bfa45-149">4</span><span class="sxs-lookup"><span data-stu-id="bfa45-149">4</span></span> | <span data-ttu-id="bfa45-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bfa45-151">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="bfa45-151">OutputTensor</span></span> | <span data-ttu-id="bfa45-152">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="bfa45-152">Output</span></span> | <span data-ttu-id="bfa45-153">4</span><span class="sxs-lookup"><span data-stu-id="bfa45-153">4</span></span> | <span data-ttu-id="bfa45-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bfa45-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="bfa45-155">Требования</span><span class="sxs-lookup"><span data-stu-id="bfa45-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bfa45-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="bfa45-156">**Header**</span></span> | <span data-ttu-id="bfa45-157">директмл. h</span><span class="sxs-lookup"><span data-stu-id="bfa45-157">directml.h</span></span> |