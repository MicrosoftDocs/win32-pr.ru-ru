---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Выполняет логическую сдвиг вправо каждого элемента *атенсор* на количество битов, заданное соответствующим элементом *бтенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719977"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="84c5b-103">Структура DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="84c5b-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="84c5b-104">Выполняет логическую сдвиг вправо каждого элемента *атенсор* на количество битов, заданное соответствующим элементом *бтенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="84c5b-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="84c5b-105">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="84c5b-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84c5b-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="84c5b-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="84c5b-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="84c5b-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84c5b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84c5b-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="84c5b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="84c5b-109">Members</span></span>

`ATensor`

<span data-ttu-id="84c5b-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84c5b-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84c5b-111">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="84c5b-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="84c5b-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84c5b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84c5b-113">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="84c5b-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="84c5b-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84c5b-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84c5b-115">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="84c5b-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="84c5b-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="84c5b-116">Availability</span></span>
<span data-ttu-id="84c5b-117">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="84c5b-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="84c5b-118">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="84c5b-118">Tensor constraints</span></span>
<span data-ttu-id="84c5b-119">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="84c5b-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="84c5b-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="84c5b-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="84c5b-121">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="84c5b-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="84c5b-122">Тензорные</span><span class="sxs-lookup"><span data-stu-id="84c5b-122">Tensor</span></span> | <span data-ttu-id="84c5b-123">Вид</span><span class="sxs-lookup"><span data-stu-id="84c5b-123">Kind</span></span> | <span data-ttu-id="84c5b-124">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="84c5b-124">Supported dimension counts</span></span> | <span data-ttu-id="84c5b-125">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="84c5b-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="84c5b-126">атенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-126">ATensor</span></span> | <span data-ttu-id="84c5b-127">Входные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-127">Input</span></span> | <span data-ttu-id="84c5b-128">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="84c5b-128">1 to 8</span></span> | <span data-ttu-id="84c5b-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="84c5b-130">бтенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-130">BTensor</span></span> | <span data-ttu-id="84c5b-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-131">Input</span></span> | <span data-ttu-id="84c5b-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="84c5b-132">1 to 8</span></span> | <span data-ttu-id="84c5b-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="84c5b-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-134">OutputTensor</span></span> | <span data-ttu-id="84c5b-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-135">Output</span></span> | <span data-ttu-id="84c5b-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="84c5b-136">1 to 8</span></span> | <span data-ttu-id="84c5b-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="84c5b-138">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="84c5b-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="84c5b-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="84c5b-139">Tensor</span></span> | <span data-ttu-id="84c5b-140">Вид</span><span class="sxs-lookup"><span data-stu-id="84c5b-140">Kind</span></span> | <span data-ttu-id="84c5b-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="84c5b-141">Supported dimension counts</span></span> | <span data-ttu-id="84c5b-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="84c5b-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="84c5b-143">атенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-143">ATensor</span></span> | <span data-ttu-id="84c5b-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-144">Input</span></span> | <span data-ttu-id="84c5b-145">4</span><span class="sxs-lookup"><span data-stu-id="84c5b-145">4</span></span> | <span data-ttu-id="84c5b-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="84c5b-147">бтенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-147">BTensor</span></span> | <span data-ttu-id="84c5b-148">Входные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-148">Input</span></span> | <span data-ttu-id="84c5b-149">4</span><span class="sxs-lookup"><span data-stu-id="84c5b-149">4</span></span> | <span data-ttu-id="84c5b-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="84c5b-151">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="84c5b-151">OutputTensor</span></span> | <span data-ttu-id="84c5b-152">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="84c5b-152">Output</span></span> | <span data-ttu-id="84c5b-153">4</span><span class="sxs-lookup"><span data-stu-id="84c5b-153">4</span></span> | <span data-ttu-id="84c5b-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="84c5b-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="84c5b-155">Требования</span><span class="sxs-lookup"><span data-stu-id="84c5b-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="84c5b-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="84c5b-156">**Header**</span></span> | <span data-ttu-id="84c5b-157">директмл. h</span><span class="sxs-lookup"><span data-stu-id="84c5b-157">directml.h</span></span> |