---
title: Константы DirectML
description: Следующие константы объявляются в `DirectML.h` .
keywords:
- Константы
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5f2d95d0eef67309ef1e5902ed6b968616b38bc081bd259d77418e950e4e028f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989604"
---
# <a name="directml-constants"></a>Константы DirectML

Следующие константы объявляются в `DirectML.h` .

| Константа | Значение | Описание |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Десятки Директмл поддерживают не более 5 измерений для DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Десятки Директмл поддерживают не более 8 измерений для DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Временные и постоянные буферы должны иметь базовый адрес, выравниваемая до 256 байт. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Для десятков буферов минимальным требованием выравнивания по базовому адресу является 16 байт. |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | Директмл. h |

## <a name="see-also"></a>См. также

* [Справочник по DirectML](direct3d-directml-reference.md)
* [Справочник по коду](direct3d-12-core-reference.md)
* [Справочник по Direct3D 12](direct3d-12-reference.md)
