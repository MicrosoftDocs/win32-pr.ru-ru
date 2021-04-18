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
ms.openlocfilehash: 55b8385d3d8b6247681dd7078a04d8f5e196abd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719997"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="64bea-104">Структура DML_INTERMEDIATE_GRAPH_EDGE_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="64bea-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="64bea-105">Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="64bea-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="64bea-106">Эта структура используется для определения соединения между внутренними узлами.</span><span class="sxs-lookup"><span data-stu-id="64bea-106">This structure is used to define a connection between internal nodes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64bea-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="64bea-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="64bea-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="64bea-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64bea-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64bea-109">Syntax</span></span>
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="64bea-110">Члены</span><span class="sxs-lookup"><span data-stu-id="64bea-110">Members</span></span>

`FromNodeIndex`

<span data-ttu-id="64bea-111">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64bea-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="64bea-112">Индекс узла графа, с которого задается соединение с другим узлом.</span><span class="sxs-lookup"><span data-stu-id="64bea-112">The index of the graph node from which a connection to another node is specified.</span></span>


`FromNodeOutputIndex`

<span data-ttu-id="64bea-113">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64bea-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="64bea-114">Индекс выходных данных на узле с индексом *фромнодеиндекс* , где указано соединение.</span><span class="sxs-lookup"><span data-stu-id="64bea-114">The index of the output on the node at index *FromNodeIndex* where the connection is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="64bea-115">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64bea-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="64bea-116">Индекс узла графа, на который указывает соединение из другого узла.</span><span class="sxs-lookup"><span data-stu-id="64bea-116">The index of the graph node into which a connection from another node is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="64bea-117">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64bea-117">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="64bea-118">Индекс входных данных на узле с индексом *тонодеиндекс* , где указано соединение.</span><span class="sxs-lookup"><span data-stu-id="64bea-118">The index of the input on the node at index *ToNodeIndex* where the connection is specified.</span></span>


`Name`

<span data-ttu-id="64bea-119">Тип: \_ поле \_ z \_ \_ майбенулл \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="64bea-119">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="64bea-120">Необязательное имя для соединения графа.</span><span class="sxs-lookup"><span data-stu-id="64bea-120">An optional name for the graph connection.</span></span> <span data-ttu-id="64bea-121">Это может использоваться в некоторых сообщениях об ошибках, созданных слоем отладки Директмл.</span><span class="sxs-lookup"><span data-stu-id="64bea-121">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="64bea-122">Доступность</span><span class="sxs-lookup"><span data-stu-id="64bea-122">Availability</span></span>

<span data-ttu-id="64bea-123">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="64bea-123">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="64bea-124">Требования</span><span class="sxs-lookup"><span data-stu-id="64bea-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64bea-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="64bea-125">**Header**</span></span> | <span data-ttu-id="64bea-126">директмл. h</span><span class="sxs-lookup"><span data-stu-id="64bea-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="64bea-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64bea-127">See also</span></span>

* [<span data-ttu-id="64bea-128">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="64bea-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="64bea-129">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="64bea-129">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="64bea-130">Структура DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="64bea-130">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)