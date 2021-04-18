---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: 'Универсальный контейнер для соединения в графе операторов Директмл, определенных [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 636556cec6fa9982ea1a30e02f6019f93b815cf8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719975"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a>Структура DML_GRAPH_EDGE_DESC (директмл. h)
Универсальный контейнер для соединения в графе операторов Директмл, определенных [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Члены

`Type`

Тип: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**

Тип границы графа. См. раздел [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) для доступных типов и [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) , где следует использовать каждый тип.


`Desc`

Тип: \_ \_ Размер поля \_ ( \_ инекспрессибле \_ ("зависимость от типа ребра")) **константа \* void**

Указатель на описание границы графа. Тип структуры, на которую указывает указатель, должен соответствовать значению, указанному в *поле Тип*.

## <a name="availability"></a>Доступность

Этот API появился в версии Директмл `1.1.0` .



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [Метод IDMLDevice1:: Компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Структура DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)