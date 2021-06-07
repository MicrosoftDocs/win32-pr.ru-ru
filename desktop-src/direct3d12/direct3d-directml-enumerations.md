---
title: Перечисления DirectML
description: Следующие перечисления объявляются в Директмл. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 11/06/2020
ms.custom: 19H1
ms.openlocfilehash: 2a761dba639ece37eba347115a831d3c6803a618
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521219"
---
# <a name="directml-enumerations"></a>Перечисления DirectML

Следующие перечисления объявляются в Директмл. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел и описание |
|-|
| [**DML_AXIS_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_axis_direction). Определяет константы, указывающие направление операции вдоль заданной оси для оператора (например, суммирование, выбор элементов Top-k, выбор минимального элемента). |
| [**DML_BINDING_TYPE**](/windows/desktop/api/directml/ne-directml-dml_binding_type). Определяет константы, указывающие характер ресурсов, на которые ссылается описание привязки [DML_BINDING_DESC структуре](/windows/desktop/api/directml/ns-directml-dml_binding_desc). |
| [**DML_CONVOLUTION_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_convolution_direction). Определяет константы, указывающие направление для оператора свертки Директмл (как описано в [структуре DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CONVOLUTION_MODE**](/windows/desktop/api/directml/ne-directml-dml_convolution_mode). Определяет константы, которые задают режим для оператора Директмл свертки (как описано в [структуре DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)). |
| [**DML_CREATE_DEVICE_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_create_device_flags). Предоставляет дополнительные варианты создания устройств для [дмлкреатедевице](/windows/desktop/api/directml/nf-directml-dmlcreatedevice). |
| [**DML_DEPTH_SPACE_ORDER**](/windows/desktop/api/directml/ne-directml-dml_depth_space_order). Определяет константы, управляющие преобразованием, применяемым в операторах Директмл [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) и **DML_OPERATOR_SPACE_TO_DEPTH1**. |
| [**DML_EXECUTION_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_execution_flags). Предоставляет параметры Директмл для управления выполнением операторов. |
| [**DML_FEATURE**](/windows/desktop/api/directml/ne-directml-dml_feature). Определяет набор дополнительных функций и возможностей, которые можно запросить с устройства Директмл. |
| [**DML_GRAPH_EDGE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_edge_type). Определяет константы, указывающие тип границы графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) . |
| [**DML_GRAPH_NODE_TYPE**](/windows/desktop/api/directml/ne-directml-dml_graph_node_type). Определяет константы, указывающие тип узла графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_NODE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_node_desc) . |
| [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode). Определяет константы, которые задают режим для Директмлного оператора-D образца 2 (как описано в [структуре DML_UPSAMPLE_2D_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_upsample_2d_operator_desc)). |
| [**DML_MATRIX_TRANSFORM**](/windows/desktop/api/directml/ne-directml-dml_matrix_transform). Определяет константы, указывающие преобразование матрицы для применения к Директмл тензорные. |
| [**DML_OPERATOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_operator_type). Определяет тип описания оператора. |
| [**DML_PADDING_MODE**](/windows/desktop/api/directml/ne-directml-dml_padding_mode). Определяет константы, которые задают режим для оператора Директмл Pad (как описано в [структуре DML_PADDING_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_padding_operator_desc)). |
| [**DML_RANDOM_GENERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_random_generator_type). Определяет константы, указывающие типы генератора случайных случайных чисел. |
| [**DML_RECURRENT_NETWORK_DIRECTION**](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction). Определяет константы, которые задают направление для перетекущего оператора Директмл. |
| [**DML_REDUCE_FUNCTION**](/windows/desktop/api/directml/ne-directml-dml_reduce_function). Определяет константы, указывающие конкретный алгоритм сокращения, используемый для оператора сокращения Директмл (как описано в [структуре DML_REDUCE_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_reduce_operator_desc)). |
| [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type). Указывает тип данных значений в тензорные. |
| [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags). Указывает дополнительные параметры в описании тензорные. |
| [**DML_TENSOR_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_type). Определяет тип описания тензорные. |

## <a name="related-topics"></a>Связанные темы

* [Справочник по DirectML](direct3d-directml-reference.md)
* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)