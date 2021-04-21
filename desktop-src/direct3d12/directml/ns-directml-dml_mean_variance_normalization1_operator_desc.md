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
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803395"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="e4b94-104">Структура DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="e4b94-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e4b94-105">Выполняет функцию нормализации значения дисперсии для входного тензорные.</span><span class="sxs-lookup"><span data-stu-id="e4b94-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="e4b94-106">Этот оператор вычисляет среднее и дисперсию входных тензорные для выполнения нормализации.</span><span class="sxs-lookup"><span data-stu-id="e4b94-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="e4b94-107">Этот оператор выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="e4b94-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="e4b94-108">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="e4b94-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e4b94-109">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e4b94-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b94-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b94-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="e4b94-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e4b94-111">Members</span></span>

`InputTensor`

<span data-ttu-id="e4b94-112">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4b94-113">Объект тензорные, содержащий входные данные.</span><span class="sxs-lookup"><span data-stu-id="e4b94-113">A tensor containing the Input data.</span></span> <span data-ttu-id="e4b94-114">Размеры тензорные должны быть `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="e4b94-115">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4b94-116">Необязательный тензорные, содержащий данные шкалы.</span><span class="sxs-lookup"><span data-stu-id="e4b94-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="e4b94-117">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="e4b94-118">Измерения Скалебатчкаунт, Скалехеигхт и Скалевидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="e4b94-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="e4b94-119">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e4b94-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="e4b94-120">Этот тензорные является обязательным, если используется *биастенсор* .</span><span class="sxs-lookup"><span data-stu-id="e4b94-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="e4b94-121">Тип: \_ майбенулл \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="e4b94-122">Необязательный тензорные, содержащий данные смещения.</span><span class="sxs-lookup"><span data-stu-id="e4b94-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="e4b94-123">Если **DML_FEATURE_LEVEL** меньше **DML_FEATURE_LEVEL_4_0**, то размеры этого тензорные должны быть `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="e4b94-124">Измерения Биасбатчкаунт, Биашеигхт и Биасвидс должны либо соответствовать *инпуттенсор*, либо иметь значение 1 для автоматического вещания этих измерений во входных данных.</span><span class="sxs-lookup"><span data-stu-id="e4b94-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="e4b94-125">Если **DML_FEATURE_LEVEL** больше или равно **DML_FEATURE_LEVEL_4_0**, то любое измерение может быть установлено в 1 и автоматически рассылаться в соответствии с *инпуттенсор*.</span><span class="sxs-lookup"><span data-stu-id="e4b94-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="e4b94-126">Этот тензорные является обязательным, если используется *скалетенсор* .</span><span class="sxs-lookup"><span data-stu-id="e4b94-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="e4b94-127">Тип: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4b94-128">Объект тензорные, в который записываются результаты.</span><span class="sxs-lookup"><span data-stu-id="e4b94-128">A tensor to write the results to.</span></span> <span data-ttu-id="e4b94-129">Это тензорные измерения `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="e4b94-130">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="e4b94-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="e4b94-131">Число осей.</span><span class="sxs-lookup"><span data-stu-id="e4b94-131">The number of axes.</span></span> <span data-ttu-id="e4b94-132">Это поле определяет размер массива *осей* .</span><span class="sxs-lookup"><span data-stu-id="e4b94-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="e4b94-133">Тип: \_ \_ Размер поля \_ (Аксискаунт) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="e4b94-134">Оси, вдоль которых вычисляется среднее и дисперсия.</span><span class="sxs-lookup"><span data-stu-id="e4b94-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="e4b94-135">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a> .</b></span><span class="sxs-lookup"><span data-stu-id="e4b94-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="e4b94-136">**Значение true** , если слой нормализации включает вариативность в вычислении нормализации.</span><span class="sxs-lookup"><span data-stu-id="e4b94-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="e4b94-137">В противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e4b94-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="e4b94-138">Если **значение равно false**, то уравнение нормализации имеет значение `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="e4b94-139">Тип: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="e4b94-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="e4b94-140">Значение Эпсилон, которое следует использовать, чтобы избежать деления на нуль.</span><span class="sxs-lookup"><span data-stu-id="e4b94-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="e4b94-141">По умолчанию рекомендуется использовать значение 0,00001.</span><span class="sxs-lookup"><span data-stu-id="e4b94-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="e4b94-142">Тип: \_ майбенулл \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4b94-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="e4b94-143">Необязательный слой активации с плавким предохранителем, применяемый после нормализации.</span><span class="sxs-lookup"><span data-stu-id="e4b94-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b94-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b94-144">Remarks</span></span>
<span data-ttu-id="e4b94-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** является надмножеством функций [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="e4b94-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="e4b94-146">Здесь установка массива **осей** равна `{ 0, 2, 3 }` эквиваленту параметра *кроссчаннел*  в **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; при установке массива **осей** равным значению `{ 1, 2, 3 }` *кроссчаннел* значение **true**.</span><span class="sxs-lookup"><span data-stu-id="e4b94-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="e4b94-147">Доступность</span><span class="sxs-lookup"><span data-stu-id="e4b94-147">Availability</span></span>
<span data-ttu-id="e4b94-148">Этот оператор появился в `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e4b94-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e4b94-149">Ограничения тензорные</span><span class="sxs-lookup"><span data-stu-id="e4b94-149">Tensor constraints</span></span>

<span data-ttu-id="e4b94-150">*Биастенсор*, *инпуттенсор*, *аутпуттенсор* и *Скалетенсор* должны иметь одинаковые типы *данных* и *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="e4b94-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e4b94-151">Поддержка тензорные</span><span class="sxs-lookup"><span data-stu-id="e4b94-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="e4b94-152">DML_FEATURE_LEVEL_3_1 и выше</span><span class="sxs-lookup"><span data-stu-id="e4b94-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="e4b94-153">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e4b94-153">Tensor</span></span> | <span data-ttu-id="e4b94-154">Вид</span><span class="sxs-lookup"><span data-stu-id="e4b94-154">Kind</span></span> | <span data-ttu-id="e4b94-155">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e4b94-155">Supported dimension counts</span></span> | <span data-ttu-id="e4b94-156">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e4b94-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e4b94-157">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-157">InputTensor</span></span> | <span data-ttu-id="e4b94-158">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e4b94-158">Input</span></span> | <span data-ttu-id="e4b94-159">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e4b94-159">1 to 8</span></span> | <span data-ttu-id="e4b94-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-161">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-161">ScaleTensor</span></span> | <span data-ttu-id="e4b94-162">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e4b94-162">Optional input</span></span> | <span data-ttu-id="e4b94-163">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e4b94-163">1 to 8</span></span> | <span data-ttu-id="e4b94-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-165">биастенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-165">BiasTensor</span></span> | <span data-ttu-id="e4b94-166">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e4b94-166">Optional input</span></span> | <span data-ttu-id="e4b94-167">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e4b94-167">1 to 8</span></span> | <span data-ttu-id="e4b94-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-169">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-169">OutputTensor</span></span> | <span data-ttu-id="e4b94-170">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e4b94-170">Output</span></span> | <span data-ttu-id="e4b94-171">от 1 до 8</span><span class="sxs-lookup"><span data-stu-id="e4b94-171">1 to 8</span></span> | <span data-ttu-id="e4b94-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e4b94-173">DML_FEATURE_LEVEL_2_1 и выше</span><span class="sxs-lookup"><span data-stu-id="e4b94-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="e4b94-174">Тензорные</span><span class="sxs-lookup"><span data-stu-id="e4b94-174">Tensor</span></span> | <span data-ttu-id="e4b94-175">Вид</span><span class="sxs-lookup"><span data-stu-id="e4b94-175">Kind</span></span> | <span data-ttu-id="e4b94-176">Поддерживаемые счетчики измерений</span><span class="sxs-lookup"><span data-stu-id="e4b94-176">Supported dimension counts</span></span> | <span data-ttu-id="e4b94-177">Поддерживаемые типы данных</span><span class="sxs-lookup"><span data-stu-id="e4b94-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e4b94-178">инпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-178">InputTensor</span></span> | <span data-ttu-id="e4b94-179">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e4b94-179">Input</span></span> | <span data-ttu-id="e4b94-180">4</span><span class="sxs-lookup"><span data-stu-id="e4b94-180">4</span></span> | <span data-ttu-id="e4b94-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-182">скалетенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-182">ScaleTensor</span></span> | <span data-ttu-id="e4b94-183">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e4b94-183">Optional input</span></span> | <span data-ttu-id="e4b94-184">4</span><span class="sxs-lookup"><span data-stu-id="e4b94-184">4</span></span> | <span data-ttu-id="e4b94-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-186">биастенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-186">BiasTensor</span></span> | <span data-ttu-id="e4b94-187">Необязательный ввод</span><span class="sxs-lookup"><span data-stu-id="e4b94-187">Optional input</span></span> | <span data-ttu-id="e4b94-188">4</span><span class="sxs-lookup"><span data-stu-id="e4b94-188">4</span></span> | <span data-ttu-id="e4b94-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e4b94-190">аутпуттенсор</span><span class="sxs-lookup"><span data-stu-id="e4b94-190">OutputTensor</span></span> | <span data-ttu-id="e4b94-191">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="e4b94-191">Output</span></span> | <span data-ttu-id="e4b94-192">4</span><span class="sxs-lookup"><span data-stu-id="e4b94-192">4</span></span> | <span data-ttu-id="e4b94-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e4b94-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e4b94-194">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b94-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e4b94-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="e4b94-195">**Header**</span></span> | <span data-ttu-id="e4b94-196">директмл. h</span><span class="sxs-lookup"><span data-stu-id="e4b94-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4b94-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b94-197">See also</span></span>

[<span data-ttu-id="e4b94-198">Использование операторов с плавким предохранителем для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="e4b94-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
