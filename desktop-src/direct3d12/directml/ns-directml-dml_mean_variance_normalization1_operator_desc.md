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
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549780"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="c2c69-104">Структура DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="c2c69-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c2c69-105">Выполняет функцию нормализации значения дисперсии для входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="c2c69-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="c2c69-106">Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.</span><span class="sxs-lookup"><span data-stu-id="c2c69-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="c2c69-107">Этот оператор выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="c2c69-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="c2c69-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="c2c69-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c2c69-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c2c69-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c69-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2c69-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="c2c69-111">Участники</span><span class="sxs-lookup"><span data-stu-id="c2c69-111">Members</span></span>

`InputTensor`

<span data-ttu-id="c2c69-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c2c69-113">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="c2c69-113">A tensor containing the Input data.</span></span> <span data-ttu-id="c2c69-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="c2c69-115">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c2c69-116">Необязательный тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="c2c69-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="c2c69-117">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="c2c69-118">Измерения Скалебатчкаунт, Скалехеигхт и Скалевидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="c2c69-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="c2c69-119">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="c2c69-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="c2c69-120">Этот тензорные является обязательным, если используется *биастенсор* .</span><span class="sxs-lookup"><span data-stu-id="c2c69-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="c2c69-121">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="c2c69-122">Необязательный тензорные, содержащий данные смещения.</span><span class="sxs-lookup"><span data-stu-id="c2c69-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="c2c69-123">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="c2c69-124">Измерения Биасбатчкаунт, Биашеигхт и Биасвидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="c2c69-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="c2c69-125">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="c2c69-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="c2c69-126">Этот тензорные является обязательным, если используется *скалетенсор* .</span><span class="sxs-lookup"><span data-stu-id="c2c69-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="c2c69-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c2c69-128">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="c2c69-128">A tensor to write the results to.</span></span> <span data-ttu-id="c2c69-129">Это тензорные измерения `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="c2c69-130">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="c2c69-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="c2c69-131">Число осей.</span><span class="sxs-lookup"><span data-stu-id="c2c69-131">The number of axes.</span></span> <span data-ttu-id="c2c69-132">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="c2c69-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="c2c69-133">Тип: \_ \_ Размер поля \_ (Аксискаунт) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="c2c69-134">Оси, вдоль которых вычисляется среднее и дисперсия.</span><span class="sxs-lookup"><span data-stu-id="c2c69-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="c2c69-135">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="c2c69-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="c2c69-136">**Значение true** , если слой нормализации включает вариативность в вычислении нормализации.</span><span class="sxs-lookup"><span data-stu-id="c2c69-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="c2c69-137">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c2c69-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="c2c69-138">Если **значение равно false**, то уравнение нормализации имеет значение `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="c2c69-139">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="c2c69-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="c2c69-140">Значение Эпсилон, которое следует использовать, чтобы избежать деления на нуль.</span><span class="sxs-lookup"><span data-stu-id="c2c69-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="c2c69-141">По умолчанию рекомендуется использовать значение 0,00001.</span><span class="sxs-lookup"><span data-stu-id="c2c69-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="c2c69-142">Тип: \_ майбенулл \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c2c69-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="c2c69-143">Необязательный слой активации с плавким предохранителем, применяемый после нормализации.</span><span class="sxs-lookup"><span data-stu-id="c2c69-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c69-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2c69-144">Remarks</span></span>
<span data-ttu-id="c2c69-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** является надмножеством функций [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="c2c69-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="c2c69-146">Здесь установка массива **осей** равна `{ 0, 2, 3 }` эквиваленту параметра *кроссчаннел*  в **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; при установке массива **осей** равным значению `{ 1, 2, 3 }` *кроссчаннел* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c2c69-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="c2c69-147">Доступность</span><span class="sxs-lookup"><span data-stu-id="c2c69-147">Availability</span></span>
<span data-ttu-id="c2c69-148">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c2c69-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c2c69-149">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="c2c69-149">Tensor constraints</span></span>

