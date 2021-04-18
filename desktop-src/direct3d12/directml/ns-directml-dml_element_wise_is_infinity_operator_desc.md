---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Проверяет каждый элемент *инпуттенсор* для IEEE-754-INF, INF или обоих параметров в зависимости от заданной *инфинитимоде* и помещает результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: b4f3f07fcbe303e86b422206a8f07eb75fb09d70
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719905"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="ca5ae-103">Структура DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="ca5ae-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="ca5ae-104">Проверяет каждый элемент *инпуттенсор* для IEEE-754-INF, INF или обоих параметров в зависимости от заданной *инфинитимоде* и помещает результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="ca5ae-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="ca5ae-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ca5ae-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ca5ae-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca5ae-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="ca5ae-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ca5ae-108">Members</span></span>

`InputTensor`

<span data-ttu-id="ca5ae-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca5ae-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca5ae-110">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="ca5ae-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca5ae-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca5ae-112">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="ca5ae-113">Тип: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="ca5ae-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="ca5ae-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) , определяющий знак бесконечности для проверки.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="ca5ae-115">Если **DML_IS_INFINITY_MODE_EITHER**, возвращается значение 1, если элемент имеет значение-INF или INF; в противном случае — значение 0.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="ca5ae-116">Если **DML_IS_INFINITY_MODE_POSITIVE**, то возвращается значение 1, если элемент является INF, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="ca5ae-117">Если **DML_IS_INFINITY_MODE_NEGATIVE**", то возвращается значение 1, если элемент имеет значение-INF; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="ca5ae-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca5ae-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="ca5ae-119">Доступность</span><span class="sxs-lookup"><span data-stu-id="ca5ae-119">Availability</span></span>
<span data-ttu-id="ca5ae-120">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ca5ae-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ca5ae-121">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-121">Tensor constraints</span></span>
<span data-ttu-id="ca5ae-122">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="ca5ae-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ca5ae-123">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="ca5ae-124">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="ca5ae-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="ca5ae-125">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-125">Tensor</span></span> | <span data-ttu-id="ca5ae-126">Вид</span><span class="sxs-lookup"><span data-stu-id="ca5ae-126">Kind</span></span> | <span data-ttu-id="ca5ae-127">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ca5ae-127">Supported dimension counts</span></span> | <span data-ttu-id="ca5ae-128">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ca5ae-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ca5ae-129">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ca5ae-129">InputTensor</span></span> | <span data-ttu-id="ca5ae-130">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-130">Input</span></span> | <span data-ttu-id="ca5ae-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="ca5ae-131">1 to 8</span></span> | <span data-ttu-id="ca5ae-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca5ae-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ca5ae-133">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ca5ae-133">OutputTensor</span></span> | <span data-ttu-id="ca5ae-134">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-134">Output</span></span> | <span data-ttu-id="ca5ae-135">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="ca5ae-135">1 to 8</span></span> | <span data-ttu-id="ca5ae-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="ca5ae-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="ca5ae-137">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="ca5ae-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="ca5ae-138">Тензорные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-138">Tensor</span></span> | <span data-ttu-id="ca5ae-139">Вид</span><span class="sxs-lookup"><span data-stu-id="ca5ae-139">Kind</span></span> | <span data-ttu-id="ca5ae-140">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="ca5ae-140">Supported dimension counts</span></span> | <span data-ttu-id="ca5ae-141">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="ca5ae-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ca5ae-142">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ca5ae-142">InputTensor</span></span> | <span data-ttu-id="ca5ae-143">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-143">Input</span></span> | <span data-ttu-id="ca5ae-144">4</span><span class="sxs-lookup"><span data-stu-id="ca5ae-144">4</span></span> | <span data-ttu-id="ca5ae-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ca5ae-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ca5ae-146">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="ca5ae-146">OutputTensor</span></span> | <span data-ttu-id="ca5ae-147">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="ca5ae-147">Output</span></span> | <span data-ttu-id="ca5ae-148">4</span><span class="sxs-lookup"><span data-stu-id="ca5ae-148">4</span></span> | <span data-ttu-id="ca5ae-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="ca5ae-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="ca5ae-150">Требования</span><span class="sxs-lookup"><span data-stu-id="ca5ae-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ca5ae-151">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="ca5ae-151">**Minimum supported client**</span></span> | <span data-ttu-id="ca5ae-152">Windows 10, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="ca5ae-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="ca5ae-153">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="ca5ae-153">**Minimum supported server**</span></span> | <span data-ttu-id="ca5ae-154">Windows Server, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="ca5ae-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="ca5ae-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="ca5ae-155">**Header**</span></span> | <span data-ttu-id="ca5ae-156">директмл. h</span><span class="sxs-lookup"><span data-stu-id="ca5ae-156">directml.h</span></span> |