---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Выполняет логическую операцию " *больше или равно* " для каждой пары соответствующих элементов входных десятков, помещая результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 4c20580a67117e6a605dfb0bf6611aca5cfd9e56
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803090"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="137c4-103">Структура DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="137c4-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="137c4-104">Выполняет логическую операцию " *больше или равно* " для каждой пары соответствующих элементов входных десятков, помещая результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="137c4-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="137c4-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="137c4-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="137c4-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="137c4-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="137c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="137c4-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="137c4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="137c4-108">Members</span></span>

`ATensor`

<span data-ttu-id="137c4-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="137c4-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="137c4-110">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="137c4-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="137c4-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="137c4-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="137c4-112">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="137c4-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="137c4-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="137c4-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="137c4-114">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="137c4-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="137c4-115">Доступность</span><span class="sxs-lookup"><span data-stu-id="137c4-115">Availability</span></span>
<span data-ttu-id="137c4-116">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="137c4-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="137c4-117">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="137c4-117">Tensor constraints</span></span>
* <span data-ttu-id="137c4-118">*Атенсор* и *бтенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="137c4-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="137c4-119">*Атенсор*, *бтенсор* и *аутпуттенсор* должны иметь одинаковые *размеры* и *DimensionCount* .</span><span class="sxs-lookup"><span data-stu-id="137c4-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="137c4-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="137c4-120">Tensor support</span></span>
| <span data-ttu-id="137c4-121">Тензорные</span><span class="sxs-lookup"><span data-stu-id="137c4-121">Tensor</span></span> | <span data-ttu-id="137c4-122">Вид</span><span class="sxs-lookup"><span data-stu-id="137c4-122">Kind</span></span> | <span data-ttu-id="137c4-123">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="137c4-123">Supported dimension counts</span></span> | <span data-ttu-id="137c4-124">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="137c4-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="137c4-125">атенсор</span><span class="sxs-lookup"><span data-stu-id="137c4-125">ATensor</span></span> | <span data-ttu-id="137c4-126">Входные данные</span><span class="sxs-lookup"><span data-stu-id="137c4-126">Input</span></span> | <span data-ttu-id="137c4-127">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="137c4-127">1 to 8</span></span> | <span data-ttu-id="137c4-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="137c4-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="137c4-129">бтенсор</span><span class="sxs-lookup"><span data-stu-id="137c4-129">BTensor</span></span> | <span data-ttu-id="137c4-130">Входные данные</span><span class="sxs-lookup"><span data-stu-id="137c4-130">Input</span></span> | <span data-ttu-id="137c4-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="137c4-131">1 to 8</span></span> | <span data-ttu-id="137c4-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="137c4-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="137c4-133">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="137c4-133">OutputTensor</span></span> | <span data-ttu-id="137c4-134">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="137c4-134">Output</span></span> | <span data-ttu-id="137c4-135">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="137c4-135">1 to 8</span></span> | <span data-ttu-id="137c4-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="137c4-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="137c4-137">Требования</span><span class="sxs-lookup"><span data-stu-id="137c4-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="137c4-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="137c4-138">**Header**</span></span> | <span data-ttu-id="137c4-139">директмл. h</span><span class="sxs-lookup"><span data-stu-id="137c4-139">directml.h</span></span> |