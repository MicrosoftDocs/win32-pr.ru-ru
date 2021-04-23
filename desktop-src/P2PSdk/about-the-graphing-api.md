---
description: API-интерфейс одноранговых диаграмм позволяет приложениям эффективно и надежно передавать данные между равноправными узлами. Основными понятиями технологии одноранговых графов являются узлы одноранговых графов и уведомления о событиях.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Сведения об API Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663369"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="601e5-104">Сведения об API Graph</span><span class="sxs-lookup"><span data-stu-id="601e5-104">About the Graphing API</span></span>

<span data-ttu-id="601e5-105">API-интерфейс одноранговых диаграмм позволяет приложениям эффективно и надежно передавать данные между равноправными узлами.</span><span class="sxs-lookup"><span data-stu-id="601e5-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="601e5-106">Основными понятиями технологии одноранговых графов являются **узлы** одноранговых графов и уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="601e5-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="601e5-107">Узлы</span><span class="sxs-lookup"><span data-stu-id="601e5-107">Nodes</span></span>

<span data-ttu-id="601e5-108">Узел представляет конкретный экземпляр однорангового узла в сети.</span><span class="sxs-lookup"><span data-stu-id="601e5-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="601e5-109">Инфраструктура API одноранговых диаграмм гарантирует, что каждый узел будет иметь единообразное представление данных в графе.</span><span class="sxs-lookup"><span data-stu-id="601e5-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="601e5-110">Узел имеет следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="601e5-110">A node has the following features:</span></span>

-   <span data-ttu-id="601e5-111">Может подключаться к другому узлу и формировать взаимосвязанную сеть, называемую одноранговой диаграммой.</span><span class="sxs-lookup"><span data-stu-id="601e5-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="601e5-112">Может совместно использовать данные с другими узлами в графе в виде [записи](records.md).</span><span class="sxs-lookup"><span data-stu-id="601e5-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="601e5-113">Может создавать прямые соединения отдельно от одноранговых графов, установленных с помощью однорангового [API группирования](about-the-grouping-api.md).</span><span class="sxs-lookup"><span data-stu-id="601e5-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="601e5-114">Прямые соединения позволяют узлам передавать закрытые данные друг другу.</span><span class="sxs-lookup"><span data-stu-id="601e5-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="601e5-115">Уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="601e5-115">Event Notices</span></span>

<span data-ttu-id="601e5-116">API-интерфейс одноранговых диаграмм имеет инфраструктуру событий, которая позволяет приложению регистрироваться и принимать уведомления о событиях одноранговой сети в инфраструктуре API-интерфейсов одноранговых диаграмм.</span><span class="sxs-lookup"><span data-stu-id="601e5-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="601e5-117">При внесении каких-либо изменений в одноранговый граф приложение отправляет уведомление о событии, чтобы выяснить, что произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="601e5-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



