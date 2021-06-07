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
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="dd45f-104">Перечисление DML_GRAPH_NODE_TYPE (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="dd45f-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="dd45f-105">Определяет константы, указывающие тип узла графа.</span><span class="sxs-lookup"><span data-stu-id="dd45f-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="dd45f-106">Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="dd45f-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd45f-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="dd45f-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="dd45f-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="dd45f-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd45f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd45f-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="dd45f-110">Константы</span><span class="sxs-lookup"><span data-stu-id="dd45f-110">Constants</span></span>

| <span data-ttu-id="dd45f-111">Имя</span><span class="sxs-lookup"><span data-stu-id="dd45f-111">Name</span></span> | <span data-ttu-id="dd45f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dd45f-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="dd45f-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="dd45f-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="dd45f-114">Указывает неизвестный тип грани графа и никогда не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="dd45f-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="dd45f-115">Использование этого значения приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="dd45f-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="dd45f-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="dd45f-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="dd45f-117">Указывает, что ребро графа описывается структурой [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="dd45f-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="dd45f-118">Доступность # #</span><span class="sxs-lookup"><span data-stu-id="dd45f-118">## Availability</span></span><br><br><span data-ttu-id="dd45f-119">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="dd45f-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="dd45f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dd45f-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dd45f-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="dd45f-121">**Header**</span></span> | <span data-ttu-id="dd45f-122">директмл. h</span><span class="sxs-lookup"><span data-stu-id="dd45f-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="dd45f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd45f-123">See also</span></span>

* [<span data-ttu-id="dd45f-124">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="dd45f-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="dd45f-125">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="dd45f-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="dd45f-126">Структура DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="dd45f-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="dd45f-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="dd45f-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)