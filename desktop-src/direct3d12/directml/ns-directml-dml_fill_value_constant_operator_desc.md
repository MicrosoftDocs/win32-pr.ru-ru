---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Заполняет тензорные заданным *значением* константы.
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: 4fe9f766fc48a4b1ca0d32082dcd8a5f67591195
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803037"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="414f6-103">Структура DML_FILL_VALUE_CONSTANT_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="414f6-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="414f6-104">Заполняет тензорные заданным *значением* константы.</span><span class="sxs-lookup"><span data-stu-id="414f6-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="414f6-105">Этот оператор выполняет следующий псевдокод.</span><span class="sxs-lookup"><span data-stu-id="414f6-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="414f6-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="414f6-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="414f6-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="414f6-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="414f6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="414f6-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="414f6-109">Члены</span><span class="sxs-lookup"><span data-stu-id="414f6-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="414f6-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="414f6-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="414f6-111">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="414f6-111">The tensor to write the results to.</span></span> <span data-ttu-id="414f6-112">Этот тензорные может иметь любой размер.</span><span class="sxs-lookup"><span data-stu-id="414f6-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="414f6-113">Тип: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="414f6-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="414f6-114">Тип данных поля *значения* , который должен соответствовать *аутпуттенсор. DataType*.</span><span class="sxs-lookup"><span data-stu-id="414f6-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="414f6-115">Тип: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="414f6-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="414f6-116">Постоянное значение для заполнения выходных данных с *валуедататипе* , определяющей способ интерпретации поля.</span><span class="sxs-lookup"><span data-stu-id="414f6-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="414f6-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="414f6-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="414f6-118">Доступность</span><span class="sxs-lookup"><span data-stu-id="414f6-118">Availability</span></span>
<span data-ttu-id="414f6-119">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="414f6-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="414f6-120">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="414f6-120">Tensor support</span></span>
| <span data-ttu-id="414f6-121">Тензорные</span><span class="sxs-lookup"><span data-stu-id="414f6-121">Tensor</span></span> | <span data-ttu-id="414f6-122">Вид</span><span class="sxs-lookup"><span data-stu-id="414f6-122">Kind</span></span> | <span data-ttu-id="414f6-123">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="414f6-123">Supported dimension counts</span></span> | <span data-ttu-id="414f6-124">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="414f6-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="414f6-125">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="414f6-125">OutputTensor</span></span> | <span data-ttu-id="414f6-126">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="414f6-126">Output</span></span> | <span data-ttu-id="414f6-127">4</span><span class="sxs-lookup"><span data-stu-id="414f6-127">4</span></span> | <span data-ttu-id="414f6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="414f6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="414f6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="414f6-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="414f6-130">**Header**</span><span class="sxs-lookup"><span data-stu-id="414f6-130">**Header**</span></span> | <span data-ttu-id="414f6-131">директмл. h</span><span class="sxs-lookup"><span data-stu-id="414f6-131">directml.h</span></span> |