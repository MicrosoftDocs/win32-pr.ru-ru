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
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417540"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="9ab24-104">Структура DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="9ab24-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9ab24-105">Выполняет функцию нормализации значения дисперсии для входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="9ab24-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="9ab24-106">Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.</span><span class="sxs-lookup"><span data-stu-id="9ab24-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="9ab24-107">Этот оператор выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="9ab24-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="9ab24-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="9ab24-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9ab24-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9ab24-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab24-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ab24-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="9ab24-111">Участники</span><span class="sxs-lookup"><span data-stu-id="9ab24-111">Members</span></span>

`InputTensor`

<span data-ttu-id="9ab24-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9ab24-113">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="9ab24-113">A tensor containing the Input data.</span></span> <span data-ttu-id="9ab24-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="9ab24-115">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9ab24-116">Необязательный тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="9ab24-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="9ab24-117">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="9ab24-118">Измерения Скалебатчкаунт, Скалехеигхт и Скалевидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="9ab24-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="9ab24-119">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="9ab24-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="9ab24-120">Этот тензорные является обязательным, если используется *биастенсор* .</span><span class="sxs-lookup"><span data-stu-id="9ab24-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="9ab24-121">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="9ab24-122">Необязательный тензорные, содержащий данные смещения.</span><span class="sxs-lookup"><span data-stu-id="9ab24-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="9ab24-123">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="9ab24-124">Измерения Биасбатчкаунт, Биашеигхт и Биасвидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="9ab24-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="9ab24-125">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="9ab24-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="9ab24-126">Этот тензорные является обязательным, если используется *скалетенсор* .</span><span class="sxs-lookup"><span data-stu-id="9ab24-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="9ab24-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9ab24-128">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="9ab24-128">A tensor to write the results to.</span></span> <span data-ttu-id="9ab24-129">Это тензорные измерения `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="9ab24-130">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="9ab24-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="9ab24-131">Число осей.</span><span class="sxs-lookup"><span data-stu-id="9ab24-131">The number of axes.</span></span> <span data-ttu-id="9ab24-132">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="9ab24-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="9ab24-133">Тип: \_ \_ Размер поля \_ (Аксискаунт) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="9ab24-134">Оси, вдоль которых вычисляется среднее и дисперсия.</span><span class="sxs-lookup"><span data-stu-id="9ab24-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="9ab24-135">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="9ab24-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="9ab24-136">**Значение true** , если слой нормализации включает вариативность в вычислении нормализации.</span><span class="sxs-lookup"><span data-stu-id="9ab24-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="9ab24-137">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9ab24-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="9ab24-138">Если **значение равно false**, то уравнение нормализации имеет значение `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="9ab24-139">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="9ab24-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="9ab24-140">Значение Эпсилон, которое следует использовать, чтобы избежать деления на нуль.</span><span class="sxs-lookup"><span data-stu-id="9ab24-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="9ab24-141">По умолчанию рекомендуется использовать значение 0,00001.</span><span class="sxs-lookup"><span data-stu-id="9ab24-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="9ab24-142">Тип: \_ майбенулл \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9ab24-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="9ab24-143">Необязательный слой активации с плавким предохранителем, применяемый после нормализации.</span><span class="sxs-lookup"><span data-stu-id="9ab24-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab24-144">Remarks</span><span class="sxs-lookup"><span data-stu-id="9ab24-144">Remarks</span></span>
<span data-ttu-id="9ab24-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** является надмножеством функций [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="9ab24-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="9ab24-146">Здесь установка массива **осей** равна `{ 0, 2, 3 }` эквиваленту параметра *кроссчаннел*  в **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; при установке массива **осей** равным значению `{ 1, 2, 3 }` *кроссчаннел* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="9ab24-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="9ab24-147">Доступность</span><span class="sxs-lookup"><span data-stu-id="9ab24-147">Availability</span></span>
<span data-ttu-id="9ab24-148">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="9ab24-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9ab24-149">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="9ab24-149">Tensor constraints</span></span>

