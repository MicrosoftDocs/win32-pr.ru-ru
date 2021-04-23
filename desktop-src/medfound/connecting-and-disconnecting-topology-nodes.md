---
description: Подключение и отключение узлов топологии
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Подключение и отключение узлов топологии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701325"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="9fbb0-103">Подключение и отключение узлов топологии</span><span class="sxs-lookup"><span data-stu-id="9fbb0-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="9fbb0-104">Чтобы топология была функциональной, необходимо подключить исходный узел и выходной узел.</span><span class="sxs-lookup"><span data-stu-id="9fbb0-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="9fbb0-105">Чтобы подключить два узла топологии, перетащите выходные данные узла одного узла в входные данные узла другого узла.</span><span class="sxs-lookup"><span data-stu-id="9fbb0-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="9fbb0-106">Топоедит отображает соединение узла в виде черной линии.</span><span class="sxs-lookup"><span data-stu-id="9fbb0-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="9fbb0-107">Это эквивалентно соединению узлов топологии путем вызова метода [**имфтопологиноде:: коннектаутпут**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .</span><span class="sxs-lookup"><span data-stu-id="9fbb0-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="9fbb0-108">Топологию можно разрешить только в том случае, если соединение с узлом является допустимым. то есть, если типы носителей двух узлов совместимы.</span><span class="sxs-lookup"><span data-stu-id="9fbb0-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="9fbb0-109">Сведения об устранении топологий см. в разделе [разрешение топологии с помощью топоедит](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="9fbb0-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="9fbb0-110">При попытке установить соединение с уже подключенным узлом подключение нового узла заменяет старое соединение с узлом.</span><span class="sxs-lookup"><span data-stu-id="9fbb0-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="9fbb0-111">Чтобы удалить подключение, выберите соединение с узлом и нажмите клавишу DELETE или выберите **Удалить** в меню **топология** .</span><span class="sxs-lookup"><span data-stu-id="9fbb0-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fbb0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9fbb0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbb0-113">Создание топологий с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="9fbb0-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="9fbb0-114">топоедит</span><span class="sxs-lookup"><span data-stu-id="9fbb0-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



