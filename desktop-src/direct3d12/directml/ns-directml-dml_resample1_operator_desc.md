---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Ресамплинг элементов из источника в целевой тензорные с использованием коэффициентов масштабирования для расчета размера целевого тензорные. Можно использовать линейный или ближайший к соседним режим интерполяции.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550399"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="215b6-104">Структура DML_RESAMPLE1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="215b6-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="215b6-105">Ресамплинг элементов из источника в целевой тензорные с использованием коэффициентов масштабирования для расчета размера целевого тензорные.</span><span class="sxs-lookup"><span data-stu-id="215b6-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="215b6-106">Можно использовать линейный или ближайший к соседним режим интерполяции.</span><span class="sxs-lookup"><span data-stu-id="215b6-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="215b6-107">Оператор поддерживает интерполяцию по нескольким измерениям, а не только к 2D.</span><span class="sxs-lookup"><span data-stu-id="215b6-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="215b6-108">Таким образом, можно иметь одинаковый пространственный размер, но выполнять интерполяцию по каналам или по пакетам.</span><span class="sxs-lookup"><span data-stu-id="215b6-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="215b6-109">Связь между входными и выходными координатами приведена ниже.</span><span class="sxs-lookup"><span data-stu-id="215b6-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="215b6-110">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="215b6-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="215b6-111">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="215b6-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="215b6-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="215b6-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="215b6-113">Участники</span><span class="sxs-lookup"><span data-stu-id="215b6-113">Members</span></span>

`InputTensor`

<span data-ttu-id="215b6-114">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="215b6-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="215b6-115">Тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="215b6-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="215b6-116">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="215b6-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="215b6-117">Тензорные для записи выходных данных.</span><span class="sxs-lookup"><span data-stu-id="215b6-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="215b6-118">Тип: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="215b6-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="215b6-119">Это поле определяет тип интерполяции, используемый для выбора выходных пикселей.</span><span class="sxs-lookup"><span data-stu-id="215b6-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="215b6-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="215b6-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="215b6-121">Использует *ближайший алгоритм соседей* , который выбирает элемент ввода, ближайший к соответствующему центру пикселей для каждого выходного элемента.</span><span class="sxs-lookup"><span data-stu-id="215b6-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="215b6-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="215b6-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="215b6-123">Использует алгоритм *куадрилинеар* , который вычисляет элемент Output, выполняя взвешенное среднее по 2 ближайшим соседним входным элементам на измерение.</span><span class="sxs-lookup"><span data-stu-id="215b6-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="215b6-124">Так как все 4 измерения можно повторно вычислить, взвешенное среднее вычисляется по общему количеству 16 входных элементов для каждого выходного элемента.</span><span class="sxs-lookup"><span data-stu-id="215b6-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="215b6-125">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="215b6-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="215b6-126">Количество значений в массивах, которые *масштабируются*, *инпутпикселоффсетс* и *аутпутпикселоффсетс* указывают на.</span><span class="sxs-lookup"><span data-stu-id="215b6-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="215b6-127">Это значение должно соответствовать числу измерений *инпуттенсор* и *аутпуттенсор*, который должен быть равен 4.</span><span class="sxs-lookup"><span data-stu-id="215b6-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="215b6-128">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="215b6-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="215b6-129">Шкалы, применяемые при переборке входных данных, где масштабируется > 1. Увеличение масштаба изображения и масштабирование < 1 масштабирование изображения для этого измерения.</span><span class="sxs-lookup"><span data-stu-id="215b6-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="215b6-130">Обратите внимание, что масштабы не обязательно должны быть в точности `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="215b6-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="215b6-131">Если входные данные после масштабирования больше, чем у границ выходных данных, мы обрезать его до размера выходных данных.</span><span class="sxs-lookup"><span data-stu-id="215b6-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="215b6-132">С другой стороны, если входные данные после масштабирования меньше, чем граница выходных данных, края выходных данных будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="215b6-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="215b6-133">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="215b6-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="215b6-134">Смещение, применяемое к входным точкам до повторной выборки.</span><span class="sxs-lookup"><span data-stu-id="215b6-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="215b6-135">Если это значение равно `0` , то вместо его центра используется верхний левый угол пикселя, который обычно не дает ожидаемого результата.</span><span class="sxs-lookup"><span data-stu-id="215b6-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="215b6-136">Для повторной выборки изображения с помощью центра пикселов и для получения того же поведения, что и [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), это значение должно быть `0.5` .</span><span class="sxs-lookup"><span data-stu-id="215b6-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="215b6-137">Тип: \_ \_ Размер поля \_ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="215b6-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="215b6-138">Смещение, применяемое к выходным пикселям после перевыборки.</span><span class="sxs-lookup"><span data-stu-id="215b6-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="215b6-139">Если это значение равно `0` , то вместо его центра используется верхний левый угол пикселя, который обычно не дает ожидаемого результата.</span><span class="sxs-lookup"><span data-stu-id="215b6-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="215b6-140">Для повторной выборки изображения с помощью центра пикселов и для получения того же поведения, что и [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), это значение должно быть `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="215b6-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="215b6-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="215b6-141">Remarks</span></span>
<span data-ttu-id="215b6-142">Если для *инпутпикселоффсетс* задано значение 0,5, а для *аутпутпикселоффсетс* задано значение-0,5, этот оператор эквивалентен [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="215b6-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="215b6-143">Доступность</span><span class="sxs-lookup"><span data-stu-id="215b6-143">Availability</span></span>
<span data-ttu-id="215b6-144">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="215b6-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="215b6-145">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="215b6-145">Tensor constraints</span></span>
<span data-ttu-id="215b6-146">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="215b6-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="215b6-147">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="215b6-147">Tensor support</span></span>
| <span data-ttu-id="215b6-148">Тензорные</span><span class="sxs-lookup"><span data-stu-id="215b6-148">Tensor</span></span> | <span data-ttu-id="215b6-149">Вид</span><span class="sxs-lookup"><span data-stu-id="215b6-149">Kind</span></span> | <span data-ttu-id="215b6-150">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="215b6-150">Supported dimension counts</span></span> | <span data-ttu-id="215b6-151">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="215b6-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="215b6-152">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="215b6-152">InputTensor</span></span> | <span data-ttu-id="215b6-153">Входные данные</span><span class="sxs-lookup"><span data-stu-id="215b6-153">Input</span></span> | <span data-ttu-id="215b6-154">4</span><span class="sxs-lookup"><span data-stu-id="215b6-154">4</span></span> | <span data-ttu-id="215b6-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="215b6-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="215b6-156">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="215b6-156">OutputTensor</span></span> | <span data-ttu-id="215b6-157">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="215b6-157">Output</span></span> | <span data-ttu-id="215b6-158">4</span><span class="sxs-lookup"><span data-stu-id="215b6-158">4</span></span> | <span data-ttu-id="215b6-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="215b6-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="215b6-160">Требования</span><span class="sxs-lookup"><span data-stu-id="215b6-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="215b6-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="215b6-161">**Header**</span></span> | <span data-ttu-id="215b6-162">директмл. h</span><span class="sxs-lookup"><span data-stu-id="215b6-162">directml.h</span></span> |