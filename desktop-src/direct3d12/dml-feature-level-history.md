---
title: Журнал уровня компонентов DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: fdc489184b3220afd0b8c75738fa1d40de207c8d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387053"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="65402-103">Журнал уровня компонентов DirectML</span><span class="sxs-lookup"><span data-stu-id="65402-103">DirectML feature level history</span></span>

<span data-ttu-id="65402-104">Общий журнал версий Директмл см. в статье [Журнал версий директмл](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="65402-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="65402-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="65402-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="65402-106">Представлено в Директмл версии 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="65402-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="65402-107">Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="65402-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="65402-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="65402-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="65402-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="65402-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="65402-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="65402-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="65402-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="65402-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="65402-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="65402-114">Максимальное число поддерживаемых измерений для следующих операторов увеличилось с 4 до 8.</span><span class="sxs-lookup"><span data-stu-id="65402-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="65402-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="65402-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="65402-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="65402-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="65402-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="65402-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="65402-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="65402-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="65402-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="65402-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="65402-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="65402-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="65402-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="65402-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="65402-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="65402-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="65402-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="65402-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="65402-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="65402-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="65402-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="65402-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="65402-127">Представлено в Директмл версии 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="65402-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="65402-128">Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="65402-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="65402-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="65402-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="65402-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="65402-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="65402-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="65402-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="65402-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="65402-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="65402-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="65402-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="65402-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="65402-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="65402-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="65402-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="65402-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="65402-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="65402-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="65402-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="65402-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="65402-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="65402-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="65402-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="65402-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="65402-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="65402-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="65402-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="65402-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="65402-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="65402-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="65402-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="65402-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="65402-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="65402-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="65402-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="65402-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="65402-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="65402-149">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="65402-149">Added the following enhancements.</span></span>

* <span data-ttu-id="65402-150">Максимальное число измерений тензорные было увеличено с 5 до 8.</span><span class="sxs-lookup"><span data-stu-id="65402-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="65402-151">См. [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="65402-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="65402-152">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="65402-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="65402-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="65402-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="65402-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="65402-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="65402-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** и **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="65402-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="65402-156">**DML_OPERATOR_REDUCE** при использовании **DML_REDUCE_FUNCTION_ARGMIN** или **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="65402-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="65402-157">Добавлены следующие 64-разрядные типы данных, которые поддерживаются операторами SELECT.</span><span class="sxs-lookup"><span data-stu-id="65402-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="65402-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="65402-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="65402-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="65402-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="65402-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="65402-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="65402-161">Устаревшие функции.</span><span class="sxs-lookup"><span data-stu-id="65402-161">Deprecated functionality.</span></span>

* <span data-ttu-id="65402-162">**DML_REDUCE_FUNCTION_ARGMAX** и **DML_REDUCE_FUNCTION_ARGMIN** являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="65402-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="65402-163">Предпочтительно использовать в своем месте автономные операторы **DML_OPERATOR_ARGMIN** и **DML_OPERATOR_ARGMAX** .</span><span class="sxs-lookup"><span data-stu-id="65402-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="65402-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="65402-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="65402-165">Представлено в Директмл версии 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="65402-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="65402-166">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="65402-166">Added the following APIs.</span></span>

* [<span data-ttu-id="65402-167">Интерфейс IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="65402-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="65402-168">Поддержка графа операторов (см [. IDMLDevice1:: компилеграф](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="65402-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="65402-169">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="65402-169">Added support for the following operators.</span></span>

* <span data-ttu-id="65402-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="65402-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="65402-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="65402-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="65402-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="65402-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="65402-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="65402-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="65402-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="65402-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="65402-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="65402-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="65402-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="65402-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="65402-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="65402-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="65402-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="65402-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="65402-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="65402-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="65402-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="65402-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="65402-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="65402-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="65402-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="65402-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="65402-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="65402-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="65402-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="65402-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="65402-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="65402-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="65402-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="65402-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="65402-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="65402-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="65402-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="65402-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="65402-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="65402-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="65402-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="65402-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="65402-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="65402-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="65402-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="65402-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="65402-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="65402-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="65402-194">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="65402-194">Added the following enhancements.</span></span>

* <span data-ttu-id="65402-195">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="65402-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="65402-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="65402-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="65402-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="65402-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="65402-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="65402-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="65402-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="65402-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="65402-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="65402-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="65402-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="65402-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="65402-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="65402-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="65402-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="65402-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="65402-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="65402-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="65402-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="65402-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="65402-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="65402-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="65402-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="65402-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="65402-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="65402-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="65402-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="65402-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="65402-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="65402-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="65402-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="65402-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="65402-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="65402-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="65402-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="65402-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="65402-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="65402-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="65402-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="65402-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="65402-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="65402-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="65402-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="65402-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="65402-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="65402-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="65402-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="65402-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="65402-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="65402-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="65402-221">**DML_OPERATOR_TOP_K** и **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="65402-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="65402-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="65402-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="65402-223">**DML_OPERATOR_REDUCE**, при использовании одной из следующих функций reduce.</span><span class="sxs-lookup"><span data-stu-id="65402-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="65402-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="65402-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="65402-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="65402-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="65402-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="65402-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="65402-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="65402-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="65402-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="65402-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="65402-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="65402-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="65402-230">Ослабленные тензорные ограничения фигур для **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="65402-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="65402-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="65402-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="65402-232">Представлено в Директмл версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="65402-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="65402-233">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="65402-233">Added the following APIs.</span></span>
* [<span data-ttu-id="65402-234">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="65402-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="65402-235">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="65402-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="65402-236">Запросы на уровне компонентов (см. [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="65402-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="65402-237">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="65402-237">Added support for the following operators.</span></span>

* <span data-ttu-id="65402-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="65402-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="65402-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="65402-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="65402-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="65402-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="65402-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="65402-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="65402-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="65402-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="65402-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="65402-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="65402-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="65402-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="65402-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="65402-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="65402-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="65402-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="65402-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="65402-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="65402-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="65402-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="65402-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="65402-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="65402-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="65402-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="65402-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="65402-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="65402-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="65402-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="65402-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="65402-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="65402-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="65402-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="65402-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="65402-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="65402-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="65402-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="65402-257">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="65402-257">Added the following enhancements.</span></span>

* <span data-ttu-id="65402-258">При привязке входного ресурса для отправки [идмлоператоринитиализер](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)теперь можно предоставить ресурс с [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (в дополнение к **D3D12_HEAP_TYPE_DEFAULT**) при условии, что также заданы соответствующие свойства кучи.</span><span class="sxs-lookup"><span data-stu-id="65402-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="65402-259">См. раздел [Binding в директмл](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="65402-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="65402-260">Следующие логические логические операторы теперь поддерживают десятки выходных данных **UINT8** в дополнение к существующей поддержке **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="65402-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="65402-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="65402-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="65402-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="65402-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="65402-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="65402-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="65402-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="65402-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="65402-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="65402-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="65402-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="65402-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="65402-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="65402-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="65402-268">в функциях активации теперь поддерживается использование STRIDE для входных и выходных десятков.</span><span class="sxs-lookup"><span data-stu-id="65402-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="65402-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="65402-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="65402-270">Уровень функций, в котором была введена Директмл.</span><span class="sxs-lookup"><span data-stu-id="65402-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="65402-271">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65402-271">See also</span></span>

* [<span data-ttu-id="65402-272">Журнал версий DirectML</span><span class="sxs-lookup"><span data-stu-id="65402-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="65402-273">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="65402-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="65402-274">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="65402-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="65402-275">Структура DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="65402-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
