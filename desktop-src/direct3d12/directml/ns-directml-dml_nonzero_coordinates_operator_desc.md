---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Выполняет вычисление N-мерных координат всех ненулевых элементов входного тензорные.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417533"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="56fa7-103">Структура DML_NONZERO_COORDINATES_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="56fa7-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="56fa7-104">Выполняет вычисление N-мерных координат всех ненулевых элементов входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="56fa7-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="56fa7-105">Этот оператор создает MxN матрицу значений, где каждая строка M содержит N-мерный координату ненулевого значения из входных данных.</span><span class="sxs-lookup"><span data-stu-id="56fa7-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="56fa7-106">При использовании входных данных **FLOAT32** или **FLOAT16** отрицательные и положительные 0 (0,0 f и-0.0 f) обрабатываются как нули в целях данного оператора.</span><span class="sxs-lookup"><span data-stu-id="56fa7-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="56fa7-107">Оператор требует, чтобы размер *аутпуткурдинатестенсор* был достаточно большим, чтобы соответствовать наихудшему сценарию, где каждый элемент входных данных не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="56fa7-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="56fa7-108">Этот оператор возвращает количество ненулевых элементов через *аутпуткаунттенсор*, которые вызывающие объекты могут проверить, чтобы определить количество координат, записанных в *аутпуткурдинатестенсор*.</span><span class="sxs-lookup"><span data-stu-id="56fa7-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56fa7-109">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="56fa7-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="56fa7-110">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="56fa7-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56fa7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56fa7-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="56fa7-112">Участники</span><span class="sxs-lookup"><span data-stu-id="56fa7-112">Members</span></span>

`InputTensor`

