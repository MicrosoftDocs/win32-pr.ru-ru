---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Выполняет функцию нормализации значения дисперсии для входного тензорные. Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
f1_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719970"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="e927b-104">Структура DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e927b-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="e927b-105">Выполняет функцию нормализации значения дисперсии для входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="e927b-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="e927b-106">Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.</span><span class="sxs-lookup"><span data-stu-id="e927b-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="e927b-107">Этот оператор выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="e927b-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="e927b-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="e927b-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e927b-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e927b-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e927b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e927b-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```



## <a name="members"></a><span data-ttu-id="e927b-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e927b-111">Members</span></span>

`InputTensor`

<span data-ttu-id="e927b-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e927b-113">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="e927b-113">A tensor containing the Input data.</span></span> <span data-ttu-id="e927b-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e927b-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="e927b-115">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e927b-116">Необязательный тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="e927b-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="e927b-117">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e927b-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="e927b-118">Любое измерение можно заменить на 1 для вещания в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="e927b-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="e927b-119">Этот тензорные является обязательным, если используется *биастенсор* .</span><span class="sxs-lookup"><span data-stu-id="e927b-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="e927b-120">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e927b-121">Необязательный тензорные, содержащий данные смещения.</span><span class="sxs-lookup"><span data-stu-id="e927b-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="e927b-122">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e927b-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="e927b-123">Любое измерение можно заменить на 1 для вещания в этом измерении.</span><span class="sxs-lookup"><span data-stu-id="e927b-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="e927b-124">Этот тензорные является обязательным, если используется *скалетенсор* .</span><span class="sxs-lookup"><span data-stu-id="e927b-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="e927b-125">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e927b-126">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="e927b-126">A tensor to write the results to.</span></span> <span data-ttu-id="e927b-127">Это тензорные измерения `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e927b-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="e927b-128">Тип: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="e927b-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="e927b-129">Число осей.</span><span class="sxs-lookup"><span data-stu-id="e927b-129">The number of axes.</span></span> <span data-ttu-id="e927b-130">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="e927b-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="e927b-131">Тип: \_ \_ Размер поля \_ (Аксискаунт) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="e927b-132">Оси, вдоль которых вычисляется среднее и дисперсия.</span><span class="sxs-lookup"><span data-stu-id="e927b-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="e927b-133">Тип: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="e927b-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="e927b-134">**Значение true** , если слой нормализации включает вариативность в вычислении нормализации.</span><span class="sxs-lookup"><span data-stu-id="e927b-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="e927b-135">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e927b-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="e927b-136">Если **значение равно false**, то уравнение нормализации имеет значение `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="e927b-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="e927b-137">Тип: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="e927b-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="e927b-138">Значение Эпсилон, которое следует использовать, чтобы избежать деления на нуль.</span><span class="sxs-lookup"><span data-stu-id="e927b-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="e927b-139">По умолчанию рекомендуется использовать значение 0,00001.</span><span class="sxs-lookup"><span data-stu-id="e927b-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="e927b-140">Тип: \_ майбенулл \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e927b-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="e927b-141">Необязательный слой активации с плавким предохранителем, применяемый после нормализации.</span><span class="sxs-lookup"><span data-stu-id="e927b-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="e927b-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e927b-142">Remarks</span></span>
<span data-ttu-id="e927b-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** является надмножеством функций [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e927b-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="e927b-144">Здесь установка массива **осей** равна `{ 0, 2, 3 }` эквиваленту параметра *кроссчаннел*  в **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; при установке массива **осей** равным значению `{ 1, 2, 3 }` *кроссчаннел* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e927b-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="e927b-145">Доступность</span><span class="sxs-lookup"><span data-stu-id="e927b-145">Availability</span></span>
<span data-ttu-id="e927b-146">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e927b-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e927b-147">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e927b-147">Tensor constraints</span></span>
* <span data-ttu-id="e927b-148">*Инпуттенсор* и *аутпуттенсор* должны иметь одинаковые *размеры*.</span><span class="sxs-lookup"><span data-stu-id="e927b-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="e927b-149">*Биастенсор*, *инпуттенсор*, *аутпуттенсор* и *скалетенсор* должны иметь одинаковый *тип данных*.</span><span class="sxs-lookup"><span data-stu-id="e927b-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e927b-150">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e927b-150">Tensor support</span></span>
| <span data-ttu-id="e927b-151">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e927b-151">Tensor</span></span> | <span data-ttu-id="e927b-152">Вид</span><span class="sxs-lookup"><span data-stu-id="e927b-152">Kind</span></span> | <span data-ttu-id="e927b-153">Измерения</span><span class="sxs-lookup"><span data-stu-id="e927b-153">Dimensions</span></span> | <span data-ttu-id="e927b-154">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e927b-154">Supported dimension counts</span></span> | <span data-ttu-id="e927b-155">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e927b-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e927b-156">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e927b-156">InputTensor</span></span> | <span data-ttu-id="e927b-157">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e927b-157">Input</span></span> | <span data-ttu-id="e927b-158">{Батчкаунт, Чаннелкаунт, высота, ширина}</span><span class="sxs-lookup"><span data-stu-id="e927b-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="e927b-159">4</span><span class="sxs-lookup"><span data-stu-id="e927b-159">4</span></span> | <span data-ttu-id="e927b-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e927b-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e927b-161">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="e927b-161">ScaleTensor</span></span> | <span data-ttu-id="e927b-162">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e927b-162">Optional input</span></span> | <span data-ttu-id="e927b-163">{Скалебатчкаунт, Скалечаннелкаунт, Скалехеигхт, Скалевидс}</span><span class="sxs-lookup"><span data-stu-id="e927b-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="e927b-164">4</span><span class="sxs-lookup"><span data-stu-id="e927b-164">4</span></span> | <span data-ttu-id="e927b-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e927b-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e927b-166">биастенсор</span><span class="sxs-lookup"><span data-stu-id="e927b-166">BiasTensor</span></span> | <span data-ttu-id="e927b-167">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e927b-167">Optional input</span></span> | <span data-ttu-id="e927b-168">{Биасбатчкаунт, Биасчаннелкаунт, Биашеигхт, Биасвидс}</span><span class="sxs-lookup"><span data-stu-id="e927b-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="e927b-169">4</span><span class="sxs-lookup"><span data-stu-id="e927b-169">4</span></span> | <span data-ttu-id="e927b-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e927b-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e927b-171">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e927b-171">OutputTensor</span></span> | <span data-ttu-id="e927b-172">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e927b-172">Output</span></span> | <span data-ttu-id="e927b-173">{Батчкаунт, Чаннелкаунт, высота, ширина}</span><span class="sxs-lookup"><span data-stu-id="e927b-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="e927b-174">4</span><span class="sxs-lookup"><span data-stu-id="e927b-174">4</span></span> | <span data-ttu-id="e927b-175">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e927b-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="e927b-176">Требования</span><span class="sxs-lookup"><span data-stu-id="e927b-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e927b-177">**Header**</span><span class="sxs-lookup"><span data-stu-id="e927b-177">**Header**</span></span> | <span data-ttu-id="e927b-178">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e927b-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e927b-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e927b-179">See also</span></span>

[<span data-ttu-id="e927b-180">Использование операторов с плавким предохранителем для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="e927b-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)