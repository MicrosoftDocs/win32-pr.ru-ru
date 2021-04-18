---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Определяет константы, управляющие преобразованием, применяемым в операторах Директмл [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) и **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 21ab43f81a5959fc6722f5f4dedc3f60319ba642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719921"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a>Перечисление DML_DEPTH_SPACE_ORDER (директмл. h)

Определяет константы, управляющие преобразованием, применяемым в операторах Директмл [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) и **DML_OPERATOR_SPACE_TO_DEPTH1**. Они используются в структурах [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a>Константы

| Имя | Описание |
| ---- |:---- |
| DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW | Приводит к тому, что десятки, используемые в [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) , будут интерпретироваться в следующих макетах, где измерения в круглых скобках будут выровнены вместе.<br><br>- **Версия глубины**: [Пакетная, (Блоккхеигхт, Блокквидс, каналы), высота, ширина]<br>- **Версия пространства**: [Пакетная, каналы, (высота, блоккхеигхт), (ширина, блокквидс)] |
| DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH | Приводит к тому, что десятки, используемые в [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) , будут интерпретироваться в следующих макетах, где измерения в круглых скобках будут выровнены вместе.<br><br>- **Версия глубины**: [Пакетная, (каналы, Блоккхеигхт, блокквидс), высота, ширина]<br>- **Версия пространства**: [Пакетная, каналы, (высота, блоккхеигхт), (ширина, блокквидс)] |

## <a name="remarks"></a>Комментарии

Примеры, демонстрирующие последствия этих значений, см. в документации по [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) и [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a>Доступность
Это перечисление было представлено в `DML_FEATURE_LEVEL_2_1` .