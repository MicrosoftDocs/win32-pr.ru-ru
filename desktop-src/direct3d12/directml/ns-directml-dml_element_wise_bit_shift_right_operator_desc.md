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
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803200"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="fe0a8-103">Структура DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="fe0a8-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fe0a8-104">Выполняет логическую сдвиг вправо каждого элемента *атенсор* на количество битов, заданное соответствующим элементом *бтенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="fe0a8-105">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe0a8-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="fe0a8-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="fe0a8-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fe0a8-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe0a8-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="fe0a8-109">Члены</span><span class="sxs-lookup"><span data-stu-id="fe0a8-109">Members</span></span>

`ATensor`

<span data-ttu-id="fe0a8-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe0a8-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe0a8-111">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="fe0a8-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe0a8-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe0a8-113">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="fe0a8-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe0a8-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe0a8-115">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="fe0a8-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="fe0a8-116">Availability</span></span>
<span data-ttu-id="fe0a8-117">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fe0a8-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fe0a8-118">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-118">Tensor constraints</span></span>
<span data-ttu-id="fe0a8-119">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="fe0a8-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fe0a8-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="fe0a8-121">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="fe0a8-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="fe0a8-122">Тензорные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-122">Tensor</span></span> | <span data-ttu-id="fe0a8-123">Вид</span><span class="sxs-lookup"><span data-stu-id="fe0a8-123">Kind</span></span> | <span data-ttu-id="fe0a8-124">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="fe0a8-124">Supported dimension counts</span></span> | <span data-ttu-id="fe0a8-125">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="fe0a8-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe0a8-126">атенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-126">ATensor</span></span> | <span data-ttu-id="fe0a8-127">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-127">Input</span></span> | <span data-ttu-id="fe0a8-128">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-128">1 to 8</span></span> | <span data-ttu-id="fe0a8-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe0a8-130">бтенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-130">BTensor</span></span> | <span data-ttu-id="fe0a8-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-131">Input</span></span> | <span data-ttu-id="fe0a8-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-132">1 to 8</span></span> | <span data-ttu-id="fe0a8-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe0a8-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-134">OutputTensor</span></span> | <span data-ttu-id="fe0a8-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-135">Output</span></span> | <span data-ttu-id="fe0a8-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-136">1 to 8</span></span> | <span data-ttu-id="fe0a8-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="fe0a8-138">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="fe0a8-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="fe0a8-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-139">Tensor</span></span> | <span data-ttu-id="fe0a8-140">Вид</span><span class="sxs-lookup"><span data-stu-id="fe0a8-140">Kind</span></span> | <span data-ttu-id="fe0a8-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="fe0a8-141">Supported dimension counts</span></span> | <span data-ttu-id="fe0a8-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="fe0a8-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe0a8-143">атенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-143">ATensor</span></span> | <span data-ttu-id="fe0a8-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-144">Input</span></span> | <span data-ttu-id="fe0a8-145">4</span><span class="sxs-lookup"><span data-stu-id="fe0a8-145">4</span></span> | <span data-ttu-id="fe0a8-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe0a8-147">бтенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-147">BTensor</span></span> | <span data-ttu-id="fe0a8-148">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-148">Input</span></span> | <span data-ttu-id="fe0a8-149">4</span><span class="sxs-lookup"><span data-stu-id="fe0a8-149">4</span></span> | <span data-ttu-id="fe0a8-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fe0a8-151">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="fe0a8-151">OutputTensor</span></span> | <span data-ttu-id="fe0a8-152">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="fe0a8-152">Output</span></span> | <span data-ttu-id="fe0a8-153">4</span><span class="sxs-lookup"><span data-stu-id="fe0a8-153">4</span></span> | <span data-ttu-id="fe0a8-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fe0a8-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fe0a8-155">Требования</span><span class="sxs-lookup"><span data-stu-id="fe0a8-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe0a8-156">**Header**</span><span class="sxs-lookup"><span data-stu-id="fe0a8-156">**Header**</span></span> | <span data-ttu-id="fe0a8-157">директмл. h</span><span class="sxs-lookup"><span data-stu-id="fe0a8-157">directml.h</span></span> |