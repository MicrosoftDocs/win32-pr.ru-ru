---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Заполняет тензорные последовательностью.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: 17b503630db2108dc4d9d2f5c2f32f7e324189d1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803040"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a><span data-ttu-id="39ed8-103">Структура DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="39ed8-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="39ed8-104">Заполняет тензорные последовательностью.</span><span class="sxs-lookup"><span data-stu-id="39ed8-104">Fills a tensor with a sequence.</span></span> <span data-ttu-id="39ed8-105">Этот оператор выполняет следующий псевдокод.</span><span class="sxs-lookup"><span data-stu-id="39ed8-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="39ed8-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="39ed8-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="39ed8-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="39ed8-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="39ed8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39ed8-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a><span data-ttu-id="39ed8-109">Члены</span><span class="sxs-lookup"><span data-stu-id="39ed8-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="39ed8-110">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="39ed8-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="39ed8-111">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="39ed8-111">The tensor to write the results to.</span></span> <span data-ttu-id="39ed8-112">Этот тензорные может иметь любой размер.</span><span class="sxs-lookup"><span data-stu-id="39ed8-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="39ed8-113">Тип: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="39ed8-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="39ed8-114">Тип данных поля *значения* , который должен соответствовать *аутпуттенсор. DataType*.</span><span class="sxs-lookup"><span data-stu-id="39ed8-114">The data type of *Value* field, which must match *OutputTensor.DataType*.</span></span>


`ValueStart`

<span data-ttu-id="39ed8-115">Тип: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="39ed8-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="39ed8-116">Начальное значение для заполнения первого элемента в выходных данных с помощью *валуедататипе* , определяющего способ интерпретации поля.</span><span class="sxs-lookup"><span data-stu-id="39ed8-116">The initial value to fill the first element in the output, with *ValueDataType* determining how to interpret the field.</span></span>


`ValueDelta`

<span data-ttu-id="39ed8-117">Тип: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="39ed8-117">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="39ed8-118">Шаг, добавляемый к значению для каждого записанного элемента с *валуедататипе* , определяющим способ интерпретации поля.</span><span class="sxs-lookup"><span data-stu-id="39ed8-118">A step to add to the value for each element written, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="39ed8-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="39ed8-119">Examples</span></span>

### <a name="example-1-1d-ascending-step"></a><span data-ttu-id="39ed8-120">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="39ed8-120">Example 1.</span></span> <span data-ttu-id="39ed8-121">Шаг с 1D по возрастанию</span><span class="sxs-lookup"><span data-stu-id="39ed8-121">1D ascending step</span></span>

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a><span data-ttu-id="39ed8-122">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="39ed8-122">Example 2.</span></span> <span data-ttu-id="39ed8-123">2D-шаг по возрастанию</span><span class="sxs-lookup"><span data-stu-id="39ed8-123">2D ascending step</span></span>

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a><span data-ttu-id="39ed8-124">Доступность</span><span class="sxs-lookup"><span data-stu-id="39ed8-124">Availability</span></span>
<span data-ttu-id="39ed8-125">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="39ed8-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="39ed8-126">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="39ed8-126">Tensor support</span></span>
| <span data-ttu-id="39ed8-127">Тензорные</span><span class="sxs-lookup"><span data-stu-id="39ed8-127">Tensor</span></span> | <span data-ttu-id="39ed8-128">Вид</span><span class="sxs-lookup"><span data-stu-id="39ed8-128">Kind</span></span> | <span data-ttu-id="39ed8-129">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="39ed8-129">Supported dimension counts</span></span> | <span data-ttu-id="39ed8-130">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="39ed8-130">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="39ed8-131">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="39ed8-131">OutputTensor</span></span> | <span data-ttu-id="39ed8-132">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="39ed8-132">Output</span></span> | <span data-ttu-id="39ed8-133">4</span><span class="sxs-lookup"><span data-stu-id="39ed8-133">4</span></span> | <span data-ttu-id="39ed8-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="39ed8-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="39ed8-135">Требования</span><span class="sxs-lookup"><span data-stu-id="39ed8-135">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="39ed8-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="39ed8-136">**Header**</span></span> | <span data-ttu-id="39ed8-137">директмл. h</span><span class="sxs-lookup"><span data-stu-id="39ed8-137">directml.h</span></span> |