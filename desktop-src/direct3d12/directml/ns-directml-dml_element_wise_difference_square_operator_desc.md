---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Вычитает каждый элемент из *бтенсор* из соответствующего элемента *атенсор*, умножает результат на себя и помещает результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804483"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="6f53e-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="6f53e-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="6f53e-104">Вычитает каждый элемент из *бтенсор* из соответствующего элемента *атенсор*, умножает результат на себя и помещает результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="6f53e-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="6f53e-105">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может иметь псевдоним *атенсор* или *бтенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="6f53e-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f53e-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="6f53e-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="6f53e-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6f53e-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f53e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f53e-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="6f53e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6f53e-109">Members</span></span>

`ATensor`

<span data-ttu-id="6f53e-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6f53e-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6f53e-111">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="6f53e-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="6f53e-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6f53e-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6f53e-113">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="6f53e-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="6f53e-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6f53e-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6f53e-115">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="6f53e-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="6f53e-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="6f53e-116">Availability</span></span>
<span data-ttu-id="6f53e-117">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="6f53e-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6f53e-118">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="6f53e-118">Tensor constraints</span></span>
<span data-ttu-id="6f53e-119">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="6f53e-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6f53e-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="6f53e-120">Tensor support</span></span>
| <span data-ttu-id="6f53e-121">Тензорные</span><span class="sxs-lookup"><span data-stu-id="6f53e-121">Tensor</span></span> | <span data-ttu-id="6f53e-122">Вид</span><span class="sxs-lookup"><span data-stu-id="6f53e-122">Kind</span></span> | <span data-ttu-id="6f53e-123">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="6f53e-123">Supported dimension counts</span></span> | <span data-ttu-id="6f53e-124">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="6f53e-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6f53e-125">атенсор</span><span class="sxs-lookup"><span data-stu-id="6f53e-125">ATensor</span></span> | <span data-ttu-id="6f53e-126">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6f53e-126">Input</span></span> | <span data-ttu-id="6f53e-127">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="6f53e-127">1 to 8</span></span> | <span data-ttu-id="6f53e-128">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="6f53e-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="6f53e-129">бтенсор</span><span class="sxs-lookup"><span data-stu-id="6f53e-129">BTensor</span></span> | <span data-ttu-id="6f53e-130">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6f53e-130">Input</span></span> | <span data-ttu-id="6f53e-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="6f53e-131">1 to 8</span></span> | <span data-ttu-id="6f53e-132">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="6f53e-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="6f53e-133">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="6f53e-133">OutputTensor</span></span> | <span data-ttu-id="6f53e-134">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="6f53e-134">Output</span></span> | <span data-ttu-id="6f53e-135">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="6f53e-135">1 to 8</span></span> | <span data-ttu-id="6f53e-136">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="6f53e-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="6f53e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="6f53e-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6f53e-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="6f53e-138">**Header**</span></span> | <span data-ttu-id="6f53e-139">директмл. h</span><span class="sxs-lookup"><span data-stu-id="6f53e-139">directml.h</span></span> |
