---
title: Журнал уровня компонентов DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521212"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="f770a-103">Журнал уровня компонентов DirectML</span><span class="sxs-lookup"><span data-stu-id="f770a-103">DirectML feature level history</span></span>

<span data-ttu-id="f770a-104">Общий журнал версий Директмл см. в статье [Журнал версий директмл](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f770a-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="f770a-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="f770a-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="f770a-106">Представлено в Директмл версии 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="f770a-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="f770a-107">Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="f770a-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="f770a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="f770a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="f770a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="f770a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="f770a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="f770a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="f770a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="f770a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="f770a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="f770a-114">Максимальное число поддерживаемых измерений для следующих операторов увеличилось с 4 до 8.</span><span class="sxs-lookup"><span data-stu-id="f770a-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="f770a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="f770a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="f770a-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="f770a-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="f770a-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="f770a-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="f770a-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="f770a-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="f770a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="f770a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="f770a-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="f770a-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="f770a-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="f770a-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="f770a-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="f770a-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="f770a-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="f770a-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="f770a-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="f770a-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="f770a-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="f770a-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="f770a-127">Представлено в Директмл версии 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="f770a-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="f770a-128">Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="f770a-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="f770a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="f770a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="f770a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="f770a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="f770a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="f770a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="f770a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="f770a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="f770a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="f770a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="f770a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="f770a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="f770a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="f770a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="f770a-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="f770a-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="f770a-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="f770a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="f770a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="f770a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="f770a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="f770a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="f770a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="f770a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="f770a-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="f770a-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="f770a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="f770a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="f770a-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="f770a-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="f770a-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="f770a-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="f770a-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="f770a-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="f770a-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="f770a-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="f770a-149">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="f770a-149">Added the following enhancements.</span></span>

* <span data-ttu-id="f770a-150">Максимальное число измерений тензорные было увеличено с 5 до 8.</span><span class="sxs-lookup"><span data-stu-id="f770a-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="f770a-151">См. [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f770a-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="f770a-152">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="f770a-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="f770a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="f770a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="f770a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="f770a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="f770a-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** и **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="f770a-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="f770a-156">**DML_OPERATOR_REDUCE** при использовании **DML_REDUCE_FUNCTION_ARGMIN** или **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="f770a-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="f770a-157">Добавлены следующие 64-разрядные типы данных, которые поддерживаются операторами SELECT.</span><span class="sxs-lookup"><span data-stu-id="f770a-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="f770a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="f770a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="f770a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="f770a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="f770a-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="f770a-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="f770a-161">Устаревшие функции.</span><span class="sxs-lookup"><span data-stu-id="f770a-161">Deprecated functionality.</span></span>

* <span data-ttu-id="f770a-162">**DML_REDUCE_FUNCTION_ARGMAX** и **DML_REDUCE_FUNCTION_ARGMIN** являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="f770a-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="f770a-163">Предпочтительно использовать в своем месте автономные операторы **DML_OPERATOR_ARGMIN** и **DML_OPERATOR_ARGMAX** .</span><span class="sxs-lookup"><span data-stu-id="f770a-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="f770a-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="f770a-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="f770a-165">Представлено в Директмл версии 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="f770a-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="f770a-166">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="f770a-166">Added the following APIs.</span></span>

* [<span data-ttu-id="f770a-167">Интерфейс IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="f770a-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="f770a-168">Поддержка графа операторов (см [. IDMLDevice1:: компилеграф](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="f770a-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="f770a-169">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="f770a-169">Added support for the following operators.</span></span>

* <span data-ttu-id="f770a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="f770a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="f770a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="f770a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="f770a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="f770a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="f770a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="f770a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="f770a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="f770a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="f770a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="f770a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="f770a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="f770a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="f770a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="f770a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="f770a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="f770a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="f770a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="f770a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="f770a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="f770a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="f770a-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="f770a-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="f770a-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="f770a-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="f770a-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="f770a-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="f770a-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="f770a-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="f770a-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="f770a-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="f770a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="f770a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="f770a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="f770a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="f770a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="f770a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="f770a-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="f770a-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="f770a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="f770a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="f770a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="f770a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="f770a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="f770a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="f770a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="f770a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="f770a-194">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="f770a-194">Added the following enhancements.</span></span>

* <span data-ttu-id="f770a-195">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="f770a-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="f770a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="f770a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="f770a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="f770a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="f770a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="f770a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="f770a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="f770a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="f770a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="f770a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="f770a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="f770a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="f770a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="f770a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="f770a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="f770a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="f770a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="f770a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="f770a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="f770a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="f770a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="f770a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="f770a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="f770a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="f770a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="f770a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="f770a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="f770a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="f770a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="f770a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="f770a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="f770a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="f770a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="f770a-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="f770a-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="f770a-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="f770a-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="f770a-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="f770a-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="f770a-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="f770a-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="f770a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="f770a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="f770a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="f770a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="f770a-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="f770a-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="f770a-221">**DML_OPERATOR_TOP_K** и **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="f770a-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="f770a-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="f770a-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="f770a-223">**DML_OPERATOR_REDUCE**, при использовании одной из следующих функций reduce.</span><span class="sxs-lookup"><span data-stu-id="f770a-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="f770a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="f770a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="f770a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="f770a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="f770a-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="f770a-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="f770a-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="f770a-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="f770a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="f770a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="f770a-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="f770a-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="f770a-230">Ослабленные тензорные ограничения фигур для **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="f770a-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="f770a-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="f770a-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="f770a-232">Представлено в Директмл версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="f770a-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="f770a-233">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="f770a-233">Added the following APIs.</span></span>
* [<span data-ttu-id="f770a-234">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="f770a-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="f770a-235">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f770a-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="f770a-236">Запросы на уровне компонентов (см. [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="f770a-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="f770a-237">Добавлена поддержка следующих операторов.</span><span class="sxs-lookup"><span data-stu-id="f770a-237">Added support for the following operators.</span></span>

* <span data-ttu-id="f770a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="f770a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="f770a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="f770a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="f770a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="f770a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="f770a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="f770a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="f770a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="f770a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="f770a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="f770a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="f770a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="f770a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="f770a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="f770a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="f770a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="f770a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="f770a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="f770a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="f770a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="f770a-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="f770a-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="f770a-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="f770a-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="f770a-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="f770a-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="f770a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="f770a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="f770a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="f770a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="f770a-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="f770a-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="f770a-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="f770a-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="f770a-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="f770a-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="f770a-257">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="f770a-257">Added the following enhancements.</span></span>

* <span data-ttu-id="f770a-258">При привязке входного ресурса для отправки [идмлоператоринитиализер](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)теперь можно предоставить ресурс с [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (в дополнение к **D3D12_HEAP_TYPE_DEFAULT**) при условии, что также заданы соответствующие свойства кучи.</span><span class="sxs-lookup"><span data-stu-id="f770a-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="f770a-259">См. раздел [Binding в директмл](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="f770a-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="f770a-260">Следующие логические логические операторы теперь поддерживают десятки выходных данных **UINT8** в дополнение к существующей поддержке **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="f770a-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="f770a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="f770a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="f770a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="f770a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="f770a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="f770a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="f770a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="f770a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="f770a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="f770a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="f770a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="f770a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="f770a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="f770a-268">в функциях активации теперь поддерживается использование STRIDE для входных и выходных десятков.</span><span class="sxs-lookup"><span data-stu-id="f770a-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="f770a-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="f770a-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="f770a-270">Уровень функций, в котором была введена Директмл.</span><span class="sxs-lookup"><span data-stu-id="f770a-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="f770a-271">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f770a-271">See also</span></span>

* [<span data-ttu-id="f770a-272">Журнал версий DirectML</span><span class="sxs-lookup"><span data-stu-id="f770a-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="f770a-273">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f770a-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="f770a-274">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="f770a-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="f770a-275">Структура DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="f770a-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
