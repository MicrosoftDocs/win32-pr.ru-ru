---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Выполняет операцию по согласованию рентабельности инвестиций, как описано в [документе Mask R-CNN](https://arxiv.org/abs/1703.06870). В целом операция извлекает кадрирование из входного изображения тензорные и изменяет их размер на общий размер выходных данных, заданный последними 2 измерениями *аутпуттенсор* , используя указанный *интерполатионмоде*.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804009"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="9be92-104">Структура DML_ROI_ALIGN_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="9be92-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9be92-105">Выполняет операцию по согласованию рентабельности инвестиций, как описано в [документе Mask R-CNN](https://arxiv.org/abs/1703.06870).</span><span class="sxs-lookup"><span data-stu-id="9be92-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="9be92-106">В целом операция извлекает кадрирование из входного изображения тензорные и изменяет их размер на общий размер выходных данных, заданный последними 2 измерениями *аутпуттенсор* , используя указанный *интерполатионмоде*.</span><span class="sxs-lookup"><span data-stu-id="9be92-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9be92-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="9be92-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9be92-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9be92-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9be92-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9be92-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="9be92-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9be92-110">Members</span></span>

`InputTensor`

<span data-ttu-id="9be92-111">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9be92-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9be92-112">Объект тензорные, содержащий входные данные с измерениями `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="9be92-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="9be92-113">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9be92-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9be92-114">Тензорные, содержащий интересующие Вас регионы (окупаемость инвестиций).</span><span class="sxs-lookup"><span data-stu-id="9be92-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="9be92-115">Допустимые размеры `ROITensor` : `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` или `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="9be92-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="9be92-116">Для каждой РЕНТАБЕЛЬности значения будут являться координатами верхнего левого и нижнего правого угла в порядке `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="9be92-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="9be92-117">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9be92-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9be92-118">Объект тензорные, содержащий индексы пакетной службы для извлечения РОИС из.</span><span class="sxs-lookup"><span data-stu-id="9be92-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="9be92-119">Допустимые размеры `BatchIndicesTensor` : `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` или `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="9be92-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="9be92-120">Каждое значение является индексом пакета из *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="9be92-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="9be92-121">Поведение не определено, если значения находятся за пределами диапазона [0, Батчкаунт).</span><span class="sxs-lookup"><span data-stu-id="9be92-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="9be92-122">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9be92-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9be92-123">Объект тензорные, содержащий выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9be92-123">A tensor containing the output data.</span></span> <span data-ttu-id="9be92-124">Ожидаемые размеры *аутпуттенсор* : `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="9be92-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="9be92-125">Тип: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="9be92-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="9be92-126">Функция сокращения, используемая при сокращении всех входных выборок, которые вносят вклад в элемент Output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) или **DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="9be92-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="9be92-127">Количество выборок, которые необходимо уменьшить, ограничено *минимумсамплеспераутпут* и *максимумсамплеспераутпут*.</span><span class="sxs-lookup"><span data-stu-id="9be92-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="9be92-128">Тип: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="9be92-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="9be92-129">Режим интерполяции, используемый при изменении размера регионов.</span><span class="sxs-lookup"><span data-stu-id="9be92-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="9be92-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="9be92-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="9be92-131">Использует *ближайший алгоритм соседей* , который выбирает элемент ввода, ближайший к соответствующему центру пикселей для каждого выходного элемента.</span><span class="sxs-lookup"><span data-stu-id="9be92-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="9be92-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="9be92-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="9be92-133">Использует алгоритм *билинейной* , который вычисляет элемент Output, выполняя взвешенное среднее по 2 ближайшим соседним входным элементам на измерение.</span><span class="sxs-lookup"><span data-stu-id="9be92-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="9be92-134">Так как размер изменяется только для двух измерений, взвешенное среднее вычисляется по общему числу из 4 входных элементов для каждого выходного элемента.</span><span class="sxs-lookup"><span data-stu-id="9be92-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="9be92-135">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="9be92-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="9be92-136">Компонент X (или Width) коэффициента масштабирования для умножения координат *роитенсор* на, чтобы сделать их пропорциональными для *инпусеигхт* и *инпутвидс*.</span><span class="sxs-lookup"><span data-stu-id="9be92-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="9be92-137">Например, если *роитенсор* содержит нормализованные координаты (значения в диапазоне [0.. 1]), то *спатиалскалекс* обычно имеют то же значение, что и *инпутвидс*.</span><span class="sxs-lookup"><span data-stu-id="9be92-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="9be92-138">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="9be92-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="9be92-139">Компонент Y (или Height) коэффициента масштабирования для умножения координат *роитенсор* на, чтобы сделать их пропорциональными для *инпусеигхт* и *инпутвидс*.</span><span class="sxs-lookup"><span data-stu-id="9be92-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="9be92-140">Например, если *роитенсор* содержит нормализованные координаты (значения в диапазоне [0.. 1]), *спатиалскалэй* обычно имеют то же значение, что и *инпусеигхт*.</span><span class="sxs-lookup"><span data-stu-id="9be92-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="9be92-141">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="9be92-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="9be92-142">Значение для чтения из *инпуттенсор* , если РОИС выходит за границы *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="9be92-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="9be92-143">Это может произойти, если значения, полученные после масштабирования *роитенсор* по *спатиалскалекс* и *Спатиалскалэй* , больше *инпутвидс* и *инпусеигхт*.</span><span class="sxs-lookup"><span data-stu-id="9be92-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="9be92-144">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="9be92-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="9be92-145">Минимальное число выборок входных данных, используемых для каждого выходного элемента.</span><span class="sxs-lookup"><span data-stu-id="9be92-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="9be92-146">Оператор вычислит количество входных выборок `ScaledCropSize / OutputSize` , а затем получит его в *Минимумсамплеспераутпут* и *максимумсамплеспераутпут*.</span><span class="sxs-lookup"><span data-stu-id="9be92-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="9be92-147">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="9be92-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="9be92-148">Максимальное число выборок входных данных, используемых для каждого элемента Output.</span><span class="sxs-lookup"><span data-stu-id="9be92-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="9be92-149">Оператор вычислит количество входных выборок `ScaledCropSize / OutputSize` , а затем получит его в *Минимумсамплеспераутпут* и *максимумсамплеспераутпут*.</span><span class="sxs-lookup"><span data-stu-id="9be92-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="9be92-150">Доступность</span><span class="sxs-lookup"><span data-stu-id="9be92-150">Availability</span></span>
<span data-ttu-id="9be92-151">Этот оператор появился в `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="9be92-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9be92-152">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="9be92-152">Tensor constraints</span></span>
<span data-ttu-id="9be92-153">*Инпуттенсор*, *аутпуттенсор* и *Роитенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="9be92-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9be92-154">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="9be92-154">Tensor support</span></span>
| <span data-ttu-id="9be92-155">Тензорные</span><span class="sxs-lookup"><span data-stu-id="9be92-155">Tensor</span></span> | <span data-ttu-id="9be92-156">Вид</span><span class="sxs-lookup"><span data-stu-id="9be92-156">Kind</span></span> | <span data-ttu-id="9be92-157">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="9be92-157">Supported dimension counts</span></span> | <span data-ttu-id="9be92-158">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="9be92-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9be92-159">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9be92-159">InputTensor</span></span> | <span data-ttu-id="9be92-160">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9be92-160">Input</span></span> | <span data-ttu-id="9be92-161">4</span><span class="sxs-lookup"><span data-stu-id="9be92-161">4</span></span> | <span data-ttu-id="9be92-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9be92-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9be92-163">роитенсор</span><span class="sxs-lookup"><span data-stu-id="9be92-163">ROITensor</span></span> | <span data-ttu-id="9be92-164">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9be92-164">Input</span></span> | <span data-ttu-id="9be92-165">от 2 до 4</span><span class="sxs-lookup"><span data-stu-id="9be92-165">2 to 4</span></span> | <span data-ttu-id="9be92-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9be92-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9be92-167">батчиндицестенсор</span><span class="sxs-lookup"><span data-stu-id="9be92-167">BatchIndicesTensor</span></span> | <span data-ttu-id="9be92-168">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9be92-168">Input</span></span> | <span data-ttu-id="9be92-169">от 1 до 4</span><span class="sxs-lookup"><span data-stu-id="9be92-169">1 to 4</span></span> | <span data-ttu-id="9be92-170">ЗНАЧЕНИЕМ</span><span class="sxs-lookup"><span data-stu-id="9be92-170">UINT32</span></span> |
| <span data-ttu-id="9be92-171">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9be92-171">OutputTensor</span></span> | <span data-ttu-id="9be92-172">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="9be92-172">Output</span></span> | <span data-ttu-id="9be92-173">4</span><span class="sxs-lookup"><span data-stu-id="9be92-173">4</span></span> | <span data-ttu-id="9be92-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9be92-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="9be92-175">Требования</span><span class="sxs-lookup"><span data-stu-id="9be92-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9be92-176">**Header**</span><span class="sxs-lookup"><span data-stu-id="9be92-176">**Header**</span></span> | <span data-ttu-id="9be92-177">директмл. h</span><span class="sxs-lookup"><span data-stu-id="9be92-177">directml.h</span></span> |