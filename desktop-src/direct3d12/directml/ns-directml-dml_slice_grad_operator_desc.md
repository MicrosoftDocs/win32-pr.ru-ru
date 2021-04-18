---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Вычисление градиентов обратного распространения для среза (см. [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719943"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="5cfdd-103">Структура DML_SLICE_GRAD_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="5cfdd-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5cfdd-104">Вычисление градиентов обратного распространения для среза (см. [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="5cfdd-105">Помните, что [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) извлекает подобласть входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="5cfdd-106">При наличии *инпутградиенттенсор* с теми же размерами, что и в *выходных данных* эквивалентного **DML_SLICE1_OPERATOR_DESC**, этот оператор создает *аутпутградиенттенсор* с теми же размерами, что и *входные данные* **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="5cfdd-107">Фрагментированные элементы распространяются на выходные данные, а все остальные элементы устанавливаются в значение 0.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="5cfdd-108">В качестве примера рассмотрим **DML_SLICE1_OPERATOR_DESC** , который извлекает из тензорные следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="5cfdd-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="5cfdd-109">Если указаны те же  / *размеры* инпутвиндовоффсетс /  , что и в приведенном выше примере, этот оператор будет выполнять следующее преобразование.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="5cfdd-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5cfdd-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfdd-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cfdd-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="5cfdd-113">Члены</span><span class="sxs-lookup"><span data-stu-id="5cfdd-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="5cfdd-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cfdd-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5cfdd-115">Входящий градиент тензорные.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-115">The incoming gradient tensor.</span></span> <span data-ttu-id="5cfdd-116">Обычно это получается из выходных данных обратного распространения предыдущего слоя.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="5cfdd-117">Как правило, этот тензорные будет иметь те же размеры, что и *выходные данные* соответствующего [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="5cfdd-118">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cfdd-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5cfdd-119">Выходной тензорные, содержащий нераспространяемые градиенты.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="5cfdd-120">Как правило, этот тензорные будет иметь те же размеры, что и *входные данные* соответствующего [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) в прямом прохождении.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="5cfdd-121">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5cfdd-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5cfdd-122">Число элементов в массивах *инпутвиндовоффсетс*, *инпутвиндовсизес* и *инпутвиндовстридес* .</span><span class="sxs-lookup"><span data-stu-id="5cfdd-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="5cfdd-123">Это значение должно равняться *DimensionCount* , указанному в *инпутградиенттенсор* и *аутпутградиенттенсор*.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="5cfdd-124">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5cfdd-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5cfdd-125">См. раздел *инпутвиндовоффсетс* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="5cfdd-126">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5cfdd-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5cfdd-127">См. раздел *инпутвиндовсизес* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="5cfdd-128">Тип: \_ \_ Размер поля \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="5cfdd-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="5cfdd-129">См. раздел *инпутвиндовстридес* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5cfdd-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="5cfdd-130">Обратите внимание, что в отличие от **DML_SLICE1_OPERATOR_DESC** этот оператор требует ненулевой STRIDE.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="5cfdd-131">Это обусловлено тем, что с нулевым шагом, что элемент input должен сопоставляться с каждым выходным элементом, поэтому невозможно выполнить обратное распространение.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="5cfdd-132">Как и **DML_SLICE1_OPERATOR_DESC**, отрицательный шаг переворачивает направление окна ввода по этой оси.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="5cfdd-133">Доступность</span><span class="sxs-lookup"><span data-stu-id="5cfdd-133">Availability</span></span>
<span data-ttu-id="5cfdd-134">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5cfdd-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5cfdd-135">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="5cfdd-135">Tensor constraints</span></span>
<span data-ttu-id="5cfdd-136">*Инпутградиенттенсор* и *аутпутградиенттенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="5cfdd-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5cfdd-137">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="5cfdd-137">Tensor support</span></span>
| <span data-ttu-id="5cfdd-138">Тензорные</span><span class="sxs-lookup"><span data-stu-id="5cfdd-138">Tensor</span></span> | <span data-ttu-id="5cfdd-139">Вид</span><span class="sxs-lookup"><span data-stu-id="5cfdd-139">Kind</span></span> | <span data-ttu-id="5cfdd-140">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="5cfdd-140">Supported dimension counts</span></span> | <span data-ttu-id="5cfdd-141">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="5cfdd-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5cfdd-142">инпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="5cfdd-142">InputGradientTensor</span></span> | <span data-ttu-id="5cfdd-143">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5cfdd-143">Input</span></span> | <span data-ttu-id="5cfdd-144">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="5cfdd-144">1 to 8</span></span> | <span data-ttu-id="5cfdd-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5cfdd-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5cfdd-146">аутпутградиенттенсор</span><span class="sxs-lookup"><span data-stu-id="5cfdd-146">OutputGradientTensor</span></span> | <span data-ttu-id="5cfdd-147">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="5cfdd-147">Output</span></span> | <span data-ttu-id="5cfdd-148">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="5cfdd-148">1 to 8</span></span> | <span data-ttu-id="5cfdd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5cfdd-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5cfdd-150">Требования</span><span class="sxs-lookup"><span data-stu-id="5cfdd-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5cfdd-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="5cfdd-151">**Header**</span></span> | <span data-ttu-id="5cfdd-152">директмл. h</span><span class="sxs-lookup"><span data-stu-id="5cfdd-152">directml.h</span></span> |