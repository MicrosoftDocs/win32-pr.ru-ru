---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Определяет константы, указывающие тип узла графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) .
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 0bb0712370da35c4b8c9278ad7721d2ffc7d875d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417445"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a>Перечисление DML_GRAPH_NODE_TYPE (директмл. h)

Определяет константы, указывающие тип узла графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a>Константы

| Имя | Описание |
| ---- |:---- |
| DML_GRAPH_NODE_TYPE_INVALID | Указывает неизвестный тип грани графа и никогда не является допустимым. Использование этого значения приводит к ошибке. |
| DML_GRAPH_NODE_TYPE_OPERATOR | Указывает, что ребро графа описывается структурой [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) .<br><br>Доступность # #<br><br>Этот API появился в версии Директмл `1.1.0` . |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [Метод IDMLDevice1:: Компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Структура DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)     
* [Структура DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)
* [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md)