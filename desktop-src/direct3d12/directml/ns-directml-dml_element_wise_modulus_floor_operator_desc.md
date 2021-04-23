---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Выполняет вычисление модуля с теми же результатами, что и у модуля Python, для каждой пары соответствующих элементов из входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803071"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="48e13-103">Структура DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="48e13-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="48e13-104">Выполняет вычисление модуля с теми же результатами, что и у модуля Python, для каждой пары соответствующих элементов из входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="48e13-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="48e13-105">Так как значение частного округляется в сторону-INF, результат будет иметь тот же знак, что и делитель.</span><span class="sxs-lookup"><span data-stu-id="48e13-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="48e13-106">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="48e13-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48e13-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="48e13-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="48e13-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="48e13-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="48e13-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48e13-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="48e13-110">Члены</span><span class="sxs-lookup"><span data-stu-id="48e13-110">Members</span></span>

`ATensor`

<span data-ttu-id="48e13-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="48e13-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="48e13-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="48e13-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="48e13-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="48e13-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="48e13-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="48e13-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="48e13-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="48e13-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="48e13-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="48e13-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="48e13-117">Доступность</span><span class="sxs-lookup"><span data-stu-id="48e13-117">Availability</span></span>
<span data-ttu-id="48e13-118">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="48e13-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="48e13-119">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="48e13-119">Tensor constraints</span></span>
<span data-ttu-id="48e13-120">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="48e13-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="48e13-121">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="48e13-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="48e13-122">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="48e13-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="48e13-123">Тензорные</span><span class="sxs-lookup"><span data-stu-id="48e13-123">Tensor</span></span> | <span data-ttu-id="48e13-124">Вид</span><span class="sxs-lookup"><span data-stu-id="48e13-124">Kind</span></span> | <span data-ttu-id="48e13-125">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="48e13-125">Supported dimension counts</span></span> | <span data-ttu-id="48e13-126">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="48e13-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="48e13-127">атенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-127">ATensor</span></span> | <span data-ttu-id="48e13-128">Входные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-128">Input</span></span> | <span data-ttu-id="48e13-129">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="48e13-129">1 to 8</span></span> | <span data-ttu-id="48e13-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="48e13-131">бтенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-131">BTensor</span></span> | <span data-ttu-id="48e13-132">Входные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-132">Input</span></span> | <span data-ttu-id="48e13-133">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="48e13-133">1 to 8</span></span> | <span data-ttu-id="48e13-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="48e13-135">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-135">OutputTensor</span></span> | <span data-ttu-id="48e13-136">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-136">Output</span></span> | <span data-ttu-id="48e13-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="48e13-137">1 to 8</span></span> | <span data-ttu-id="48e13-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="48e13-139">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="48e13-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="48e13-140">Тензорные</span><span class="sxs-lookup"><span data-stu-id="48e13-140">Tensor</span></span> | <span data-ttu-id="48e13-141">Вид</span><span class="sxs-lookup"><span data-stu-id="48e13-141">Kind</span></span> | <span data-ttu-id="48e13-142">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="48e13-142">Supported dimension counts</span></span> | <span data-ttu-id="48e13-143">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="48e13-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="48e13-144">атенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-144">ATensor</span></span> | <span data-ttu-id="48e13-145">Входные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-145">Input</span></span> | <span data-ttu-id="48e13-146">4</span><span class="sxs-lookup"><span data-stu-id="48e13-146">4</span></span> | <span data-ttu-id="48e13-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="48e13-148">бтенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-148">BTensor</span></span> | <span data-ttu-id="48e13-149">Входные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-149">Input</span></span> | <span data-ttu-id="48e13-150">4</span><span class="sxs-lookup"><span data-stu-id="48e13-150">4</span></span> | <span data-ttu-id="48e13-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="48e13-152">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="48e13-152">OutputTensor</span></span> | <span data-ttu-id="48e13-153">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="48e13-153">Output</span></span> | <span data-ttu-id="48e13-154">4</span><span class="sxs-lookup"><span data-stu-id="48e13-154">4</span></span> | <span data-ttu-id="48e13-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="48e13-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="48e13-156">Требования</span><span class="sxs-lookup"><span data-stu-id="48e13-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="48e13-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="48e13-157">**Header**</span></span> | <span data-ttu-id="48e13-158">директмл. h</span><span class="sxs-lookup"><span data-stu-id="48e13-158">directml.h</span></span> |