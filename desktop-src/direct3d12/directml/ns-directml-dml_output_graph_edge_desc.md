---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: 'Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Эта структура используется для определения соединения из выходных данных внутреннего узла к выходным данным графа.'
helpviewer_keywords:
- DML_OUTPUT_GRAPH_EDGE_DESC
- DML_OUTPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_output_graph_edge_desc
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 55d234fcf487e7ad92b39b60d43eb992b46d0d2c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417524"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="9682c-104">Структура DML_OUTPUT_GRAPH_EDGE_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="9682c-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="9682c-105">Описывает соединение в графе операторов Директмл, определенных [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) и передаваемых в [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="9682c-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="9682c-106">Эта структура используется для определения соединения из выходных данных внутреннего узла к выходным данным графа.</span><span class="sxs-lookup"><span data-stu-id="9682c-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9682c-107">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="9682c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9682c-108">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9682c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9682c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9682c-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="9682c-110">Участники</span><span class="sxs-lookup"><span data-stu-id="9682c-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="9682c-111">Тип: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9682c-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="9682c-112">Индекс выходных данных графа, к которому задается соединение из выходных данных внутреннего узла.</span><span class="sxs-lookup"><span data-stu-id="9682c-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="9682c-113">Тип: \_ поле \_ z \_ \_ майбенулл \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="9682c-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="9682c-114">Необязательное имя для соединения графа.</span><span class="sxs-lookup"><span data-stu-id="9682c-114">An optional name for the graph connection.</span></span> <span data-ttu-id="9682c-115">Это может использоваться в некоторых сообщениях об ошибках, созданных слоем отладки Директмл.</span><span class="sxs-lookup"><span data-stu-id="9682c-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="9682c-116">Доступность</span><span class="sxs-lookup"><span data-stu-id="9682c-116">Availability</span></span>

<span data-ttu-id="9682c-117">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="9682c-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="9682c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9682c-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9682c-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="9682c-119">**Header**</span></span> | <span data-ttu-id="9682c-120">директмл. h</span><span class="sxs-lookup"><span data-stu-id="9682c-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9682c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9682c-121">See also</span></span>

* [<span data-ttu-id="9682c-122">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="9682c-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="9682c-123">Структура DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="9682c-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="9682c-124">Структура DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="9682c-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)