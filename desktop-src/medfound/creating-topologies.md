---
description: Создание топологий
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Создание топологий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423562"
---
# <a name="creating-topologies"></a><span data-ttu-id="8bd8a-103">Создание топологий</span><span class="sxs-lookup"><span data-stu-id="8bd8a-103">Creating Topologies</span></span>

<span data-ttu-id="8bd8a-104">В этом разделе описаны некоторые общие процедуры создания топологии.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="8bd8a-105">Ниже приведены общие действия по созданию топологии.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="8bd8a-106">Создайте новый объект Topology, вызвав [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="8bd8a-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="8bd8a-107">Эта функция возвращает указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) топологии.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="8bd8a-108">Изначально топология не содержит узлов.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="8bd8a-109">Чтобы создать узлы для топологии, вызовите [**мфкреатетопологиноде**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span><span class="sxs-lookup"><span data-stu-id="8bd8a-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="8bd8a-110">Эта функция возвращает указатель на интерфейс [**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) узла.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="8bd8a-111">При создании узла необходимо указать тип узла:</span><span class="sxs-lookup"><span data-stu-id="8bd8a-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="8bd8a-112">Исходный узел.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-112">Source node.</span></span>

    -   <span data-ttu-id="8bd8a-113">Узел преобразования.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-113">Transform node.</span></span>

    -   <span data-ttu-id="8bd8a-114">Выходной узел.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-114">Output node.</span></span>

    -   <span data-ttu-id="8bd8a-115">Узел Tee.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-115">Tee node.</span></span>

3.  <span data-ttu-id="8bd8a-116">Инициализируйте каждый узел.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-116">Initialize each node.</span></span> <span data-ttu-id="8bd8a-117">Процесс инициализации зависит от типа узла, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="8bd8a-118">Добавьте каждый узел в топологию, вызвав [**имфтопологи:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span><span class="sxs-lookup"><span data-stu-id="8bd8a-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="8bd8a-119">Подключите узлы.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-119">Connect the nodes.</span></span> <span data-ttu-id="8bd8a-120">Чтобы подключить узел, вызовите [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) на вышестоящем узле и передайте указатель на подчиненный узел.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="8bd8a-121">Следующие разделы содержат конкретные шаги для каждого типа узла.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="8bd8a-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="8bd8a-122">Topic</span></span>                                                    | <span data-ttu-id="8bd8a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="8bd8a-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="8bd8a-124">Создание исходных узлов</span><span class="sxs-lookup"><span data-stu-id="8bd8a-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="8bd8a-125">Создание исходного узла.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="8bd8a-126">Создание узлов преобразования</span><span class="sxs-lookup"><span data-stu-id="8bd8a-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="8bd8a-127">Создание узла преобразования.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="8bd8a-128">Создание выходных узлов</span><span class="sxs-lookup"><span data-stu-id="8bd8a-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="8bd8a-129">Создание выходного узла.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="8bd8a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8bd8a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd8a-131">Топологии</span><span class="sxs-lookup"><span data-stu-id="8bd8a-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



