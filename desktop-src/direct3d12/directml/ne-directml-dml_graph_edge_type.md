---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Определяет константы, указывающие тип границы графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) .
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418105"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>Перечисление DML_GRAPH_EDGE_TYPE (директмл. h)

Определяет константы, указывающие тип границы графа. Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) .

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>Константы

| Имя | Описание |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | Указывает неизвестный тип грани графа и никогда не является допустимым. Использование этого значения приводит к ошибке. |
| DML_GRAPH_EDGE_TYPE_INPUT | Указывает, что ребро графа описывается структурой [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) . |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Указывает, что ребро графа описывается структурой [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) . |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Указывает, что ребро графа описывается структурой [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) .<br><br>Доступность # #<br><br>Этот API появился в версии Директмл `1.1.0` . |


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [Метод IDMLDevice1:: Компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Структура DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)     
* [Структура DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)
* [Структура DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md)
* [Структура DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md)
* [Структура DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md)