<span data-ttu-id="9ab24-150">*Биастенсор*, *инпуттенсор*, *аутпуттенсор* и *Скалетенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="9ab24-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9ab24-151">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="9ab24-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="9ab24-152">DML_FEATURE_LEVEL_3_1 и выше</span><span class="sxs-lookup"><span data-stu-id="9ab24-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="9ab24-153">Тензорные</span><span class="sxs-lookup"><span data-stu-id="9ab24-153">Tensor</span></span> | <span data-ttu-id="9ab24-154">Вид</span><span class="sxs-lookup"><span data-stu-id="9ab24-154">Kind</span></span> | <span data-ttu-id="9ab24-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="9ab24-155">Supported dimension counts</span></span> | <span data-ttu-id="9ab24-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="9ab24-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9ab24-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-157">InputTensor</span></span> | <span data-ttu-id="9ab24-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ab24-158">Input</span></span> | <span data-ttu-id="9ab24-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="9ab24-159">1 to 8</span></span> | <span data-ttu-id="9ab24-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-161">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-161">ScaleTensor</span></span> | <span data-ttu-id="9ab24-162">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="9ab24-162">Optional input</span></span> | <span data-ttu-id="9ab24-163">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="9ab24-163">1 to 8</span></span> | <span data-ttu-id="9ab24-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-165">биастенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-165">BiasTensor</span></span> | <span data-ttu-id="9ab24-166">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="9ab24-166">Optional input</span></span> | <span data-ttu-id="9ab24-167">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="9ab24-167">1 to 8</span></span> | <span data-ttu-id="9ab24-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-169">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-169">OutputTensor</span></span> | <span data-ttu-id="9ab24-170">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="9ab24-170">Output</span></span> | <span data-ttu-id="9ab24-171">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="9ab24-171">1 to 8</span></span> | <span data-ttu-id="9ab24-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="9ab24-173">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="9ab24-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="9ab24-174">Тензорные</span><span class="sxs-lookup"><span data-stu-id="9ab24-174">Tensor</span></span> | <span data-ttu-id="9ab24-175">Вид</span><span class="sxs-lookup"><span data-stu-id="9ab24-175">Kind</span></span> | <span data-ttu-id="9ab24-176">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="9ab24-176">Supported dimension counts</span></span> | <span data-ttu-id="9ab24-177">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="9ab24-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9ab24-178">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-178">InputTensor</span></span> | <span data-ttu-id="9ab24-179">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9ab24-179">Input</span></span> | <span data-ttu-id="9ab24-180">4</span><span class="sxs-lookup"><span data-stu-id="9ab24-180">4</span></span> | <span data-ttu-id="9ab24-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-182">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-182">ScaleTensor</span></span> | <span data-ttu-id="9ab24-183">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="9ab24-183">Optional input</span></span> | <span data-ttu-id="9ab24-184">4</span><span class="sxs-lookup"><span data-stu-id="9ab24-184">4</span></span> | <span data-ttu-id="9ab24-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-186">биастенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-186">BiasTensor</span></span> | <span data-ttu-id="9ab24-187">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="9ab24-187">Optional input</span></span> | <span data-ttu-id="9ab24-188">4</span><span class="sxs-lookup"><span data-stu-id="9ab24-188">4</span></span> | <span data-ttu-id="9ab24-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="9ab24-190">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="9ab24-190">OutputTensor</span></span> | <span data-ttu-id="9ab24-191">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="9ab24-191">Output</span></span> | <span data-ttu-id="9ab24-192">4</span><span class="sxs-lookup"><span data-stu-id="9ab24-192">4</span></span> | <span data-ttu-id="9ab24-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9ab24-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="9ab24-194">Требования</span><span class="sxs-lookup"><span data-stu-id="9ab24-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9ab24-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="9ab24-195">**Header**</span></span> | <span data-ttu-id="9ab24-196">директмл. h</span><span class="sxs-lookup"><span data-stu-id="9ab24-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9ab24-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ab24-197">See also</span></span>

[<span data-ttu-id="9ab24-198">Использование операторов с плавким предохранителем для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="9ab24-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)