---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Декрибес узел в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и переданных в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 997f441de76a60229b76f2f7d67b7acf1a26ed5f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803560"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="2fdf6-103">Структура DML_OPERATOR_GRAPH_NODE_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="2fdf6-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="2fdf6-104">Декрибес узел в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и переданных в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="2fdf6-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="2fdf6-105">Поведение этого узла определяется оператором Директмл.</span><span class="sxs-lookup"><span data-stu-id="2fdf6-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fdf6-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="2fdf6-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2fdf6-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2fdf6-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fdf6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fdf6-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="2fdf6-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2fdf6-109">Members</span></span>

`Operator`

<span data-ttu-id="2fdf6-110">Тип: <b> [идмлоператор](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="2fdf6-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="2fdf6-111">Оператор Директмл, определяющий поведение узла.</span><span class="sxs-lookup"><span data-stu-id="2fdf6-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="2fdf6-112">Тип: \_ поле \_ z \_ \_ майбенулл \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="2fdf6-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="2fdf6-113">Необязательное имя для соединения графа.</span><span class="sxs-lookup"><span data-stu-id="2fdf6-113">An optional name for the graph connection.</span></span> <span data-ttu-id="2fdf6-114">Это может использоваться в некоторых сообщениях об ошибках, созданных слоем отладки Директмл.</span><span class="sxs-lookup"><span data-stu-id="2fdf6-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="2fdf6-115">Доступность</span><span class="sxs-lookup"><span data-stu-id="2fdf6-115">Availability</span></span>

<span data-ttu-id="2fdf6-116">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="2fdf6-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="2fdf6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2fdf6-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2fdf6-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="2fdf6-118">**Header**</span></span> | <span data-ttu-id="2fdf6-119">директмл. h</span><span class="sxs-lookup"><span data-stu-id="2fdf6-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="2fdf6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fdf6-120">See also</span></span>

* [<span data-ttu-id="2fdf6-121">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="2fdf6-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="2fdf6-122">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="2fdf6-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="2fdf6-123">Структура DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="2fdf6-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)