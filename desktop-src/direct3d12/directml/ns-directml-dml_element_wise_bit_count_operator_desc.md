---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Выполняет побитовую операцию не для каждого элемента входного тензорные и записывает результат в выходной тензорные.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: bb42be1e1f00fcf749ed271d55a7958b43464f1a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719951"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="18ed6-103">Структура DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="18ed6-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="18ed6-104">Выполняет побитовую операцию не для каждого элемента входного тензорные и записывает результат в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="18ed6-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="18ed6-105">Входные и выходные тензорные должны иметь одинаковые *DimensionCount*, *размеры* и *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="18ed6-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="18ed6-106">Этот оператор поддерживает выполнение на месте, что означает, что выходным тензорные может быть присвоен псевдоним входным тензорные во время привязки.</span><span class="sxs-lookup"><span data-stu-id="18ed6-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18ed6-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="18ed6-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="18ed6-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="18ed6-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18ed6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18ed6-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="18ed6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="18ed6-110">Members</span></span>

`InputTensor`

<span data-ttu-id="18ed6-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="18ed6-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="18ed6-112">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="18ed6-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="18ed6-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="18ed6-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="18ed6-114">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="18ed6-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="18ed6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="18ed6-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="18ed6-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="18ed6-116">Availability</span></span>
<span data-ttu-id="18ed6-117">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="18ed6-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="18ed6-118">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="18ed6-118">Tensor constraints</span></span>
<span data-ttu-id="18ed6-119">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="18ed6-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="18ed6-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="18ed6-120">Tensor support</span></span>
| <span data-ttu-id="18ed6-121">Тензорные</span><span class="sxs-lookup"><span data-stu-id="18ed6-121">Tensor</span></span> | <span data-ttu-id="18ed6-122">Вид</span><span class="sxs-lookup"><span data-stu-id="18ed6-122">Kind</span></span> | <span data-ttu-id="18ed6-123">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="18ed6-123">Supported dimension counts</span></span> | <span data-ttu-id="18ed6-124">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="18ed6-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="18ed6-125">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="18ed6-125">InputTensor</span></span> | <span data-ttu-id="18ed6-126">Входные данные</span><span class="sxs-lookup"><span data-stu-id="18ed6-126">Input</span></span> | <span data-ttu-id="18ed6-127">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="18ed6-127">1 to 8</span></span> | <span data-ttu-id="18ed6-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="18ed6-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="18ed6-129">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="18ed6-129">OutputTensor</span></span> | <span data-ttu-id="18ed6-130">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="18ed6-130">Output</span></span> | <span data-ttu-id="18ed6-131">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="18ed6-131">1 to 8</span></span> | <span data-ttu-id="18ed6-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="18ed6-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="18ed6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="18ed6-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="18ed6-134">**Header**</span><span class="sxs-lookup"><span data-stu-id="18ed6-134">**Header**</span></span> | <span data-ttu-id="18ed6-135">директмл. h</span><span class="sxs-lookup"><span data-stu-id="18ed6-135">directml.h</span></span> |