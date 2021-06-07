---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: 'Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Эта структура используется для определения соединения между внутренними узлами.'
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417436"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>Структура DML_INTERMEDIATE_GRAPH_EDGE_DESC (директмл. h)
Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Эта структура используется для определения соединения между внутренними узлами.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Участники

`FromNodeIndex`

Тип: **[uint](/windows/desktop/winprog/windows-data-types)**

Индекс узла графа, с которого задается соединение с другим узлом.


`FromNodeOutputIndex`

Тип: **[uint](/windows/desktop/winprog/windows-data-types)**

Индекс выходных данных на узле с индексом *фромнодеиндекс* , где указано соединение.


`ToNodeIndex`

Тип: **[uint](/windows/desktop/winprog/windows-data-types)**

Индекс узла графа, на который указывает соединение из другого узла.


`ToNodeInputIndex`

Тип: **[uint](/windows/desktop/winprog/windows-data-types)**

Индекс входных данных на узле с индексом *тонодеиндекс* , где указано соединение.


`Name`

Тип: \_ поле \_ z \_ \_ майбенулл \_ **const char \***

Необязательное имя для соединения графа. Это может использоваться в некоторых сообщениях об ошибках, созданных слоем отладки Директмл.

## <a name="availability"></a>Доступность

Этот API появился в версии Директмл `1.1.0` .



## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | директмл. h |

## <a name="see-also"></a>См. также раздел

* [Метод IDMLDevice1:: Компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Структура DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [Структура DML_GRAPH_EDGE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)