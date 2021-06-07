---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Вычисляются побитовое или между соответствующим элементом входных десятков и записывает результат в выходной тензорные.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: 7138c6647e1bd4df5d8957468ca67f103f4a3f5a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418085"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a><span data-ttu-id="5d7ff-103">Структура DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="5d7ff-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5d7ff-104">Вычисляются побитовое или между соответствующим элементом входных десятков и записывает результат в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-104">Computes the bitwise OR between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="5d7ff-105">Входные и выходные тензорные должны иметь одинаковые *DimensionCount*, *размеры* и *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="5d7ff-106">Этот оператор поддерживает выполнение на месте. Это означает, что выходным тензорные может быть присвоен псевдоним одному или нескольким входным десяткам во время привязки.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d7ff-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="5d7ff-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5d7ff-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5d7ff-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7ff-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d7ff-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="5d7ff-110">Участники</span><span class="sxs-lookup"><span data-stu-id="5d7ff-110">Members</span></span>

`ATensor`

<span data-ttu-id="5d7ff-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5d7ff-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5d7ff-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="5d7ff-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5d7ff-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5d7ff-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="5d7ff-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5d7ff-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5d7ff-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="5d7ff-117">Доступность</span><span class="sxs-lookup"><span data-stu-id="5d7ff-117">Availability</span></span>
<span data-ttu-id="5d7ff-118">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5d7ff-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5d7ff-119">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-119">Tensor constraints</span></span>
<span data-ttu-id="5d7ff-120">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="5d7ff-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5d7ff-121">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-121">Tensor support</span></span>
| <span data-ttu-id="5d7ff-122">Тензорные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-122">Tensor</span></span> | <span data-ttu-id="5d7ff-123">Вид</span><span class="sxs-lookup"><span data-stu-id="5d7ff-123">Kind</span></span> | <span data-ttu-id="5d7ff-124">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="5d7ff-124">Supported dimension counts</span></span> | <span data-ttu-id="5d7ff-125">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="5d7ff-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5d7ff-126">атенсор</span><span class="sxs-lookup"><span data-stu-id="5d7ff-126">ATensor</span></span> | <span data-ttu-id="5d7ff-127">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-127">Input</span></span> | <span data-ttu-id="5d7ff-128">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-128">1 to 8</span></span> | <span data-ttu-id="5d7ff-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5d7ff-130">бтенсор</span><span class="sxs-lookup"><span data-stu-id="5d7ff-130">BTensor</span></span> | <span data-ttu-id="5d7ff-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-131">Input</span></span> | <span data-ttu-id="5d7ff-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-132">1 to 8</span></span> | <span data-ttu-id="5d7ff-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5d7ff-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="5d7ff-134">OutputTensor</span></span> | <span data-ttu-id="5d7ff-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="5d7ff-135">Output</span></span> | <span data-ttu-id="5d7ff-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-136">1 to 8</span></span> | <span data-ttu-id="5d7ff-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5d7ff-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5d7ff-138">Требования</span><span class="sxs-lookup"><span data-stu-id="5d7ff-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5d7ff-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="5d7ff-139">**Header**</span></span> | <span data-ttu-id="5d7ff-140">директмл. h</span><span class="sxs-lookup"><span data-stu-id="5d7ff-140">directml.h</span></span> |