<span data-ttu-id="56fa7-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56fa7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56fa7-114">Входной тензорные.</span><span class="sxs-lookup"><span data-stu-id="56fa7-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="56fa7-115">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56fa7-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56fa7-116">Выходной тензорные, содержащий количество ненулевых элементов во входном тензорные.</span><span class="sxs-lookup"><span data-stu-id="56fa7-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="56fa7-117">Этот тензорные должен быть скалярным, то &mdash; есть размеры этого тензорные должны быть 1.</span><span class="sxs-lookup"><span data-stu-id="56fa7-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="56fa7-118">Тип этого тензорные должен быть **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="56fa7-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="56fa7-119">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56fa7-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56fa7-120">Выходной тензорные, содержащий N-мерных координат элементов ввода, которые не равны нулю.</span><span class="sxs-lookup"><span data-stu-id="56fa7-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="56fa7-121">Этот тензорные должен иметь *размеры* `{1,1,M,N}` (если значение *DimensionCount* равно 4) или `{1,1,1,M,N}` (если *DimensionCount* равно 5), где M — общее число элементов в *инпуттенсор*, а N — больше или равно *эффективному рангу* *инпуттенсор*, вплоть до *DimensionCount* входного значения.</span><span class="sxs-lookup"><span data-stu-id="56fa7-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="56fa7-122">Эффективный ранг тензорные определяется *DimensionCountом* того, что тензорные за исключением ведущих измерений размера 1.</span><span class="sxs-lookup"><span data-stu-id="56fa7-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="56fa7-123">Например, тензорные с размером `{1,2,3,4}` имеет эффективный ранг 3, как и тензорные с размерами `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="56fa7-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="56fa7-124">Тензорные с размером `{1,1,1,1}` имеет действующий ранг 0.</span><span class="sxs-lookup"><span data-stu-id="56fa7-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="56fa7-125">Рассмотрим *инпуттенсор* с *размерами* `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="56fa7-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="56fa7-126">Этот входной тензорные содержит 60 элементов и имеет эффективный ранг 2.</span><span class="sxs-lookup"><span data-stu-id="56fa7-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="56fa7-127">В этом примере все допустимые размеры *аутпуткурдинатестенсор* имеют форму `{1,1,60,N}` , где N >= 2, но не больше, чем *DimensionCount* (4 в этом примере).</span><span class="sxs-lookup"><span data-stu-id="56fa7-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="56fa7-128">Координаты, записанные в этот тензорные, гарантированно упорядочиваются по возрастанию индексов элементов.</span><span class="sxs-lookup"><span data-stu-id="56fa7-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="56fa7-129">Например, если входные тензорные имеют 3 ненулевые значения в координатах {1,0} , {1,2} , и {0,5} , значения, записанные *в аутпуткурдинатестенсор* , будут иметь значение `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="56fa7-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="56fa7-130">Хотя для этого тензорные требуется, чтобы измерение M было равно числу элементов во входном тензорные, этот оператор записывает в этот тензорные не более Аутпуткаунт элементов.</span><span class="sxs-lookup"><span data-stu-id="56fa7-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="56fa7-131">Аутпуткаунт возвращается через скалярный *аутпуткаунттенсор*.</span><span class="sxs-lookup"><span data-stu-id="56fa7-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="56fa7-132">Оставшиеся элементы этого тензорные за пределами Аутпуткаунт не определены после завершения этого оператора.</span><span class="sxs-lookup"><span data-stu-id="56fa7-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="56fa7-133">Не следует полагаться на значения этих элементов.</span><span class="sxs-lookup"><span data-stu-id="56fa7-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="56fa7-134">Пример</span><span class="sxs-lookup"><span data-stu-id="56fa7-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="56fa7-135">Доступность</span><span class="sxs-lookup"><span data-stu-id="56fa7-135">Availability</span></span>
<span data-ttu-id="56fa7-136">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="56fa7-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="56fa7-137">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="56fa7-137">Tensor constraints</span></span>
<span data-ttu-id="56fa7-138">*Инпуттенсор*, *аутпуткурдинатестенсор* и `OutputCountTensor` должны иметь одинаковый *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="56fa7-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="56fa7-139">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="56fa7-139">Tensor support</span></span>
| <span data-ttu-id="56fa7-140">Тензорные</span><span class="sxs-lookup"><span data-stu-id="56fa7-140">Tensor</span></span> | <span data-ttu-id="56fa7-141">Вид</span><span class="sxs-lookup"><span data-stu-id="56fa7-141">Kind</span></span> | <span data-ttu-id="56fa7-142">Измерения</span><span class="sxs-lookup"><span data-stu-id="56fa7-142">Dimensions</span></span> | <span data-ttu-id="56fa7-143">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="56fa7-143">Supported dimension counts</span></span> | <span data-ttu-id="56fa7-144">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="56fa7-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="56fa7-145">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="56fa7-145">InputTensor</span></span> | <span data-ttu-id="56fa7-146">Входные данные</span><span class="sxs-lookup"><span data-stu-id="56fa7-146">Input</span></span> | <span data-ttu-id="56fa7-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="56fa7-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="56fa7-148">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="56fa7-148">4 to 5</span></span> | <span data-ttu-id="56fa7-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="56fa7-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="56fa7-150">аутпуткаунттенсор</span><span class="sxs-lookup"><span data-stu-id="56fa7-150">OutputCountTensor</span></span> | <span data-ttu-id="56fa7-151">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="56fa7-151">Output</span></span> | <span data-ttu-id="56fa7-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="56fa7-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="56fa7-153">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="56fa7-153">4 to 5</span></span> | <span data-ttu-id="56fa7-154">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="56fa7-154">UINT32</span></span> |
| <span data-ttu-id="56fa7-155">аутпуткурдинатестенсор</span><span class="sxs-lookup"><span data-stu-id="56fa7-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="56fa7-156">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="56fa7-156">Output</span></span> | <span data-ttu-id="56fa7-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="56fa7-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="56fa7-158">от 4 до 5</span><span class="sxs-lookup"><span data-stu-id="56fa7-158">4 to 5</span></span> | <span data-ttu-id="56fa7-159">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="56fa7-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="56fa7-160">Требования</span><span class="sxs-lookup"><span data-stu-id="56fa7-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="56fa7-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="56fa7-161">**Header**</span></span> | <span data-ttu-id="56fa7-162">директмл. h</span><span class="sxs-lookup"><span data-stu-id="56fa7-162">directml.h</span></span> |