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
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719976"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="deee2-103">Структура DML_GRAPH_DESC (директмл. h)</span><span class="sxs-lookup"><span data-stu-id="deee2-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="deee2-104">Описывает граф операторов Директмл, используемых для компиляции комбинированного, оптимизированного оператора.</span><span class="sxs-lookup"><span data-stu-id="deee2-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="deee2-105">См. раздел [IDMLDevice1:: компилеграф](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="deee2-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="deee2-106">Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="deee2-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="deee2-107">См. также [Журнал версий директмл](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="deee2-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="deee2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deee2-108">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="deee2-109">Члены</span><span class="sxs-lookup"><span data-stu-id="deee2-109">Members</span></span>

`InputCount`

<span data-ttu-id="deee2-110">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-111">Число входов общего графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="deee2-112">Все входные данные графа могут быть подключены к переменному числу внутренних узлов, поэтому это может отличаться от *инпутеджекаунт*.</span><span class="sxs-lookup"><span data-stu-id="deee2-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="deee2-113">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-114">Число выходов общего графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="deee2-115">Все выходные данные графа могут быть подключены к переменному числу внутренних узлов, поэтому это может отличаться от *аутпутеджекаунт*.</span><span class="sxs-lookup"><span data-stu-id="deee2-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="deee2-116">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-117">Число внутренних узлов в графе.</span><span class="sxs-lookup"><span data-stu-id="deee2-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="deee2-118">Тип: \_ " \_ Размер поля" \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="deee2-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="deee2-119">Внутренние узлы в графе.</span><span class="sxs-lookup"><span data-stu-id="deee2-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="deee2-120">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-121">Число соединений между входными данными графа и входами внутренних узлов в графе.</span><span class="sxs-lookup"><span data-stu-id="deee2-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="deee2-122">Тип: \_ " \_ Размер поля" \_ (инпутеджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="deee2-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="deee2-123">Массив соединений между входными данными графа и входными данными внутренних узлов в графе.</span><span class="sxs-lookup"><span data-stu-id="deee2-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="deee2-124">Поле *типа* в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="deee2-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="deee2-125">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-126">Число соединений между выходными данными графа и выходами внутренних узлов графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="deee2-127">Тип: \_ " \_ Размер поля" \_ (аутпутеджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="deee2-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="deee2-128">Массив соединений между выходными данными графа и выходами внутренних узлов графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="deee2-129">Поле *типа* в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="deee2-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="deee2-130">Тип: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="deee2-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="deee2-131">Число внутренних соединений между узлами в графе.</span><span class="sxs-lookup"><span data-stu-id="deee2-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="deee2-132">Тип: \_ " \_ Размер поля" \_ (интермедиатиджекаунт) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="deee2-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="deee2-133">Массив соединений между входными и выходными данными внутренних узлов графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="deee2-134">Поле типа в каждом элементе должно иметь значение [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="deee2-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="deee2-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="deee2-135">Remarks</span></span>
<span data-ttu-id="deee2-136">Граф, описываемый этой структурой, должен быть направленным ациклический графом.</span><span class="sxs-lookup"><span data-stu-id="deee2-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="deee2-137">Необходимо определить соединение для ввода и вывода каждого предоставляемого узла, за исключением входных и выходных данных, которые не являются обязательными для связанного оператора.</span><span class="sxs-lookup"><span data-stu-id="deee2-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="deee2-138">Узлы могут использовать операторы, созданные с помощью флага [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) для определенных входных данных.</span><span class="sxs-lookup"><span data-stu-id="deee2-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="deee2-139">Все входные операторы, использующие этот флаг, должны быть подключены к входным данным графа.</span><span class="sxs-lookup"><span data-stu-id="deee2-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="deee2-140">Все входные операторы, подключенные к одному и тому же входным данным графа, должны использовать или опускать этот флаг эквивалентно.</span><span class="sxs-lookup"><span data-stu-id="deee2-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="deee2-141">Допустимо соединять операторы, подключенные входные и выходные данные которых используют разные количества измерений, размеры и типы данных.</span><span class="sxs-lookup"><span data-stu-id="deee2-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="deee2-142">Это означает, что для каждого оператора большой двоичный объект данных тензорные интерпретируется по-разному.</span><span class="sxs-lookup"><span data-stu-id="deee2-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="deee2-143">Однако поле *тоталтенсорсизеинбитес* в подключенных входных и выходных данных тензорные должно быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="deee2-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="deee2-144">Операторы должны читать только регионы десятков, написанных более ранними операторами.</span><span class="sxs-lookup"><span data-stu-id="deee2-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="deee2-145">Все области заполнения в выходных данных операции (в результате использования STRIDE) не обязательно будут считаться нулями операторами нижнего потока.</span><span class="sxs-lookup"><span data-stu-id="deee2-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="deee2-146">Доступность</span><span class="sxs-lookup"><span data-stu-id="deee2-146">Availability</span></span>

<span data-ttu-id="deee2-147">Этот API появился в версии Директмл `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="deee2-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="deee2-148">Требования</span><span class="sxs-lookup"><span data-stu-id="deee2-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="deee2-149">**Header**</span><span class="sxs-lookup"><span data-stu-id="deee2-149">**Header**</span></span> | <span data-ttu-id="deee2-150">директмл. h</span><span class="sxs-lookup"><span data-stu-id="deee2-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="deee2-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="deee2-151">See also</span></span>

* [<span data-ttu-id="deee2-152">Метод IDMLDevice1:: Компилеграф</span><span class="sxs-lookup"><span data-stu-id="deee2-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="deee2-153">Структура DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="deee2-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="deee2-154">Структура DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="deee2-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)