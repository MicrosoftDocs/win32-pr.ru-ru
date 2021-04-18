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
ms.openlocfilehash: e0afa89e18b6393efc976a782469d1a9765211f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719940"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a><span data-ttu-id="31267-103">Структура DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="31267-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="31267-104">Вычисляются побитовое или между соответствующим элементом входных десятков и записывает результат в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="31267-104">Computes the bitwise OR between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="31267-105">Входные и выходные тензорные должны иметь одинаковые *DimensionCount*, *размеры* и *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="31267-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="31267-106">Этот оператор поддерживает выполнение на месте. Это означает, что выходным тензорные может быть присвоен псевдоним одному или нескольким входным десяткам во время привязки.</span><span class="sxs-lookup"><span data-stu-id="31267-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31267-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="31267-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="31267-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="31267-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31267-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31267-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="31267-110">Члены</span><span class="sxs-lookup"><span data-stu-id="31267-110">Members</span></span>

`ATensor`

<span data-ttu-id="31267-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31267-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31267-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="31267-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="31267-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31267-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31267-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="31267-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="31267-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="31267-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="31267-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="31267-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="31267-117">Доступность</span><span class="sxs-lookup"><span data-stu-id="31267-117">Availability</span></span>
<span data-ttu-id="31267-118">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="31267-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="31267-119">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="31267-119">Tensor constraints</span></span>
<span data-ttu-id="31267-120">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="31267-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="31267-121">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="31267-121">Tensor support</span></span>
| <span data-ttu-id="31267-122">Тензорные</span><span class="sxs-lookup"><span data-stu-id="31267-122">Tensor</span></span> | <span data-ttu-id="31267-123">Вид</span><span class="sxs-lookup"><span data-stu-id="31267-123">Kind</span></span> | <span data-ttu-id="31267-124">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="31267-124">Supported dimension counts</span></span> | <span data-ttu-id="31267-125">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="31267-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="31267-126">атенсор</span><span class="sxs-lookup"><span data-stu-id="31267-126">ATensor</span></span> | <span data-ttu-id="31267-127">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31267-127">Input</span></span> | <span data-ttu-id="31267-128">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="31267-128">1 to 8</span></span> | <span data-ttu-id="31267-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31267-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31267-130">бтенсор</span><span class="sxs-lookup"><span data-stu-id="31267-130">BTensor</span></span> | <span data-ttu-id="31267-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="31267-131">Input</span></span> | <span data-ttu-id="31267-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="31267-132">1 to 8</span></span> | <span data-ttu-id="31267-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31267-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="31267-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="31267-134">OutputTensor</span></span> | <span data-ttu-id="31267-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="31267-135">Output</span></span> | <span data-ttu-id="31267-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="31267-136">1 to 8</span></span> | <span data-ttu-id="31267-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="31267-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="31267-138">Требования</span><span class="sxs-lookup"><span data-stu-id="31267-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="31267-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="31267-139">**Header**</span></span> | <span data-ttu-id="31267-140">директмл. h</span><span class="sxs-lookup"><span data-stu-id="31267-140">directml.h</span></span> |