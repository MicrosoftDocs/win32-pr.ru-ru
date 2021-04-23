---
description: Создание топологий с помощью Топоедит
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Создание топологий с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143276"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="32902-103">Создание топологий с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="32902-104">Топология должна содержать следующие три узла:</span><span class="sxs-lookup"><span data-stu-id="32902-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="32902-105">Исходный узел: потоки из файла мультимедиа, которые используются в качестве источника топологии.</span><span class="sxs-lookup"><span data-stu-id="32902-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="32902-106">Узел преобразования: преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="32902-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="32902-107">Эти узлы обычно представляют собой кодировщики, декодеры и эффекты для топологии.</span><span class="sxs-lookup"><span data-stu-id="32902-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="32902-108">Выходной узел: приемник потока, передающий данные мультимедиа, видеокадры или звуковые потоки в сеанс мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="32902-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="32902-109">Сведения о структуре топологии см. в разделе [о топологиях](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="32902-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="32902-110">Чтобы создать топологию, необходимо добавить узлы, подключить их и разрешить топологию, чтобы ее можно было воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="32902-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="32902-111">Узлы топологии отображаются в виде прямоугольников с текстом, содержащим имя узла.</span><span class="sxs-lookup"><span data-stu-id="32902-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="32902-112">Зеленые прямоугольники представляют узлы, добавленные пользователем.</span><span class="sxs-lookup"><span data-stu-id="32902-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="32902-113">При разрешении топологии Топоедит может автоматически добавлять узлы преобразования в топологию.</span><span class="sxs-lookup"><span data-stu-id="32902-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="32902-114">Они отображаются в виде синих прямоугольников на **панели топология**.</span><span class="sxs-lookup"><span data-stu-id="32902-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="32902-115">Входные и выходные данные топологии представлены в виде черных квадратов вдоль края узла.</span><span class="sxs-lookup"><span data-stu-id="32902-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="32902-116">*Входные данные узла* отображаются в левой части узла, а *выходные данные узла* — в правой части узла.</span><span class="sxs-lookup"><span data-stu-id="32902-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="32902-117">Узлы топологии соединены через соединение с *узлом* , которое отображается как черная линия, соединяющая входные данные узла одного узла с выходными данными узла другого узла.</span><span class="sxs-lookup"><span data-stu-id="32902-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="32902-118">На следующем рисунке показана топология подключения для звукового источника.</span><span class="sxs-lookup"><span data-stu-id="32902-118">The following illustration shows a connected topology for an audio source.</span></span>

![Иллюстрация, показывающая соединения от исходного узла, два узла преобразования, а затем в выходной узел](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="32902-120">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="32902-120">This section contains the following topics:</span></span>



| <span data-ttu-id="32902-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="32902-121">Topic</span></span>                                                                                          | <span data-ttu-id="32902-122">Описание</span><span class="sxs-lookup"><span data-stu-id="32902-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="32902-123">Добавление исходных узлов с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="32902-124">Описывает процесс добавления исходных узлов в топологию.</span><span class="sxs-lookup"><span data-stu-id="32902-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="32902-125">Добавление узлов преобразования с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="32902-126">Описывает процесс добавления узлов преобразования в топологию.</span><span class="sxs-lookup"><span data-stu-id="32902-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="32902-127">Добавление выходных узлов с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="32902-128">Описывает процесс добавления выходных узлов в топологию.</span><span class="sxs-lookup"><span data-stu-id="32902-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="32902-129">Подключение и отключение узлов топологии</span><span class="sxs-lookup"><span data-stu-id="32902-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="32902-130">Описывает процесс подключения двух узлов.</span><span class="sxs-lookup"><span data-stu-id="32902-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="32902-131">Разрешение топологии с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="32902-132">Описывает процесс разрешения топологии.</span><span class="sxs-lookup"><span data-stu-id="32902-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="32902-133">См. также</span><span class="sxs-lookup"><span data-stu-id="32902-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32902-134">топоедит</span><span class="sxs-lookup"><span data-stu-id="32902-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



