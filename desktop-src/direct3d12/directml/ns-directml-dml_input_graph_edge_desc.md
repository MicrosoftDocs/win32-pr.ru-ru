---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: 'Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Эта структура используется для определения соединения из входных данных графа с входными данными внутреннего узла.'
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417429"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="dc4fe-104">Структура DML_INPUT_GRAPH_EDGE_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="dc4fe-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="dc4fe-105">Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="dc4fe-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="dc4fe-106">Эта структура используется для определения соединения из входных данных графа с входными данными внутреннего узла.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc4fe-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="dc4fe-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="dc4fe-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="dc4fe-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4fe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc4fe-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="dc4fe-110">Участники</span><span class="sxs-lookup"><span data-stu-id="dc4fe-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="dc4fe-111">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="dc4fe-112">Индекс входных данных графа, из которого задается соединение с входными данными внутреннего узла.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="dc4fe-113">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="dc4fe-114">Индекс внутреннего узла, на который задается соединение из входных данных графа.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="dc4fe-115">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="dc4fe-116">Индекс входных данных на внутреннем узле, где указано соединение.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="dc4fe-117">Тип: \_ поле \_ z \_ \_ майбенулл \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="dc4fe-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="dc4fe-118">Необязательное имя для соединения графа.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-118">An optional name for the graph connection.</span></span> <span data-ttu-id="dc4fe-119">Это может использоваться в некоторых сообщениях об ошибках, созданных слоем отладки Директмл.</span><span class="sxs-lookup"><span data-stu-id="dc4fe-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="dc4fe-120">Доступность</span><span class="sxs-lookup"><span data-stu-id="dc4fe-120">Availability</span></span>

<span data-ttu-id="dc4fe-121">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="dc4fe-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="dc4fe-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dc4fe-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dc4fe-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="dc4fe-123">**Header**</span></span> | <span data-ttu-id="dc4fe-124">директмл. h</span><span class="sxs-lookup"><span data-stu-id="dc4fe-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="dc4fe-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc4fe-125">See also</span></span>

* [<span data-ttu-id="dc4fe-126">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="dc4fe-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="dc4fe-127">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="dc4fe-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="dc4fe-128">Структура DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="dc4fe-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)