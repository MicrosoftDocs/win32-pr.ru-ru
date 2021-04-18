---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: 'Универсальный контейнер для узла в графе операторов Директмл, определенных [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719998"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a><span data-ttu-id="7115d-103">Структура DML_GRAPH_NODE_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="7115d-103">DML_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="7115d-104">Универсальный контейнер для узла в графе операторов Директмл, определенных [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="7115d-104">A generic container for a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7115d-105">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="7115d-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="7115d-106">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7115d-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7115d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7115d-107">Syntax</span></span>
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="7115d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7115d-108">Members</span></span>

`Type`

<span data-ttu-id="7115d-109">Тип: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span><span class="sxs-lookup"><span data-stu-id="7115d-109">Type: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span></span>

<span data-ttu-id="7115d-110">Тип узла графа.</span><span class="sxs-lookup"><span data-stu-id="7115d-110">The type of graph node.</span></span> <span data-ttu-id="7115d-111">Доступные типы см. в разделе [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) .</span><span class="sxs-lookup"><span data-stu-id="7115d-111">See [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) for available types.</span></span>


`Desc`

<span data-ttu-id="7115d-112">Тип: \_ \_ Размер поля \_ ( \_ инекспрессибле \_ ("зависимость от типа узла")) **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="7115d-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on node type")) **const void\***</span></span>

<span data-ttu-id="7115d-113">Указатель на описание узла графа.</span><span class="sxs-lookup"><span data-stu-id="7115d-113">A pointer to the graph node description.</span></span> <span data-ttu-id="7115d-114">Тип структуры, на которую указывает указатель, должен соответствовать значению, указанному в *поле Тип*.</span><span class="sxs-lookup"><span data-stu-id="7115d-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="7115d-115">Доступность</span><span class="sxs-lookup"><span data-stu-id="7115d-115">Availability</span></span>

<span data-ttu-id="7115d-116">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="7115d-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="7115d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7115d-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7115d-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="7115d-118">**Header**</span></span> | <span data-ttu-id="7115d-119">директмл. h</span><span class="sxs-lookup"><span data-stu-id="7115d-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="7115d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7115d-120">See also</span></span>

* [<span data-ttu-id="7115d-121">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="7115d-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="7115d-122">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="7115d-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)