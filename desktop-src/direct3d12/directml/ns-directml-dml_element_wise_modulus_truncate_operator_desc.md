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
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803063"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="62be5-103">Структура DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="62be5-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="62be5-104">Рассчитывает оператор модуля C для каждой пары соответствующих элементов входных десятков, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="62be5-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="62be5-105">Так как значение частного округляется в сторону 0, результат будет иметь тот же знак, что и делимое.</span><span class="sxs-lookup"><span data-stu-id="62be5-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="62be5-106">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдонимы для одного из входных десятков во время привязки.</span><span class="sxs-lookup"><span data-stu-id="62be5-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62be5-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="62be5-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="62be5-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="62be5-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62be5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62be5-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="62be5-110">Члены</span><span class="sxs-lookup"><span data-stu-id="62be5-110">Members</span></span>

`ATensor`

<span data-ttu-id="62be5-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="62be5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="62be5-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="62be5-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="62be5-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="62be5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="62be5-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="62be5-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="62be5-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="62be5-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="62be5-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="62be5-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="62be5-117">Доступность</span><span class="sxs-lookup"><span data-stu-id="62be5-117">Availability</span></span>
<span data-ttu-id="62be5-118">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="62be5-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="62be5-119">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="62be5-119">Tensor constraints</span></span>
<span data-ttu-id="62be5-120">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="62be5-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="62be5-121">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="62be5-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="62be5-122">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="62be5-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="62be5-123">Тензорные</span><span class="sxs-lookup"><span data-stu-id="62be5-123">Tensor</span></span> | <span data-ttu-id="62be5-124">Вид</span><span class="sxs-lookup"><span data-stu-id="62be5-124">Kind</span></span> | <span data-ttu-id="62be5-125">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="62be5-125">Supported dimension counts</span></span> | <span data-ttu-id="62be5-126">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="62be5-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="62be5-127">атенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-127">ATensor</span></span> | <span data-ttu-id="62be5-128">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-128">Input</span></span> | <span data-ttu-id="62be5-129">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="62be5-129">1 to 8</span></span> | <span data-ttu-id="62be5-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="62be5-131">бтенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-131">BTensor</span></span> | <span data-ttu-id="62be5-132">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-132">Input</span></span> | <span data-ttu-id="62be5-133">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="62be5-133">1 to 8</span></span> | <span data-ttu-id="62be5-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="62be5-135">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-135">OutputTensor</span></span> | <span data-ttu-id="62be5-136">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-136">Output</span></span> | <span data-ttu-id="62be5-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="62be5-137">1 to 8</span></span> | <span data-ttu-id="62be5-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="62be5-139">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="62be5-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="62be5-140">Тензорные</span><span class="sxs-lookup"><span data-stu-id="62be5-140">Tensor</span></span> | <span data-ttu-id="62be5-141">Вид</span><span class="sxs-lookup"><span data-stu-id="62be5-141">Kind</span></span> | <span data-ttu-id="62be5-142">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="62be5-142">Supported dimension counts</span></span> | <span data-ttu-id="62be5-143">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="62be5-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="62be5-144">атенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-144">ATensor</span></span> | <span data-ttu-id="62be5-145">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-145">Input</span></span> | <span data-ttu-id="62be5-146">4</span><span class="sxs-lookup"><span data-stu-id="62be5-146">4</span></span> | <span data-ttu-id="62be5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="62be5-148">бтенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-148">BTensor</span></span> | <span data-ttu-id="62be5-149">Входные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-149">Input</span></span> | <span data-ttu-id="62be5-150">4</span><span class="sxs-lookup"><span data-stu-id="62be5-150">4</span></span> | <span data-ttu-id="62be5-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="62be5-152">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="62be5-152">OutputTensor</span></span> | <span data-ttu-id="62be5-153">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="62be5-153">Output</span></span> | <span data-ttu-id="62be5-154">4</span><span class="sxs-lookup"><span data-stu-id="62be5-154">4</span></span> | <span data-ttu-id="62be5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="62be5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="62be5-156">Требования</span><span class="sxs-lookup"><span data-stu-id="62be5-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="62be5-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="62be5-157">**Header**</span></span> | <span data-ttu-id="62be5-158">директмл. h</span><span class="sxs-lookup"><span data-stu-id="62be5-158">directml.h</span></span> |