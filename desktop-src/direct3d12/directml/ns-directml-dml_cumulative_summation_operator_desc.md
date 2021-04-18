---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719982"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="b4a67-103">Структура DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="b4a67-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b4a67-104">Суммирует элементы тензорные вдоль оси, записывая выполняющийся счетчик суммы в выходном тензорные.</span><span class="sxs-lookup"><span data-stu-id="b4a67-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4a67-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="b4a67-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b4a67-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b4a67-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a67-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4a67-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="b4a67-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b4a67-108">Members</span></span>

`InputTensor`

<span data-ttu-id="b4a67-109">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4a67-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4a67-110">Входной тензорные, содержащий элементы для суммирования.</span><span class="sxs-lookup"><span data-stu-id="b4a67-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="b4a67-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b4a67-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b4a67-112">Выходной тензорные для записи итоговых суммарных сумм в.</span><span class="sxs-lookup"><span data-stu-id="b4a67-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="b4a67-113">Этот тензорные должен иметь те же размеры и тип данных, что и *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="b4a67-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="b4a67-114">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b4a67-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b4a67-115">Индекс измерения для суммирования элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a67-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="b4a67-116">Это значение должно быть меньше значения параметра *DimensionCount* *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="b4a67-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="b4a67-117">Тип: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="b4a67-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="b4a67-118">Одно из значений перечисления [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a67-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="b4a67-119">Если задано значение **DML_AXIS_DIRECTION_INCREASING**, то суммирование выполняется путем просмотра тензорные вдоль указанной оси по возрастанию индекса элементов.</span><span class="sxs-lookup"><span data-stu-id="b4a67-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="b4a67-120">Если задано значение **DML_AXIS_DIRECTION_DECREASING**, обратное значение равно true, а суммирование выполняется путем обхода элементов по убыванию индекса.</span><span class="sxs-lookup"><span data-stu-id="b4a67-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="b4a67-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4a67-121">Remarks</span></span>
<span data-ttu-id="b4a67-122">Этот оператор поддерживает выполнение на месте, что означает, что *аутпуттенсор* может использовать псевдоним *инпуттенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="b4a67-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="b4a67-123">Доступность</span><span class="sxs-lookup"><span data-stu-id="b4a67-123">Availability</span></span>
<span data-ttu-id="b4a67-124">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b4a67-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b4a67-125">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="b4a67-125">Tensor constraints</span></span>
<span data-ttu-id="b4a67-126">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые типы *данных* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="b4a67-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b4a67-127">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="b4a67-127">Tensor support</span></span>
| <span data-ttu-id="b4a67-128">Тензорные</span><span class="sxs-lookup"><span data-stu-id="b4a67-128">Tensor</span></span> | <span data-ttu-id="b4a67-129">Вид</span><span class="sxs-lookup"><span data-stu-id="b4a67-129">Kind</span></span> | <span data-ttu-id="b4a67-130">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="b4a67-130">Supported dimension counts</span></span> | <span data-ttu-id="b4a67-131">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="b4a67-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b4a67-132">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="b4a67-132">InputTensor</span></span> | <span data-ttu-id="b4a67-133">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b4a67-133">Input</span></span> | <span data-ttu-id="b4a67-134">4</span><span class="sxs-lookup"><span data-stu-id="b4a67-134">4</span></span> | <span data-ttu-id="b4a67-135">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b4a67-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="b4a67-136">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="b4a67-136">OutputTensor</span></span> | <span data-ttu-id="b4a67-137">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="b4a67-137">Output</span></span> | <span data-ttu-id="b4a67-138">4</span><span class="sxs-lookup"><span data-stu-id="b4a67-138">4</span></span> | <span data-ttu-id="b4a67-139">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b4a67-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="b4a67-140">Требования</span><span class="sxs-lookup"><span data-stu-id="b4a67-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b4a67-141">**Header**</span><span class="sxs-lookup"><span data-stu-id="b4a67-141">**Header**</span></span> | <span data-ttu-id="b4a67-142">директмл. h</span><span class="sxs-lookup"><span data-stu-id="b4a67-142">directml.h</span></span> |