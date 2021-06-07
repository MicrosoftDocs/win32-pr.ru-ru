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
# <a name="directml-feature-level-history"></a>Журнал уровня компонентов DirectML

Общий журнал версий Директмл см. в статье [Журнал версий директмл](./dml-version-history.md).

## <a name="dml_feature_level_3_1"></a>DML_FEATURE_LEVEL_3_1

Представлено в Директмл версии 1.5.0.

Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).

* **DML_OPERATOR_ELEMENT_WISE_ATAN_YX**
* **DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**
* **DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**
* **DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**
* **DML_OPERATOR_CUMULATIVE_PRODUCT**
* **DML_OPERATOR_BATCH_NORMALIZATION_GRAD**

Максимальное число поддерживаемых измерений для следующих операторов увеличилось с 4 до 8.

* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_CAST**
* **DML_OPERATOR_JOIN**
* **DML_OPERATOR_LP_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_PADDING**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_TILE**
* **DML_OPERATOR_TOP_K**
* **DML_OPERATOR_TOP_K1**

## <a name="dml_feature_level_3_0"></a>DML_FEATURE_LEVEL_3_0

Представлено в Директмл версии 1.4.0.

Добавлена поддержка следующих [операторов](/windows/win32/api/directml/ne-directml-dml_operator_type).

* **DML_OPERATOR_ELEMENT_WISE_BIT_AND**
* **DML_OPERATOR_ELEMENT_WISE_BIT_OR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_XOR**
* **DML_OPERATOR_ELEMENT_WISE_BIT_NOT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**
* **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**
* **DML_OPERATOR_ACTIVATION_CELU**
* **DML_OPERATOR_ACTIVATION_RELU_GRAD**
* **DML_OPERATOR_AVERAGE_POOLING_GRAD**
* **DML_OPERATOR_MAX_POOLING_GRAD**
* **DML_OPERATOR_RANDOM_GENERATOR**
* **DML_OPERATOR_NONZERO_COORDINATES**
* **DML_OPERATOR_RESAMPLE_GRAD**
* **DML_OPERATOR_SLICE_GRAD**
* **DML_OPERATOR_ADAM_OPTIMIZER**
* **DML_OPERATOR_ARGMIN**
* **DML_OPERATOR_ARGMAX**
* **DML_OPERATOR_ROI_ALIGN**
* **DML_OPERATOR_GATHER_ND1**

Добавлены следующие усовершенствования.

* Максимальное число измерений тензорные было увеличено с 5 до 8. См. [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).
* В следующие операторы добавлена дополнительная поддержка целочисленных типов.
  * **DML_OPERATOR_ELEMENT_WISE_POW**
  * **DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**
  * **DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** и **DML_OPERATOR_MAX_POOLING2**
  * **DML_OPERATOR_REDUCE** при использовании **DML_REDUCE_FUNCTION_ARGMIN** или **DML_REDUCE_FUNCTION_ARGMAX**
* Добавлены следующие 64-разрядные типы данных, которые поддерживаются операторами SELECT.
  * **DML_TENSOR_DATA_TYPE_FLOAT64**
  * **DML_TENSOR_DATA_TYPE_UINT64**
  * **DML_TENSOR_DATA_TYPE_INT64**

Устаревшие функции.

* **DML_REDUCE_FUNCTION_ARGMAX** и **DML_REDUCE_FUNCTION_ARGMIN** являются устаревшими. Предпочтительно использовать в своем месте автономные операторы **DML_OPERATOR_ARGMIN** и **DML_OPERATOR_ARGMAX** .

## <a name="dml_feature_level_2_1"></a>DML_FEATURE_LEVEL_2_1

Представлено в Директмл версии 1.2.0.

Добавлены следующие API.

