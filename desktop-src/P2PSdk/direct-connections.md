---
description: Инфраструктуры одноранговых схем и одноранговых групп позволяют приложениям напрямую подключаться к одному узлу (графике) или члену (группированию), а затем напрямую обмениваться данными с узлом. Это соединение называется прямым соединением.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Прямые подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663355"
---
# <a name="direct-connections"></a><span data-ttu-id="69de9-104">Прямые подключения</span><span class="sxs-lookup"><span data-stu-id="69de9-104">Direct Connections</span></span>

<span data-ttu-id="69de9-105">Инфраструктуры одноранговых схем и одноранговых групп позволяют приложениям напрямую подключаться к одному узлу (графике) или члену (группированию), а затем напрямую обмениваться данными с узлом.</span><span class="sxs-lookup"><span data-stu-id="69de9-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="69de9-106">Это соединение называется **прямым соединением**.</span><span class="sxs-lookup"><span data-stu-id="69de9-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="69de9-107">Прямые подключения с помощью инфраструктуры одноранговых диаграмм</span><span class="sxs-lookup"><span data-stu-id="69de9-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="69de9-108">Прежде чем можно будет установить прямое соединение между двумя узлами в графе, оба узла должны быть зарегистрированы для **события \_ \_ \_ прямого \_ подключения однорангового графа** .</span><span class="sxs-lookup"><span data-stu-id="69de9-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="69de9-109">Для получения данных через прямое подключение узлы также должны быть зарегистрированы для события « **\_ \_ \_ входные \_ данные события однорангового графа** ».</span><span class="sxs-lookup"><span data-stu-id="69de9-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="69de9-110">**Одноранговая сеть \_ \_ \_ Прямое \_ соединение с событием Graph** — это событие, которое уведомляет приложение о том, успешно ли выполнена или неудачная попытка прямого подключения.</span><span class="sxs-lookup"><span data-stu-id="69de9-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="69de9-111">Фактическое состояние успеха или сбоя вызова [**пирграфопендиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) возвращается в структуре [**\_ \_ \_ данных события однорангового графа**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .</span><span class="sxs-lookup"><span data-stu-id="69de9-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="69de9-112">Чтобы создать прямое соединение, приложение вызывает [**пирграфопендиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), а затем передает в граф маркер, указатель на удостоверение другого узла, участвующего в соединении, и указатель на структуру IPv6-адреса для участвующего узла.</span><span class="sxs-lookup"><span data-stu-id="69de9-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="69de9-113">Идентификатор узла и IPv6-адрес, указанные в вызове **пирграфопендиректконнектион** , должны быть зарегистрированы для события **с \_ \_ \_ \_ данными о событиях однорангового графа** или не могут получать данные, отправленные вызывающим одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="69de9-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="69de9-114">При успешном выполнении **пирграфопендиректконнектион** возвращает идентификатор 64-битного соединения.</span><span class="sxs-lookup"><span data-stu-id="69de9-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="69de9-115">Однако одноранговый узел должен ожидать событие **\_ \_ \_ прямого \_ подключения одноранговой группы** , прежде чем идентификатор прямого подключения может быть идентифицирован как допустимый.</span><span class="sxs-lookup"><span data-stu-id="69de9-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="69de9-116">После установления соединения и подтверждения допустимого идентификатора соединения приложение может вызвать [**пирграфсенддата**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) , чтобы отправить данные по соединению, заданному ДОПУСТИМЫм идентификатором соединения, к участвующему одноранговому узлу — Если участвующий кэширующий узел зарегистрирован для события одноэлементных **\_ \_ \_ \_ данных однорангового графа** .</span><span class="sxs-lookup"><span data-stu-id="69de9-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="69de9-117">Непрозрачные данные доступны как структура [**\_ данных однорангового узла**](/windows/desktop/api/P2P/ns-p2p-peer_data) в [**\_ \_ \_ данных**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) одноранговых событий, возвращенных событием **\_ \_ \_ входящих \_ данных события однорангового графа** .</span><span class="sxs-lookup"><span data-stu-id="69de9-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="69de9-118">Если соединение не требуется, приложение вызывает [**пирграфклоседиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) с маркером графа и идентификатором соединения.</span><span class="sxs-lookup"><span data-stu-id="69de9-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="69de9-119">Прямые соединения с использованием инфраструктуры однорангового группирования</span><span class="sxs-lookup"><span data-stu-id="69de9-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="69de9-120">Прямые соединения в инфраструктуре одноранговых групп обрабатываются аналогично инфраструктуре одноранговых диаграмм.</span><span class="sxs-lookup"><span data-stu-id="69de9-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="69de9-121">Прежде чем можно будет установить прямое соединение между двумя членами в группе, оба члена должны зарегистрироваться для события **\_ \_ \_ прямого \_ соединения с событием одноранговой группы** .</span><span class="sxs-lookup"><span data-stu-id="69de9-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="69de9-122">Если члену группы требуется получать данные через прямое соединение, член группы также должен зарегистрироваться для события **\_ \_ \_ входящих \_ данных события одноранговой группы** .</span><span class="sxs-lookup"><span data-stu-id="69de9-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="69de9-123">**Одноранговая сеть \_ \_ \_ Прямое \_ соединение с событием группы** — это событие, которое уведомляет приложение о том, успешно ли выполнена или неудачная попытка прямого подключения.</span><span class="sxs-lookup"><span data-stu-id="69de9-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="69de9-124">Фактическое состояние успеха или сбоя вызова [**пирграупопендиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) возвращается в структуре [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .</span><span class="sxs-lookup"><span data-stu-id="69de9-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="69de9-125">Чтобы создать прямое соединение, приложение вызывает [**пирграупопендиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), а затем передает в группу маркер, указатель на удостоверение другого члена, который будет участвовать в этом соединении, и указатель на структуру IPv6-адреса для участвующего члена.</span><span class="sxs-lookup"><span data-stu-id="69de9-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="69de9-126">Элемент, удостоверение и IPv6-адрес которого указаны в вызове **пирграупопендиректконнектион** , должен быть зарегистрирован для **события \_ \_ \_ входящих \_ данных события одноранговой группы** , или член не может получать данные, отправленные вызывающим одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="69de9-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="69de9-127">**Пирграупопендиректконнектион** возвращает 64-разрядный идентификатор соединения при успешном выполнении.</span><span class="sxs-lookup"><span data-stu-id="69de9-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="69de9-128">Однако одноранговый узел должен дождаться возникновения события **\_ \_ \_ прямого \_ подключения однорангового графа** , прежде чем идентификатор прямого подключения сможет быть идентифицирован как допустимый.</span><span class="sxs-lookup"><span data-stu-id="69de9-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="69de9-129">После установления соединения и подтверждения допустимого идентификатора соединения приложение может вызвать [**пирграупсенддата**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) для отправки данных через соединение, заданное ДОПУСТИМЫм идентификатором соединения, на участвующего в качестве участника, если участвующий кэширующий узел зарегистрирован для события **\_ \_ \_ входящих \_ данных одноранговой группы** .</span><span class="sxs-lookup"><span data-stu-id="69de9-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="69de9-130">Непрозрачные данные доступны в виде [**структуры \_ данных одноранговых узлов**](/windows/desktop/api/P2P/ns-p2p-peer_data) в [**\_ \_ \_ данных**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) одноранговых событий, возвращенных событием **\_ \_ \_ входящих \_ данных события одноранговой группы** .</span><span class="sxs-lookup"><span data-stu-id="69de9-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="69de9-131">Если соединение не требуется, приложение вызывает [**пирграупклоседиректконнектион**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) с маркером группы и идентификатором соединения.</span><span class="sxs-lookup"><span data-stu-id="69de9-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="69de9-132">Пример прямого подключения для построения диаграмм</span><span class="sxs-lookup"><span data-stu-id="69de9-132">Example of a Direct Connection for Graphing</span></span>


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



