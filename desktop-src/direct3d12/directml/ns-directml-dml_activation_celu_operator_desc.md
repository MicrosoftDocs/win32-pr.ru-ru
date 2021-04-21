---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Выполняет постоянную функцию активации дифферентиабле экспоненциального линейного блока (ЦЕЛУ) для каждого элемента в *инпуттенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: b6497e995601d7e9e01696f39920672674be07c4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803727"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="339c1-103">Структура DML_ACTIVATION_CELU_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="339c1-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="339c1-104">Выполняет постоянную функцию активации дифферентиабле экспоненциального линейного блока (ЦЕЛУ) для каждого элемента в *инпуттенсор*, помещая результат в соответствующий элемент *аутпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="339c1-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="339c1-105">Где:</span><span class="sxs-lookup"><span data-stu-id="339c1-105">Where:</span></span>
* <span data-ttu-id="339c1-106">EXP (x) является естественной функцией возведения в степень</span><span class="sxs-lookup"><span data-stu-id="339c1-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="339c1-107">Функция Max (a, b) возвращает большее из двух значений a, b</span><span class="sxs-lookup"><span data-stu-id="339c1-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="339c1-108">min (a, b) Возвращает меньшее из двух значений a, b</span><span class="sxs-lookup"><span data-stu-id="339c1-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="339c1-109">Этот оператор поддерживает выполнение на месте. Это означает, что тензорные вывода может иметь псевдоним *инпуттенсор* во время привязки.</span><span class="sxs-lookup"><span data-stu-id="339c1-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="339c1-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="339c1-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="339c1-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="339c1-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="339c1-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="339c1-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="339c1-113">Члены</span><span class="sxs-lookup"><span data-stu-id="339c1-113">Members</span></span>

`InputTensor`

<span data-ttu-id="339c1-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="339c1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="339c1-115">Входной тензорные для чтения из.</span><span class="sxs-lookup"><span data-stu-id="339c1-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="339c1-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="339c1-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="339c1-117">Выходной тензорные для записи результатов в.</span><span class="sxs-lookup"><span data-stu-id="339c1-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="339c1-118">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="339c1-118">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="339c1-119">Коэффициент альфа.</span><span class="sxs-lookup"><span data-stu-id="339c1-119">The alpha coefficient.</span></span> <span data-ttu-id="339c1-120">Стандартное значение по умолчанию для этого параметра — 1,0.</span><span class="sxs-lookup"><span data-stu-id="339c1-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="339c1-121">Доступность</span><span class="sxs-lookup"><span data-stu-id="339c1-121">Availability</span></span>
<span data-ttu-id="339c1-122">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="339c1-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="339c1-123">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="339c1-123">Tensor constraints</span></span>
<span data-ttu-id="339c1-124">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="339c1-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="339c1-125">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="339c1-125">Tensor support</span></span>
| <span data-ttu-id="339c1-126">Тензорные</span><span class="sxs-lookup"><span data-stu-id="339c1-126">Tensor</span></span> | <span data-ttu-id="339c1-127">Вид</span><span class="sxs-lookup"><span data-stu-id="339c1-127">Kind</span></span> | <span data-ttu-id="339c1-128">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="339c1-128">Supported Dimension Counts</span></span> | <span data-ttu-id="339c1-129">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="339c1-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="339c1-130">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="339c1-130">InputTensor</span></span> | <span data-ttu-id="339c1-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="339c1-131">Input</span></span> | <span data-ttu-id="339c1-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="339c1-132">1 to 8</span></span> | <span data-ttu-id="339c1-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="339c1-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="339c1-134">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="339c1-134">OutputTensor</span></span> | <span data-ttu-id="339c1-135">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="339c1-135">Output</span></span> | <span data-ttu-id="339c1-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="339c1-136">1 to 8</span></span> | <span data-ttu-id="339c1-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="339c1-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="339c1-138">Требования</span><span class="sxs-lookup"><span data-stu-id="339c1-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="339c1-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="339c1-139">**Header**</span></span> | <span data-ttu-id="339c1-140">директмл. h</span><span class="sxs-lookup"><span data-stu-id="339c1-140">directml.h</span></span> |