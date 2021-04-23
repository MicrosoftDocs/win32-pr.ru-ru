---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Выдает значение счетчика побитового заполнения (число бит, заданное равным 1) для каждого элемента входного тензорные и записывает результат в выходной тензорные.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 3c8dddc3159ebcd857c7423b76856fbeba465d2e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803226"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="b13b1-103">Структура DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="b13b1-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b13b1-104">Выдает значение счетчика побитового заполнения (число бит, заданное равным 1) для каждого элемента входного тензорные и записывает результат в выходной тензорные.</span><span class="sxs-lookup"><span data-stu-id="b13b1-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="b13b1-105">Входной и выходной тензорные должны иметь одинаковые *DimensionCount* и *размеры*, хотя они могут различаться в *DataType*.</span><span class="sxs-lookup"><span data-stu-id="b13b1-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b13b1-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="b13b1-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b13b1-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b13b1-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b13b1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b13b1-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="b13b1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b13b1-109">Members</span></span>

`InputTensor`

<span data-ttu-id="b13b1-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b13b1-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b13b1-111">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="b13b1-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="b13b1-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b13b1-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b13b1-113">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="b13b1-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="b13b1-114">Пример</span><span class="sxs-lookup"><span data-stu-id="b13b1-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="b13b1-115">Доступность</span><span class="sxs-lookup"><span data-stu-id="b13b1-115">Availability</span></span>
<span data-ttu-id="b13b1-116">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b13b1-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b13b1-117">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="b13b1-117">Tensor constraints</span></span>
<span data-ttu-id="b13b1-118">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="b13b1-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b13b1-119">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="b13b1-119">Tensor support</span></span>
| <span data-ttu-id="b13b1-120">Тензорные</span><span class="sxs-lookup"><span data-stu-id="b13b1-120">Tensor</span></span> | <span data-ttu-id="b13b1-121">Вид</span><span class="sxs-lookup"><span data-stu-id="b13b1-121">Kind</span></span> | <span data-ttu-id="b13b1-122">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="b13b1-122">Supported dimension counts</span></span> | <span data-ttu-id="b13b1-123">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="b13b1-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b13b1-124">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="b13b1-124">InputTensor</span></span> | <span data-ttu-id="b13b1-125">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b13b1-125">Input</span></span> | <span data-ttu-id="b13b1-126">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="b13b1-126">1 to 8</span></span> | <span data-ttu-id="b13b1-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b13b1-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b13b1-128">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="b13b1-128">OutputTensor</span></span> | <span data-ttu-id="b13b1-129">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b13b1-129">Output</span></span> | <span data-ttu-id="b13b1-130">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="b13b1-130">1 to 8</span></span> | <span data-ttu-id="b13b1-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="b13b1-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b13b1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b13b1-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b13b1-133">**Header**</span><span class="sxs-lookup"><span data-stu-id="b13b1-133">**Header**</span></span> | <span data-ttu-id="b13b1-134">директмл. h</span><span class="sxs-lookup"><span data-stu-id="b13b1-134">directml.h</span></span> |