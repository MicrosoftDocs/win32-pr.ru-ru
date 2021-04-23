---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Выполняет побитовую операцию XOR (исключающее или) между каждым соответствующим элементом входных десятков и записывает результат в выходной тензорные.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803193"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="e1b32-103">Структура DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e1b32-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e1b32-104">Выполняет побитовую операцию XOR (исключающее или) между каждым соответствующим элементом входных десятков и записывает результат в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="e1b32-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="e1b32-105">Входные и выходные тензорные должны иметь одинаковые *DimensionCount*, *размеры* и *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="e1b32-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="e1b32-106">Этот оператор поддерживает выполнение на месте. Это означает, что выходным тензорные может быть присвоен псевдоним одному или нескольким входным десяткам во время привязки.</span><span class="sxs-lookup"><span data-stu-id="e1b32-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1b32-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="e1b32-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e1b32-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e1b32-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b32-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1b32-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="e1b32-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e1b32-110">Members</span></span>

`ATensor`

<span data-ttu-id="e1b32-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e1b32-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e1b32-112">Объект тензорные, содержащий входные данные левого края.</span><span class="sxs-lookup"><span data-stu-id="e1b32-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="e1b32-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e1b32-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e1b32-114">Объект тензорные, содержащий правые входные данные.</span><span class="sxs-lookup"><span data-stu-id="e1b32-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="e1b32-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e1b32-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e1b32-116">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="e1b32-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="e1b32-117">Пример</span><span class="sxs-lookup"><span data-stu-id="e1b32-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="e1b32-118">Доступность</span><span class="sxs-lookup"><span data-stu-id="e1b32-118">Availability</span></span>
<span data-ttu-id="e1b32-119">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e1b32-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e1b32-120">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e1b32-120">Tensor constraints</span></span>
<span data-ttu-id="e1b32-121">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="e1b32-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e1b32-122">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e1b32-122">Tensor support</span></span>
| <span data-ttu-id="e1b32-123">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e1b32-123">Tensor</span></span> | <span data-ttu-id="e1b32-124">Вид</span><span class="sxs-lookup"><span data-stu-id="e1b32-124">Kind</span></span> | <span data-ttu-id="e1b32-125">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e1b32-125">Supported dimension counts</span></span> | <span data-ttu-id="e1b32-126">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e1b32-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e1b32-127">атенсор</span><span class="sxs-lookup"><span data-stu-id="e1b32-127">ATensor</span></span> | <span data-ttu-id="e1b32-128">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e1b32-128">Input</span></span> | <span data-ttu-id="e1b32-129">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e1b32-129">1 to 8</span></span> | <span data-ttu-id="e1b32-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e1b32-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e1b32-131">бтенсор</span><span class="sxs-lookup"><span data-stu-id="e1b32-131">BTensor</span></span> | <span data-ttu-id="e1b32-132">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e1b32-132">Input</span></span> | <span data-ttu-id="e1b32-133">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e1b32-133">1 to 8</span></span> | <span data-ttu-id="e1b32-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e1b32-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e1b32-135">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e1b32-135">OutputTensor</span></span> | <span data-ttu-id="e1b32-136">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e1b32-136">Output</span></span> | <span data-ttu-id="e1b32-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e1b32-137">1 to 8</span></span> | <span data-ttu-id="e1b32-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e1b32-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="e1b32-139">Требования</span><span class="sxs-lookup"><span data-stu-id="e1b32-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e1b32-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="e1b32-140">**Header**</span></span> | <span data-ttu-id="e1b32-141">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e1b32-141">directml.h</span></span> |