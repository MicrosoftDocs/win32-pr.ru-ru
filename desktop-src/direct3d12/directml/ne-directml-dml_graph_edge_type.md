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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803802"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="9c01f-104">Перечисление DML_GRAPH_EDGE_TYPE (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="9c01f-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="9c01f-105">Определяет константы, указывающие тип границы графа.</span><span class="sxs-lookup"><span data-stu-id="9c01f-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="9c01f-106">Сведения об использовании этого перечисления см. в разделе [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c01f-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c01f-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="9c01f-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9c01f-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9c01f-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c01f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c01f-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="9c01f-110">Константы</span><span class="sxs-lookup"><span data-stu-id="9c01f-110">Constants</span></span>

| <span data-ttu-id="9c01f-111">Имя</span><span class="sxs-lookup"><span data-stu-id="9c01f-111">Name</span></span> | <span data-ttu-id="9c01f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9c01f-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="9c01f-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="9c01f-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="9c01f-114">Указывает неизвестный тип грани графа и никогда не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9c01f-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="9c01f-115">Использование этого значения приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="9c01f-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="9c01f-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="9c01f-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="9c01f-117">Указывает, что ребро графа описывается структурой [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c01f-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="9c01f-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c01f-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="9c01f-119">Указывает, что ребро графа описывается структурой [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c01f-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="9c01f-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="9c01f-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="9c01f-121">Указывает, что ребро графа описывается структурой [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c01f-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="9c01f-122">Доступность # #</span><span class="sxs-lookup"><span data-stu-id="9c01f-122">## Availability</span></span><br><br><span data-ttu-id="9c01f-123">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="9c01f-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="9c01f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9c01f-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9c01f-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="9c01f-125">**Header**</span></span> | <span data-ttu-id="9c01f-126">директмл. h</span><span class="sxs-lookup"><span data-stu-id="9c01f-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9c01f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c01f-127">See also</span></span>

* [<span data-ttu-id="9c01f-128">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="9c01f-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="9c01f-129">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="9c01f-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="9c01f-130">Структура DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="9c01f-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="9c01f-131">Структура DML_INPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="9c01f-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="9c01f-132">Структура DML_OUTPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="9c01f-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="9c01f-133">Структура DML_INTERMEDIATE_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="9c01f-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)