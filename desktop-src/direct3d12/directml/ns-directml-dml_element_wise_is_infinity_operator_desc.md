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
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803096"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="86255-103">Структура DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="86255-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="86255-104">Проверяет каждый элемент *инпуттенсор* для IEEE-754-INF, INF или обоих параметров в зависимости от заданной *инфинитимоде* и помещает результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="86255-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="86255-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="86255-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="86255-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="86255-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86255-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86255-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="86255-108">Члены</span><span class="sxs-lookup"><span data-stu-id="86255-108">Members</span></span>

`InputTensor`

<span data-ttu-id="86255-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="86255-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="86255-110">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="86255-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="86255-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="86255-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="86255-112">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="86255-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="86255-113">Тип: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="86255-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="86255-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) , определяющий знак бесконечности для проверки.</span><span class="sxs-lookup"><span data-stu-id="86255-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="86255-115">Если **DML_IS_INFINITY_MODE_EITHER**, возвращается значение 1, если элемент имеет значение-INF или INF; в противном случае — значение 0.</span><span class="sxs-lookup"><span data-stu-id="86255-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="86255-116">Если **DML_IS_INFINITY_MODE_POSITIVE**, то возвращается значение 1, если элемент является INF, в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="86255-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="86255-117">Если **DML_IS_INFINITY_MODE_NEGATIVE**", то возвращается значение 1, если элемент имеет значение-INF; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="86255-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="86255-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86255-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="86255-119">Доступность</span><span class="sxs-lookup"><span data-stu-id="86255-119">Availability</span></span>
<span data-ttu-id="86255-120">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="86255-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="86255-121">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="86255-121">Tensor constraints</span></span>
<span data-ttu-id="86255-122">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="86255-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="86255-123">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="86255-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="86255-124">DML_FEATURE_LEVEL_3_0 и выше</span><span class="sxs-lookup"><span data-stu-id="86255-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="86255-125">Тензорные</span><span class="sxs-lookup"><span data-stu-id="86255-125">Tensor</span></span> | <span data-ttu-id="86255-126">Вид</span><span class="sxs-lookup"><span data-stu-id="86255-126">Kind</span></span> | <span data-ttu-id="86255-127">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="86255-127">Supported dimension counts</span></span> | <span data-ttu-id="86255-128">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="86255-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="86255-129">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="86255-129">InputTensor</span></span> | <span data-ttu-id="86255-130">Входные данные</span><span class="sxs-lookup"><span data-stu-id="86255-130">Input</span></span> | <span data-ttu-id="86255-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="86255-131">1 to 8</span></span> | <span data-ttu-id="86255-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="86255-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="86255-133">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="86255-133">OutputTensor</span></span> | <span data-ttu-id="86255-134">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="86255-134">Output</span></span> | <span data-ttu-id="86255-135">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="86255-135">1 to 8</span></span> | <span data-ttu-id="86255-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="86255-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="86255-137">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="86255-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="86255-138">Тензорные</span><span class="sxs-lookup"><span data-stu-id="86255-138">Tensor</span></span> | <span data-ttu-id="86255-139">Вид</span><span class="sxs-lookup"><span data-stu-id="86255-139">Kind</span></span> | <span data-ttu-id="86255-140">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="86255-140">Supported dimension counts</span></span> | <span data-ttu-id="86255-141">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="86255-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="86255-142">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="86255-142">InputTensor</span></span> | <span data-ttu-id="86255-143">Входные данные</span><span class="sxs-lookup"><span data-stu-id="86255-143">Input</span></span> | <span data-ttu-id="86255-144">4</span><span class="sxs-lookup"><span data-stu-id="86255-144">4</span></span> | <span data-ttu-id="86255-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="86255-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="86255-146">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="86255-146">OutputTensor</span></span> | <span data-ttu-id="86255-147">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="86255-147">Output</span></span> | <span data-ttu-id="86255-148">4</span><span class="sxs-lookup"><span data-stu-id="86255-148">4</span></span> | <span data-ttu-id="86255-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="86255-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="86255-150">Требования</span><span class="sxs-lookup"><span data-stu-id="86255-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="86255-151">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="86255-151">**Minimum supported client**</span></span> | <span data-ttu-id="86255-152">Windows 10, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="86255-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="86255-153">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="86255-153">**Minimum supported server**</span></span> | <span data-ttu-id="86255-154">Windows Server, версия 2004 (10,0; Сборка 19041)</span><span class="sxs-lookup"><span data-stu-id="86255-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="86255-155">**Header**</span><span class="sxs-lookup"><span data-stu-id="86255-155">**Header**</span></span> | <span data-ttu-id="86255-156">директмл. h</span><span class="sxs-lookup"><span data-stu-id="86255-156">directml.h</span></span> |