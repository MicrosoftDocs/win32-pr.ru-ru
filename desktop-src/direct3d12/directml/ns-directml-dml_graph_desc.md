---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Описывает граф операторов Директмл, используемых для компиляции комбинированного, оптимизированного оператора.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418045"
---
# <a name="dml_graph_desc-structure-directmlh"></a>Структура DML_GRAPH_DESC (директмл. h)

Описывает граф операторов Директмл, используемых для компиляции комбинированного, оптимизированного оператора. См. раздел [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a>Участники

`InputCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число входов общего графа. Все входные данные графа могут быть подключены к переменному числу внутренних узлов, поэтому это может отличаться от *инпутеджекаунт*.


`OutputCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число выходов общего графа. Все выходные данные графа могут быть подключены к переменному числу внутренних узлов, поэтому это может отличаться от *аутпутеджекаунт*.


`NodeCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число внутренних узлов в графе.


`Nodes`

Тип: \_ " \_ Размер поля" \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Внутренние узлы в графе.


`InputEdgeCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число соединений между входными данными графа и входами внутренних узлов в графе.


`InputEdges`

Тип: \_ " \_ Размер поля" \_ (инпутеджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Массив соединений между входными данными графа и входными данными внутренних узлов в графе. Поле *типа* в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число соединений между выходными данными графа и выходами внутренних узлов графа.


`OutputEdges`

Тип: \_ " \_ Размер поля" \_ (аутпутеджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Массив соединений между выходными данными графа и выходами внутренних узлов графа. Поле *типа* в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)

Число внутренних соединений между узлами в графе.


`IntermediateEdges`

Тип: \_ " \_ Размер поля" \_ (интермедиатиджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Массив соединений между входными и выходными данными внутренних узлов графа. Поле типа в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Remarks
Граф, описываемый этой структурой, должен быть направленным ациклический графом. Необходимо определить соединение для ввода и вывода каждого предоставляемого узла, за исключением входных и выходных данных, которые не являются обязательными для связанного оператора.

Узлы могут использовать операторы, созданные с помощью флага [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) для определенных входных данных. Все входные операторы, использующие этот флаг, должны быть подключены к входным данным графа. Все входные операторы, подключенные к одному и тому же входным данным графа, должны использовать или опускать этот флаг эквивалентно.

Допустимо соединять операторы, подключенные входные и выходные данные которых используют разные количества измерений, размеры и типы данных. Это означает, что для каждого оператора большой двоичный объект данных тензорные интерпретируется по-разному. Однако поле *тоталтенсорсизеинбитес* в подключенных входных и выходных данных тензорные должно быть одинаковым. Операторы должны читать только регионы десятков, написанных более ранними операторами. Все области заполнения в выходных данных операции (в результате использования STRIDE) не обязательно будут считаться нулями операторами нижнего потока.

## <a name="availability"></a>Доступность

Этот API появился в версии Директмл `1.1.0` .


## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [Метод IDMLDevice1:: Компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Структура DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)
* [Структура DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)