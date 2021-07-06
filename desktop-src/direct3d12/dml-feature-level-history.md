---
title: Журнал уровня компонентов DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282553"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="6d0d3-103">Журнал уровня компонентов DirectML</span><span class="sxs-lookup"><span data-stu-id="6d0d3-103">DirectML feature level history</span></span>

<span data-ttu-id="6d0d3-104">Общий журнал версий Директмл см. в статье [Журнал версий директмл](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="6d0d3-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="6d0d3-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="6d0d3-106">Представлено в Директмл версии 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="6d0d3-107">Добавлена поддержка следующих типов операторов, описанных в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-108">Для каждой константы типа оператора этот раздел предоставляет ссылку на соответствующую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="6d0d3-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="6d0d3-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="6d0d3-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="6d0d3-112">Расширенный тип данных и количество измерений поддерживают следующие операторы, описанные в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-113">Дополнительные сведения о конкретной поддержке, добавленной в [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), см. в разделе Структура каждого оператора.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="6d0d3-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="6d0d3-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="6d0d3-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="6d0d3-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="6d0d3-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="6d0d3-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="6d0d3-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="6d0d3-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="6d0d3-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="6d0d3-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="6d0d3-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="6d0d3-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="6d0d3-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="6d0d3-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="6d0d3-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="6d0d3-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="6d0d3-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="6d0d3-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="6d0d3-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="6d0d3-132">Представлено в Директмл версии 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="6d0d3-133">Добавлена поддержка следующих типов операторов, описанных в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-134">Для каждой константы типа оператора этот раздел предоставляет ссылку на соответствующую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="6d0d3-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="6d0d3-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="6d0d3-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="6d0d3-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="6d0d3-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="6d0d3-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="6d0d3-141">Максимальное число поддерживаемых измерений для следующих операторов увеличилось с 4 до 8.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="6d0d3-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="6d0d3-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="6d0d3-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="6d0d3-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="6d0d3-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="6d0d3-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="6d0d3-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="6d0d3-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="6d0d3-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="6d0d3-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="6d0d3-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="6d0d3-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="6d0d3-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="6d0d3-154">Представлено в Директмл версии 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="6d0d3-155">Добавлена поддержка следующих типов операторов, описанных в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-156">Для каждой константы типа оператора этот раздел предоставляет ссылку на соответствующую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="6d0d3-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="6d0d3-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="6d0d3-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="6d0d3-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="6d0d3-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="6d0d3-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="6d0d3-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="6d0d3-164">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="6d0d3-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="6d0d3-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="6d0d3-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="6d0d3-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="6d0d3-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="6d0d3-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="6d0d3-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="6d0d3-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="6d0d3-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="6d0d3-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="6d0d3-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="6d0d3-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="6d0d3-177">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-177">Added the following enhancements.</span></span>

* <span data-ttu-id="6d0d3-178">Максимальное число измерений тензорные было увеличено с 5 до 8.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="6d0d3-179">См. [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="6d0d3-180">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="6d0d3-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="6d0d3-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="6d0d3-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** и **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="6d0d3-184">**DML_OPERATOR_REDUCE** при использовании **DML_REDUCE_FUNCTION_ARGMIN** или **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="6d0d3-185">Добавлены следующие 64-разрядные типы данных, которые поддерживаются операторами SELECT.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="6d0d3-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="6d0d3-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="6d0d3-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="6d0d3-189">Устаревшие функции.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-189">Deprecated functionality.</span></span>

* <span data-ttu-id="6d0d3-190">**DML_REDUCE_FUNCTION_ARGMAX** и **DML_REDUCE_FUNCTION_ARGMIN** являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="6d0d3-191">Предпочтительно использовать в своем месте автономные операторы **DML_OPERATOR_ARGMIN** и **DML_OPERATOR_ARGMAX** .</span><span class="sxs-lookup"><span data-stu-id="6d0d3-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="6d0d3-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="6d0d3-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="6d0d3-193">Представлено в Директмл версии 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="6d0d3-194">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-194">Added the following APIs.</span></span>

* [<span data-ttu-id="6d0d3-195">Интерфейс IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="6d0d3-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="6d0d3-196">Поддержка графа операторов (см [. IDMLDevice1:: компилеграф](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="6d0d3-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="6d0d3-197">Добавлена поддержка следующих типов операторов, описанных в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-198">Для каждой константы типа оператора этот раздел предоставляет ссылку на соответствующую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="6d0d3-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="6d0d3-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="6d0d3-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="6d0d3-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="6d0d3-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="6d0d3-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="6d0d3-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="6d0d3-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="6d0d3-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="6d0d3-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="6d0d3-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="6d0d3-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="6d0d3-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="6d0d3-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="6d0d3-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="6d0d3-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="6d0d3-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="6d0d3-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="6d0d3-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="6d0d3-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="6d0d3-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="6d0d3-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="6d0d3-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="6d0d3-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="6d0d3-223">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-223">Added the following enhancements.</span></span>

* <span data-ttu-id="6d0d3-224">В следующие операторы добавлена дополнительная поддержка целочисленных типов.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="6d0d3-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="6d0d3-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="6d0d3-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="6d0d3-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="6d0d3-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="6d0d3-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="6d0d3-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="6d0d3-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="6d0d3-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="6d0d3-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="6d0d3-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="6d0d3-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="6d0d3-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="6d0d3-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="6d0d3-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="6d0d3-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="6d0d3-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="6d0d3-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="6d0d3-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="6d0d3-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="6d0d3-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="6d0d3-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="6d0d3-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="6d0d3-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="6d0d3-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="6d0d3-250">**DML_OPERATOR_TOP_K** и **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="6d0d3-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="6d0d3-252">**DML_OPERATOR_REDUCE**, при использовании одной из следующих функций reduce.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="6d0d3-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="6d0d3-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="6d0d3-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="6d0d3-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="6d0d3-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="6d0d3-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="6d0d3-259">Ослабленные тензорные ограничения фигур для **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="6d0d3-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="6d0d3-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="6d0d3-261">Представлено в Директмл версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="6d0d3-262">Добавлены следующие API.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-262">Added the following APIs.</span></span>
* [<span data-ttu-id="6d0d3-263">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="6d0d3-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="6d0d3-264">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="6d0d3-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="6d0d3-265">Запросы на уровне компонентов (см. [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="6d0d3-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="6d0d3-266">Добавлена поддержка следующих типов операторов, описанных в [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="6d0d3-267">Для каждой константы типа оператора этот раздел предоставляет ссылку на соответствующую структуру.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="6d0d3-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="6d0d3-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="6d0d3-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="6d0d3-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="6d0d3-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="6d0d3-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="6d0d3-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="6d0d3-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="6d0d3-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="6d0d3-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="6d0d3-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="6d0d3-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="6d0d3-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="6d0d3-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="6d0d3-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="6d0d3-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="6d0d3-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="6d0d3-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="6d0d3-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="6d0d3-287">Добавлены следующие усовершенствования.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-287">Added the following enhancements.</span></span>

* <span data-ttu-id="6d0d3-288">При привязке входного ресурса для отправки [идмлоператоринитиализер](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)теперь можно предоставить ресурс с [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (в дополнение к **D3D12_HEAP_TYPE_DEFAULT**) при условии, что также заданы соответствующие свойства кучи.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="6d0d3-289">См. раздел [Binding в директмл](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="6d0d3-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="6d0d3-290">Следующие логические логические операторы теперь поддерживают десятки выходных данных **UINT8** в дополнение к существующей поддержке **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="6d0d3-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="6d0d3-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="6d0d3-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="6d0d3-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="6d0d3-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="6d0d3-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="6d0d3-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="6d0d3-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="6d0d3-298">в функциях активации теперь поддерживается использование STRIDE для входных и выходных десятков.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="6d0d3-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="6d0d3-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="6d0d3-300">Уровень функций, в котором была введена Директмл.</span><span class="sxs-lookup"><span data-stu-id="6d0d3-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d0d3-301">См. также</span><span class="sxs-lookup"><span data-stu-id="6d0d3-301">See also</span></span>

* [<span data-ttu-id="6d0d3-302">Журнал версий DirectML</span><span class="sxs-lookup"><span data-stu-id="6d0d3-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="6d0d3-303">Перечисление DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="6d0d3-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="6d0d3-304">Функция DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="6d0d3-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="6d0d3-305">Структура DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="6d0d3-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
