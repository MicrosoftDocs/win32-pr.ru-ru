---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Вычисляются градиенты обратного распространения для линейной единицы исправить (Релу).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803674"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="3973b-103">Структура DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="3973b-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3973b-104">Вычисляются градиенты обратного распространения для линейной единицы исправить (Релу).</span><span class="sxs-lookup"><span data-stu-id="3973b-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="3973b-105">Этот оператор выполняет следующие вычисления на уровне элемента.</span><span class="sxs-lookup"><span data-stu-id="3973b-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="3973b-106">Соответствующий оператор прямой передачи — [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="3973b-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3973b-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="3973b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3973b-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3973b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3973b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3973b-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="3973b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="3973b-110">Members</span></span>

`InputTensor`

<span data-ttu-id="3973b-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3973b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3973b-112">Входные данные (функция) тензорные.</span><span class="sxs-lookup"><span data-stu-id="3973b-112">The input (feature) tensor.</span></span> <span data-ttu-id="3973b-113">Обычно это те же входные данные, что были предоставлены во время прямого прохода (см. [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="3973b-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="3973b-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3973b-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3973b-115">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="3973b-115">The incoming gradient tensor.</span></span> <span data-ttu-id="3973b-116">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="3973b-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="3973b-117">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="3973b-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="3973b-118">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3973b-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3973b-119">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="3973b-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="3973b-120">*Размеры* и *тип данных* этого тензорные должны точно соответствовать параметрам *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="3973b-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="3973b-121">Доступность</span><span class="sxs-lookup"><span data-stu-id="3973b-121">Availability</span></span>
<span data-ttu-id="3973b-122">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="3973b-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3973b-123">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="3973b-123">Tensor constraints</span></span>
<span data-ttu-id="3973b-124">*Инпутградиенттенсор*, *инпуттенсор* и *Аутпутградиенттенсор* должны иметь одинаковые типы *данных*, *DimensionCount* и *размеры*.</span><span class="sxs-lookup"><span data-stu-id="3973b-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3973b-125">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="3973b-125">Tensor support</span></span>
| <span data-ttu-id="3973b-126">Тензорные</span><span class="sxs-lookup"><span data-stu-id="3973b-126">Tensor</span></span> | <span data-ttu-id="3973b-127">Вид</span><span class="sxs-lookup"><span data-stu-id="3973b-127">Kind</span></span> | <span data-ttu-id="3973b-128">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="3973b-128">Supported dimension counts</span></span> | <span data-ttu-id="3973b-129">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="3973b-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3973b-130">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="3973b-130">InputTensor</span></span> | <span data-ttu-id="3973b-131">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3973b-131">Input</span></span> | <span data-ttu-id="3973b-132">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="3973b-132">1 to 8</span></span> | <span data-ttu-id="3973b-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3973b-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3973b-134">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="3973b-134">InputGradientTensor</span></span> | <span data-ttu-id="3973b-135">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3973b-135">Input</span></span> | <span data-ttu-id="3973b-136">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="3973b-136">1 to 8</span></span> | <span data-ttu-id="3973b-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3973b-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="3973b-138">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="3973b-138">OutputGradientTensor</span></span> | <span data-ttu-id="3973b-139">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="3973b-139">Output</span></span> | <span data-ttu-id="3973b-140">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="3973b-140">1 to 8</span></span> | <span data-ttu-id="3973b-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3973b-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="3973b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3973b-142">See also</span></span>
[<span data-ttu-id="3973b-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="3973b-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="3973b-144">Требования</span><span class="sxs-lookup"><span data-stu-id="3973b-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3973b-145">**Header**</span><span class="sxs-lookup"><span data-stu-id="3973b-145">**Header**</span></span> | <span data-ttu-id="3973b-146">директмл. h</span><span class="sxs-lookup"><span data-stu-id="3973b-146">directml.h</span></span> |