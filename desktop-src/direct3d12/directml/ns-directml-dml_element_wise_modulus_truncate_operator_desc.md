---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Рассчитывает оператор модуля C для каждой пары соответствующих элементов входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: f7cbfbf8613fb4309c6d336ccd807565d0dae53c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719903"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="fb307-103">Структура DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="fb307-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="fb307-104">Рассчитывает оператор модуля C для каждой пары соответствующих элементов входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="fb307-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="fb307-105">Так как значение частного округляется в сторону 0, результат будет иметь тот же знак, что и делимое.</span><span class="sxs-lookup"><span data-stu-id="fb307-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="fb307-106">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="fb307-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb307-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="fb307-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="fb307-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fb307-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb307-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb307-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="fb307-110">Члены</span><span class="sxs-lookup"><span data-stu-id="fb307-110">Members</span></span>

`ATensor`

<span data-ttu-id="fb307-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fb307-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fb307-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="fb307-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="fb307-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fb307-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fb307-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="fb307-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="fb307-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fb307-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fb307-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="fb307-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="fb307-117">Доступность</span><span class="sxs-lookup"><span data-stu-id="fb307-117">Availability</span></span>
<span data-ttu-id="fb307-118">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fb307-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fb307-119">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="fb307-119">Tensor constraints</span></span>
<span data-ttu-id="fb307-120">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="fb307-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fb307-121">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="fb307-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="fb307-122">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="fb307-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="fb307-123">Тензорные</span><span class="sxs-lookup"><span data-stu-id="fb307-123">Tensor</span></span> | <span data-ttu-id="fb307-124">Вид</span><span class="sxs-lookup"><span data-stu-id="fb307-124">Kind</span></span> | <span data-ttu-id="fb307-125">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="fb307-125">Supported dimension counts</span></span> | <span data-ttu-id="fb307-126">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="fb307-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fb307-127">атенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-127">ATensor</span></span> | <span data-ttu-id="fb307-128">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-128">Input</span></span> | <span data-ttu-id="fb307-129">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fb307-129">1 to 8</span></span> | <span data-ttu-id="fb307-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fb307-131">бтенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-131">BTensor</span></span> | <span data-ttu-id="fb307-132">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-132">Input</span></span> | <span data-ttu-id="fb307-133">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fb307-133">1 to 8</span></span> | <span data-ttu-id="fb307-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fb307-135">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-135">OutputTensor</span></span> | <span data-ttu-id="fb307-136">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-136">Output</span></span> | <span data-ttu-id="fb307-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="fb307-137">1 to 8</span></span> | <span data-ttu-id="fb307-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="fb307-139">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="fb307-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="fb307-140">Тензорные</span><span class="sxs-lookup"><span data-stu-id="fb307-140">Tensor</span></span> | <span data-ttu-id="fb307-141">Вид</span><span class="sxs-lookup"><span data-stu-id="fb307-141">Kind</span></span> | <span data-ttu-id="fb307-142">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="fb307-142">Supported dimension counts</span></span> | <span data-ttu-id="fb307-143">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="fb307-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fb307-144">атенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-144">ATensor</span></span> | <span data-ttu-id="fb307-145">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-145">Input</span></span> | <span data-ttu-id="fb307-146">4</span><span class="sxs-lookup"><span data-stu-id="fb307-146">4</span></span> | <span data-ttu-id="fb307-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fb307-148">бтенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-148">BTensor</span></span> | <span data-ttu-id="fb307-149">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-149">Input</span></span> | <span data-ttu-id="fb307-150">4</span><span class="sxs-lookup"><span data-stu-id="fb307-150">4</span></span> | <span data-ttu-id="fb307-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="fb307-152">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="fb307-152">OutputTensor</span></span> | <span data-ttu-id="fb307-153">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="fb307-153">Output</span></span> | <span data-ttu-id="fb307-154">4</span><span class="sxs-lookup"><span data-stu-id="fb307-154">4</span></span> | <span data-ttu-id="fb307-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="fb307-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fb307-156">Требования</span><span class="sxs-lookup"><span data-stu-id="fb307-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fb307-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="fb307-157">**Header**</span></span> | <span data-ttu-id="fb307-158">директмл. h</span><span class="sxs-lookup"><span data-stu-id="fb307-158">directml.h</span></span> |