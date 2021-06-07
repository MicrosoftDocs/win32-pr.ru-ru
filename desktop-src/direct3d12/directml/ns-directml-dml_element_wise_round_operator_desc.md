---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Округляет каждый элемент *инпуттенсор* в целочисленное значение, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418073"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="1f291-103">Структура DML_ELEMENT_WISE_ROUND_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="1f291-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1f291-104">Округляет каждый элемент *инпуттенсор* в целочисленное значение, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="1f291-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="1f291-105">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдоним *инпуттенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="1f291-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f291-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="1f291-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="1f291-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1f291-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f291-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f291-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="1f291-109">Участники</span><span class="sxs-lookup"><span data-stu-id="1f291-109">Members</span></span>

`InputTensor`

<span data-ttu-id="1f291-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1f291-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1f291-111">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="1f291-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="1f291-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1f291-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1f291-113">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="1f291-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="1f291-114">Тип: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="1f291-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="1f291-115">[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) , определяющее направление, по которому будет направлено округление.</span><span class="sxs-lookup"><span data-stu-id="1f291-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="1f291-116">Если **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: значения округляются до ближайшего целого числа с посредними значениями (например, 0,5), округленными до ближайшего четного целого числа.</span><span class="sxs-lookup"><span data-stu-id="1f291-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="1f291-117">Если **DML_ROUNDING_MODE_TOWARD_ZERO**: значения округляются в сторону нуля.</span><span class="sxs-lookup"><span data-stu-id="1f291-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="1f291-118">Это фактически усекает дробную часть.</span><span class="sxs-lookup"><span data-stu-id="1f291-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="1f291-119">Если **DML_ROUNDING_MODE_TOWARD_INFINITY**: значения округляются до ближайшего целого числа, с посредними значениями (например, 0,5) округляются от нуля (в сторону положительной или отрицательной бесконечности, в зависимости от знака значения).</span><span class="sxs-lookup"><span data-stu-id="1f291-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="1f291-120">Доступность</span><span class="sxs-lookup"><span data-stu-id="1f291-120">Availability</span></span>
<span data-ttu-id="1f291-121">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="1f291-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1f291-122">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="1f291-122">Tensor constraints</span></span>
<span data-ttu-id="1f291-123">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="1f291-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1f291-124">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="1f291-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="1f291-125">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="1f291-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="1f291-126">Тензорные</span><span class="sxs-lookup"><span data-stu-id="1f291-126">Tensor</span></span> | <span data-ttu-id="1f291-127">Вид</span><span class="sxs-lookup"><span data-stu-id="1f291-127">Kind</span></span> | <span data-ttu-id="1f291-128">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="1f291-128">Supported dimension counts</span></span> | <span data-ttu-id="1f291-129">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="1f291-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1f291-130">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="1f291-130">InputTensor</span></span> | <span data-ttu-id="1f291-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1f291-131">Input</span></span> | <span data-ttu-id="1f291-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="1f291-132">1 to 8</span></span> | <span data-ttu-id="1f291-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1f291-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="1f291-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="1f291-134">OutputTensor</span></span> | <span data-ttu-id="1f291-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="1f291-135">Output</span></span> | <span data-ttu-id="1f291-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="1f291-136">1 to 8</span></span> | <span data-ttu-id="1f291-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1f291-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="1f291-138">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="1f291-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="1f291-139">Тензорные</span><span class="sxs-lookup"><span data-stu-id="1f291-139">Tensor</span></span> | <span data-ttu-id="1f291-140">Вид</span><span class="sxs-lookup"><span data-stu-id="1f291-140">Kind</span></span> | <span data-ttu-id="1f291-141">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="1f291-141">Supported dimension counts</span></span> | <span data-ttu-id="1f291-142">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="1f291-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1f291-143">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="1f291-143">InputTensor</span></span> | <span data-ttu-id="1f291-144">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1f291-144">Input</span></span> | <span data-ttu-id="1f291-145">4</span><span class="sxs-lookup"><span data-stu-id="1f291-145">4</span></span> | <span data-ttu-id="1f291-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1f291-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="1f291-147">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="1f291-147">OutputTensor</span></span> | <span data-ttu-id="1f291-148">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="1f291-148">Output</span></span> | <span data-ttu-id="1f291-149">4</span><span class="sxs-lookup"><span data-stu-id="1f291-149">4</span></span> | <span data-ttu-id="1f291-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1f291-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="1f291-151">Требования</span><span class="sxs-lookup"><span data-stu-id="1f291-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1f291-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="1f291-152">**Header**</span></span> | <span data-ttu-id="1f291-153">директмл. h</span><span class="sxs-lookup"><span data-stu-id="1f291-153">directml.h</span></span> |