<span data-ttu-id="c2c69-150">*Биастенсор*, *инпуттенсор*, *аутпуттенсор* и *Скалетенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c2c69-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c2c69-151">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="c2c69-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="c2c69-152">DML_FEATURE_LEVEL_3_1 и выше</span><span class="sxs-lookup"><span data-stu-id="c2c69-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="c2c69-153">Тензорные</span><span class="sxs-lookup"><span data-stu-id="c2c69-153">Tensor</span></span> | <span data-ttu-id="c2c69-154">Вид</span><span class="sxs-lookup"><span data-stu-id="c2c69-154">Kind</span></span> | <span data-ttu-id="c2c69-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="c2c69-155">Supported dimension counts</span></span> | <span data-ttu-id="c2c69-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="c2c69-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c2c69-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-157">InputTensor</span></span> | <span data-ttu-id="c2c69-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2c69-158">Input</span></span> | <span data-ttu-id="c2c69-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="c2c69-159">1 to 8</span></span> | <span data-ttu-id="c2c69-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-161">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-161">ScaleTensor</span></span> | <span data-ttu-id="c2c69-162">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="c2c69-162">Optional input</span></span> | <span data-ttu-id="c2c69-163">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="c2c69-163">1 to 8</span></span> | <span data-ttu-id="c2c69-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-165">биастенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-165">BiasTensor</span></span> | <span data-ttu-id="c2c69-166">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="c2c69-166">Optional input</span></span> | <span data-ttu-id="c2c69-167">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="c2c69-167">1 to 8</span></span> | <span data-ttu-id="c2c69-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-169">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-169">OutputTensor</span></span> | <span data-ttu-id="c2c69-170">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c2c69-170">Output</span></span> | <span data-ttu-id="c2c69-171">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="c2c69-171">1 to 8</span></span> | <span data-ttu-id="c2c69-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c2c69-173">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="c2c69-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="c2c69-174">Тензорные</span><span class="sxs-lookup"><span data-stu-id="c2c69-174">Tensor</span></span> | <span data-ttu-id="c2c69-175">Вид</span><span class="sxs-lookup"><span data-stu-id="c2c69-175">Kind</span></span> | <span data-ttu-id="c2c69-176">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="c2c69-176">Supported dimension counts</span></span> | <span data-ttu-id="c2c69-177">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="c2c69-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c2c69-178">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-178">InputTensor</span></span> | <span data-ttu-id="c2c69-179">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2c69-179">Input</span></span> | <span data-ttu-id="c2c69-180">4</span><span class="sxs-lookup"><span data-stu-id="c2c69-180">4</span></span> | <span data-ttu-id="c2c69-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-182">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-182">ScaleTensor</span></span> | <span data-ttu-id="c2c69-183">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="c2c69-183">Optional input</span></span> | <span data-ttu-id="c2c69-184">4</span><span class="sxs-lookup"><span data-stu-id="c2c69-184">4</span></span> | <span data-ttu-id="c2c69-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-186">биастенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-186">BiasTensor</span></span> | <span data-ttu-id="c2c69-187">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="c2c69-187">Optional input</span></span> | <span data-ttu-id="c2c69-188">4</span><span class="sxs-lookup"><span data-stu-id="c2c69-188">4</span></span> | <span data-ttu-id="c2c69-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c2c69-190">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="c2c69-190">OutputTensor</span></span> | <span data-ttu-id="c2c69-191">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="c2c69-191">Output</span></span> | <span data-ttu-id="c2c69-192">4</span><span class="sxs-lookup"><span data-stu-id="c2c69-192">4</span></span> | <span data-ttu-id="c2c69-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c2c69-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="c2c69-194">Требования</span><span class="sxs-lookup"><span data-stu-id="c2c69-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c2c69-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="c2c69-195">**Header**</span></span> | <span data-ttu-id="c2c69-196">директмл. h</span><span class="sxs-lookup"><span data-stu-id="c2c69-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="c2c69-197">См. также</span><span class="sxs-lookup"><span data-stu-id="c2c69-197">See also</span></span>

[<span data-ttu-id="c2c69-198">Использование операторов с плавким предохранителем для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="c2c69-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)