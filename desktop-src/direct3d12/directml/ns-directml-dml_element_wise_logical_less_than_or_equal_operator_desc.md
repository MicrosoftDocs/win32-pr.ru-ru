---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Выполняет логическую операцию " *меньше или равно* " для каждой пары соответствующих элементов входных десятков, помещая результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 815c7ea148d6754cb410da6aeedaf31ab6cd7ece
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719904"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="e689a-103">Структура DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e689a-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e689a-104">Выполняет логическую операцию " *меньше или равно* " для каждой пары соответствующих элементов входных десятков, помещая результат (1 для true, 0 для false) в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e689a-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="e689a-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e689a-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e689a-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e689a-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e689a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e689a-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e689a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e689a-108">Members</span></span>

`ATensor`

<span data-ttu-id="e689a-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e689a-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e689a-110">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="e689a-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="e689a-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e689a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e689a-112">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="e689a-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="e689a-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e689a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e689a-114">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="e689a-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e689a-115">Доступность</span><span class="sxs-lookup"><span data-stu-id="e689a-115">Availability</span></span>
<span data-ttu-id="e689a-116">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e689a-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e689a-117">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e689a-117">Tensor constraints</span></span>
* <span data-ttu-id="e689a-118">*Атенсор* и *бтенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="e689a-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="e689a-119">*Атенсор*, *бтенсор* и *аутпуттенсор* должны иметь одинаковые *размеры* и *DimensionCount* .</span><span class="sxs-lookup"><span data-stu-id="e689a-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e689a-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e689a-120">Tensor support</span></span>
| <span data-ttu-id="e689a-121">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e689a-121">Tensor</span></span> | <span data-ttu-id="e689a-122">Вид</span><span class="sxs-lookup"><span data-stu-id="e689a-122">Kind</span></span> | <span data-ttu-id="e689a-123">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e689a-123">Supported dimension counts</span></span> | <span data-ttu-id="e689a-124">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e689a-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e689a-125">атенсор</span><span class="sxs-lookup"><span data-stu-id="e689a-125">ATensor</span></span> | <span data-ttu-id="e689a-126">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e689a-126">Input</span></span> | <span data-ttu-id="e689a-127">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e689a-127">1 to 8</span></span> | <span data-ttu-id="e689a-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e689a-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e689a-129">бтенсор</span><span class="sxs-lookup"><span data-stu-id="e689a-129">BTensor</span></span> | <span data-ttu-id="e689a-130">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e689a-130">Input</span></span> | <span data-ttu-id="e689a-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e689a-131">1 to 8</span></span> | <span data-ttu-id="e689a-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e689a-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e689a-133">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e689a-133">OutputTensor</span></span> | <span data-ttu-id="e689a-134">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e689a-134">Output</span></span> | <span data-ttu-id="e689a-135">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e689a-135">1 to 8</span></span> | <span data-ttu-id="e689a-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="e689a-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="e689a-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e689a-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e689a-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="e689a-138">**Header**</span></span> | <span data-ttu-id="e689a-139">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e689a-139">directml.h</span></span> |