---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Выполняет вычисление двух аргументов-арктангенс для каждого элемента *атенсор* и *Бтенсор*, где *атенсор* — это *ось Y* , а *бтенсор* — *ось X*, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804496"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="a0a14-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="a0a14-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="a0a14-104">Выполняет вычисление двух аргументов-арктангенс для каждого элемента *атенсор* и *Бтенсор*, где *атенсор* — это *ось Y* , а *бтенсор* — *ось X*, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="a0a14-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="a0a14-105">Этот оператор не определен для источника (т. е. Если *атенсор* и *бтенсор* равны 0 для соответствующих элементов).</span><span class="sxs-lookup"><span data-stu-id="a0a14-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="a0a14-107">Этот оператор поддерживает выполнение на месте, что означает, что выходному тензорныеу может быть присвоен псевдоним *атенсор* или *бтенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="a0a14-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0a14-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,5 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="a0a14-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="a0a14-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a0a14-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a14-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0a14-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a0a14-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a0a14-111">Members</span></span>

`ATensor`

<span data-ttu-id="a0a14-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a0a14-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a0a14-113">Входной тензорные для считывания значений оси Y из.</span><span class="sxs-lookup"><span data-stu-id="a0a14-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="a0a14-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a0a14-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a0a14-115">Входной тензорные для считывания значений оси X из.</span><span class="sxs-lookup"><span data-stu-id="a0a14-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="a0a14-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a0a14-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a0a14-117">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="a0a14-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="a0a14-118">Доступность</span><span class="sxs-lookup"><span data-stu-id="a0a14-118">Availability</span></span>
<span data-ttu-id="a0a14-119">Этот оператор появился в `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="a0a14-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a0a14-120">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="a0a14-120">Tensor constraints</span></span>
<span data-ttu-id="a0a14-121">*Атенсор*, *бтенсор* и *Аутпуттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="a0a14-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a0a14-122">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="a0a14-122">Tensor support</span></span>
| <span data-ttu-id="a0a14-123">Тензорные</span><span class="sxs-lookup"><span data-stu-id="a0a14-123">Tensor</span></span> | <span data-ttu-id="a0a14-124">Вид</span><span class="sxs-lookup"><span data-stu-id="a0a14-124">Kind</span></span> | <span data-ttu-id="a0a14-125">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="a0a14-125">Supported dimension counts</span></span> | <span data-ttu-id="a0a14-126">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="a0a14-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a0a14-127">атенсор</span><span class="sxs-lookup"><span data-stu-id="a0a14-127">ATensor</span></span> | <span data-ttu-id="a0a14-128">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0a14-128">Input</span></span> | <span data-ttu-id="a0a14-129">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="a0a14-129">1 to 8</span></span> | <span data-ttu-id="a0a14-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a0a14-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a0a14-131">бтенсор</span><span class="sxs-lookup"><span data-stu-id="a0a14-131">BTensor</span></span> | <span data-ttu-id="a0a14-132">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0a14-132">Input</span></span> | <span data-ttu-id="a0a14-133">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="a0a14-133">1 to 8</span></span> | <span data-ttu-id="a0a14-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a0a14-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a0a14-135">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="a0a14-135">OutputTensor</span></span> | <span data-ttu-id="a0a14-136">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="a0a14-136">Output</span></span> | <span data-ttu-id="a0a14-137">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="a0a14-137">1 to 8</span></span> | <span data-ttu-id="a0a14-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a0a14-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="a0a14-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a0a14-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a0a14-140">**Header**</span><span class="sxs-lookup"><span data-stu-id="a0a14-140">**Header**</span></span> | <span data-ttu-id="a0a14-141">директмл. h</span><span class="sxs-lookup"><span data-stu-id="a0a14-141">directml.h</span></span> |