* [Интерфейс IDMLDevice1](./directml/nn-directml-idmldevice1.md)
* Поддержка графа операторов (см [. IDMLDevice1:: компилеграф](./directml/nf-directml-idmldevice1-compilegraph.md)

Добавлена поддержка следующих операторов.

* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**
* **DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**
* **DML_OPERATOR_ELEMENT_WISE_ROUND**
* **DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**
* **DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**
* **DML_OPERATOR_FILL_VALUE_CONSTANT**
* **DML_OPERATOR_FILL_VALUE_SEQUENCE**
* **DML_OPERATOR_CUMULATIVE_SUMMATION**
* **DML_OPERATOR_REVERSE_SUBSEQUENCES**
* **DML_OPERATOR_GATHER_ELEMENTS**
* **DML_OPERATOR_GATHER_ND**
* **DML_OPERATOR_SCATTER_ND**
* **DML_OPERATOR_MAX_POOLING2**
* **DML_OPERATOR_SLICE1**
* **DML_OPERATOR_TOP_K1**
* **DML_OPERATOR_DEPTH_TO_SPACE1**
* **DML_OPERATOR_SPACE_TO_DEPTH1**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_RESAMPLE1**
* **DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**
* **DML_OPERATOR_CONVOLUTION_INTEGER**
* **DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**

Добавлены следующие усовершенствования.

* В следующие операторы добавлена дополнительная поддержка целочисленных типов.
  * **DML_OPERATOR_ELEMENT_WISE_IDENTITY**
  * **DML_OPERATOR_ELEMENT_WISE_ABS**
  * **DML_OPERATOR_ELEMENT_WISE_ADD**
  * **DML_OPERATOR_ELEMENT_WISE_CLIP**
  * **DML_OPERATOR_ELEMENT_WISE_DIVIDE**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_MAX**
  * **DML_OPERATOR_ELEMENT_WISE_MEAN**
  * **DML_OPERATOR_ELEMENT_WISE_MIN**
  * **DML_OPERATOR_ELEMENT_WISE_MULTIPLY**
  * **DML_OPERATOR_ELEMENT_WISE_SUBTRACT**
  * **DML_OPERATOR_ELEMENT_WISE_THRESHOLD**
  * **DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**
  * **DML_OPERATOR_ELEMENT_WISE_SIGN**
  * **DML_OPERATOR_ELEMENT_WISE_IF**
  * **DML_OPERATOR_ACTIVATION_SHRINK**
  * **DML_OPERATOR_PADDING**
  * **DML_OPERATOR_GATHER**
  * **DML_OPERATOR_SCATTER**
  * **DML_OPERATOR_DEPTH_TO_SPACE**
  * **DML_OPERATOR_SPACE_TO_DEPTH**
  * **DML_OPERATOR_TILE**
  * **DML_OPERATOR_TOP_K** и **DML_OPERATOR_TOP_K1**
  * **DML_OPERATOR_ONE_HOT**
  * **DML_OPERATOR_REDUCE**, при использовании одной из следующих функций reduce.
    * **DML_REDUCE_FUNCTION_ARGMIN**
    * **DML_REDUCE_FUNCTION_ARGMAX**
    * **DML_REDUCE_FUNCTION_MAX**
    * **DML_REDUCE_FUNCTION_MIN**
    * **DML_REDUCE_FUNCTION_MULTIPLY**
    * **DML_REDUCE_FUNCTION_SUM**
* Ослабленные тензорные ограничения фигур для **DML_OPERATOR_GATHER**

## <a name="dml_feature_level_2_0"></a>DML_FEATURE_LEVEL_2_0

Представлено в Директмл версии 1.1.0.

Добавлены следующие API.
* [Функция DMLCreateDevice1](./directml/nf-directml-dmlcreatedevice1.md)
* [Перечисление DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* Запросы на уровне компонентов (см. [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))

Добавлена поддержка следующих операторов.

* **DML_OPERATOR_ELEMENT_WISE_SIGN**
* **DML_OPERATOR_ELEMENT_WISE_IS_NAN**
* **DML_OPERATOR_ELEMENT_WISE_ERF**
* **DML_OPERATOR_ELEMENT_WISE_SINH**
* **DML_OPERATOR_ELEMENT_WISE_COSH**
* **DML_OPERATOR_ELEMENT_WISE_TANH**
* **DML_OPERATOR_ELEMENT_WISE_ASINH**
* **DML_OPERATOR_ELEMENT_WISE_ACOSH**
* **DML_OPERATOR_ELEMENT_WISE_ATANH**
* **DML_OPERATOR_ELEMENT_WISE_IF**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_MAX_POOLING1**
* **DML_OPERATOR_MAX_UNPOOLING**
* **DML_OPERATOR_DIAGONAL_MATRIX**
* **DML_OPERATOR_SCATTER_ELEMENTS**
* **DML_OPERATOR_SCATTER**
* **DML_OPERATOR_ONE_HOT**
* **DML_OPERATOR_RESAMPLE**

Добавлены следующие усовершенствования.

* При привязке входного ресурса для отправки [идмлоператоринитиализер](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)теперь можно предоставить ресурс с [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (в дополнение к **D3D12_HEAP_TYPE_DEFAULT**) при условии, что также заданы соответствующие свойства кучи. См. раздел [Binding в директмл](./dml-binding.md).
* Следующие логические логические операторы теперь поддерживают десятки выходных данных **UINT8** в дополнение к существующей поддержке **UINT32**.
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**
  * **DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**
* в функциях активации теперь поддерживается использование STRIDE для входных и выходных десятков.

## <a name="dml_feature_level_1_0"></a>DML_FEATURE_LEVEL_1_0

Уровень функций, в котором была введена Директмл.

## <a name="see-also"></a>См. также раздел

* [Журнал версий DirectML](./dml-version-history.md)
* [Перечисление DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Функция DMLCreateDevice1](./directml/nf-directml-dmlcreatedevice1.md)
* [Структура DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
