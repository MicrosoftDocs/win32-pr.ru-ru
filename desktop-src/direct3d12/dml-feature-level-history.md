---
title: Журнал уровня компонентов DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 68633f531c627eed8b02c7f65a248213743ca8bc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803793"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="6dfd6-103">Журнал уровня компонентов DirectML</span><span class="sxs-lookup"><span data-stu-id="6dfd6-103">DirectML feature level history</span></span>

<span data-ttu-id="6dfd6-104">Общий журнал версий Директмл см. в статье [Журнал версий директмл](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6dfd6-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="6dfd6-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="6dfd6-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="6dfd6-106">Представлено в Директмл версии 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="6dfd6-107">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-107">Added support for the following operators.</span></span>

* [<span data-ttu-id="6dfd6-108">DML_OPERATOR_ELEMENT_WISE_ATAN_YX</span><span class="sxs-lookup"><span data-stu-id="6dfd6-108">DML_OPERATOR_ELEMENT_WISE_ATAN_YX</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="6dfd6-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="6dfd6-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="6dfd6-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="6dfd6-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="6dfd6-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="6dfd6-114">Максимальное число поддерживаемых измерений для следующих операторов увеличилось с 4 до 8.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="6dfd6-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="6dfd6-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="6dfd6-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="6dfd6-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="6dfd6-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="6dfd6-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="6dfd6-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="6dfd6-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="6dfd6-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="6dfd6-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="6dfd6-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="6dfd6-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="6dfd6-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="6dfd6-127">Представлено в Директмл версии 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="6dfd6-128">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-128">Added support for the following operators.</span></span>

* [<span data-ttu-id="6dfd6-129">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span><span class="sxs-lookup"><span data-stu-id="6dfd6-129">DML_OPERATOR_ELEMENT_WISE_BIT_AND</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="6dfd6-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="6dfd6-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="6dfd6-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="6dfd6-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="6dfd6-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="6dfd6-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="6dfd6-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="6dfd6-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="6dfd6-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="6dfd6-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="6dfd6-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="6dfd6-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="6dfd6-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="6dfd6-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="6dfd6-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="6dfd6-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="6dfd6-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="6dfd6-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="6dfd6-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="6dfd6-149">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-149">Added the following enhancements.</span></span>

* <span data-ttu-id="6dfd6-150">Максимальное число измерений тензорные было увеличено с 5 до 8.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="6dfd6-151">См. [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6dfd6-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="6dfd6-152">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="6dfd6-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="6dfd6-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="6dfd6-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** и **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="6dfd6-156">**DML_OPERATOR_REDUCE** при использовании **DML_REDUCE_FUNCTION_ARGMIN** или **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="6dfd6-157">Добавлены следующие 64-разрядные типы данных, которые поддерживаются операторами SELECT.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="6dfd6-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="6dfd6-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="6dfd6-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="6dfd6-161">Устаревшие функции.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-161">Deprecated functionality.</span></span>

* <span data-ttu-id="6dfd6-162">**DML_REDUCE_FUNCTION_ARGMAX** и **DML_REDUCE_FUNCTION_ARGMIN** являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="6dfd6-163">Предпочтительно использовать в своем месте автономные операторы **DML_OPERATOR_ARGMIN** и **DML_OPERATOR_ARGMAX** .</span><span class="sxs-lookup"><span data-stu-id="6dfd6-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="6dfd6-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="6dfd6-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="6dfd6-165">Представлено в Директмл версии 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="6dfd6-166">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-166">Added the following APIs.</span></span>

* [<span data-ttu-id="6dfd6-167">Интерфейс IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="6dfd6-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="6dfd6-168">Поддержка графа операторов (см [. IDMLDevice1:: компилеграф](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="6dfd6-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="6dfd6-169">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-169">Added support for the following operators.</span></span>

* <span data-ttu-id="6dfd6-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="6dfd6-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="6dfd6-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="6dfd6-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="6dfd6-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="6dfd6-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="6dfd6-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="6dfd6-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="6dfd6-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="6dfd6-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="6dfd6-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="6dfd6-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="6dfd6-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="6dfd6-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="6dfd6-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="6dfd6-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="6dfd6-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="6dfd6-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="6dfd6-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="6dfd6-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="6dfd6-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="6dfd6-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="6dfd6-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="6dfd6-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="6dfd6-194">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-194">Added the following enhancements.</span></span>

* <span data-ttu-id="6dfd6-195">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="6dfd6-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="6dfd6-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="6dfd6-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="6dfd6-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="6dfd6-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="6dfd6-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="6dfd6-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="6dfd6-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="6dfd6-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="6dfd6-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="6dfd6-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="6dfd6-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="6dfd6-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="6dfd6-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="6dfd6-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="6dfd6-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="6dfd6-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="6dfd6-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="6dfd6-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="6dfd6-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="6dfd6-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="6dfd6-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="6dfd6-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="6dfd6-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="6dfd6-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="6dfd6-221">**DML_OPERATOR_TOP_K** и **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="6dfd6-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="6dfd6-223">**DML_OPERATOR_REDUCE**, при использовании одной из следующих функций reduce.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="6dfd6-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="6dfd6-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="6dfd6-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="6dfd6-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="6dfd6-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="6dfd6-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="6dfd6-230">Ослабленные тензорные ограничения фигур для **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="6dfd6-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="6dfd6-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="6dfd6-232">Представлено в Директмл версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="6dfd6-233">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-233">Added the following APIs.</span></span>
* [<span data-ttu-id="6dfd6-234">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="6dfd6-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="6dfd6-235">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="6dfd6-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="6dfd6-236">Запросы на уровне компонентов (см. [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="6dfd6-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="6dfd6-237">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-237">Added support for the following operators.</span></span>

* <span data-ttu-id="6dfd6-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="6dfd6-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="6dfd6-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="6dfd6-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="6dfd6-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="6dfd6-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="6dfd6-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="6dfd6-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="6dfd6-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="6dfd6-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="6dfd6-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="6dfd6-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="6dfd6-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="6dfd6-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="6dfd6-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="6dfd6-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="6dfd6-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="6dfd6-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="6dfd6-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="6dfd6-257">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-257">Added the following enhancements.</span></span>

* <span data-ttu-id="6dfd6-258">При привязке входного ресурса для отправки [идмлоператоринитиализер](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)теперь можно предоставить ресурс с [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (в дополнение к **D3D12_HEAP_TYPE_DEFAULT**) при условии, что также заданы соответствующие свойства кучи.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="6dfd6-259">См. раздел [Binding в директмл](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="6dfd6-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="6dfd6-260">Следующие логические логические операторы теперь поддерживают десятки выходных данных **UINT8** в дополнение к существующей поддержке **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="6dfd6-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="6dfd6-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="6dfd6-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="6dfd6-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="6dfd6-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="6dfd6-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="6dfd6-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="6dfd6-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="6dfd6-268">в функциях активации теперь поддерживается использование STRIDE для входных и выходных десятков.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="6dfd6-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="6dfd6-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="6dfd6-270">Уровень функций, в котором была введена Директмл.</span><span class="sxs-lookup"><span data-stu-id="6dfd6-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dfd6-271">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6dfd6-271">See also</span></span>

* [<span data-ttu-id="6dfd6-272">Журнал версий DirectML</span><span class="sxs-lookup"><span data-stu-id="6dfd6-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="6dfd6-273">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="6dfd6-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="6dfd6-274">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="6dfd6-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="6dfd6-275">Структура DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="6dfd6-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)