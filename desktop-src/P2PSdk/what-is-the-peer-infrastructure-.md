---
description: Одноранговая инфраструктура — это набор нескольких интерфейсов API, которые являются мощными и гибкими.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Что такое одноранговая инфраструктура?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663274"
---
# <a name="what-is-the-peer-infrastructure"></a><span data-ttu-id="7002d-103">Что такое одноранговая инфраструктура?</span><span class="sxs-lookup"><span data-stu-id="7002d-103">What is the Peer Infrastructure?</span></span>

<span data-ttu-id="7002d-104">Одноранговая инфраструктура — это набор нескольких интерфейсов API, которые являются мощными и гибкими.</span><span class="sxs-lookup"><span data-stu-id="7002d-104">The Peer Infrastructure is a set of several APIs that are powerful and flexible.</span></span> <span data-ttu-id="7002d-105">К основным компонентам относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="7002d-105">The major components include the following:</span></span>

-   [<span data-ttu-id="7002d-106">API одноранговых диаграмм</span><span class="sxs-lookup"><span data-stu-id="7002d-106">Peer Graphing API</span></span>](#peer-graphing-api)
-   [<span data-ttu-id="7002d-107">API однорангового группирования</span><span class="sxs-lookup"><span data-stu-id="7002d-107">Peer Grouping API</span></span>](#peer-grouping-api)
-   [<span data-ttu-id="7002d-108">API диспетчера одноранговых удостоверений</span><span class="sxs-lookup"><span data-stu-id="7002d-108">Peer Identity Manager API</span></span>](#peer-identity-manager-api)
-   [<span data-ttu-id="7002d-109">API поставщика пространства имен PNRP</span><span class="sxs-lookup"><span data-stu-id="7002d-109">PNRP Namespace Provider API</span></span>](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a><span data-ttu-id="7002d-110">API одноранговых диаграмм</span><span class="sxs-lookup"><span data-stu-id="7002d-110">Peer Graphing API</span></span>

<span data-ttu-id="7002d-111">Одноранговая инфраструктура предоставляет технологию для работы с графикой, которая позволяет эффективно и надежно передавать информацию между одноранговыми узлами в одноранговой диаграмме.</span><span class="sxs-lookup"><span data-stu-id="7002d-111">The Peer Infrastructure provides a graphing technology that can pass information efficiently and reliably between peers in a peer graph.</span></span> <span data-ttu-id="7002d-112">[API-интерфейс одноранговых диаграмм](graphing-api.md) обеспечивает единообразное представление данных в графе для каждого узла.</span><span class="sxs-lookup"><span data-stu-id="7002d-112">The [Peer Graphing API](graphing-api.md) ensures that each node has a consistent view of the data in a graph.</span></span>

<span data-ttu-id="7002d-113">[API-интерфейс одноранговых диаграмм](graphing-api.md) можно использовать для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7002d-113">You can use the [Peer Graphing API](graphing-api.md) to do the following:</span></span>

-   <span data-ttu-id="7002d-114">Создание одноранговых диаграмм и управление ими</span><span class="sxs-lookup"><span data-stu-id="7002d-114">Create and manage peer graphs</span></span>
-   <span data-ttu-id="7002d-115">Перечисление и взаимодействие с другими одноранговыми узлами в одноранговой диаграмме</span><span class="sxs-lookup"><span data-stu-id="7002d-115">Enumerate and interact with other peers in a peer graph</span></span>
-   <span data-ttu-id="7002d-116">Отправка данных в виде [записи](records.md) в каждый узел однорангового графа</span><span class="sxs-lookup"><span data-stu-id="7002d-116">Send data in the form of a [record](records.md) to each node in a peer graph</span></span>

## <a name="peer-grouping-api"></a><span data-ttu-id="7002d-117">API однорангового группирования</span><span class="sxs-lookup"><span data-stu-id="7002d-117">Peer Grouping API</span></span>

<span data-ttu-id="7002d-118">[Интерфейс API группирования одноранговых узлов](grouping-api.md) сочетает и расширяет одноранговые API-интерфейсы [PNRP](#pnrp-namespace-provider-api) и [Graph](#peer-graphing-api) и добавляет следующие два компонента:</span><span class="sxs-lookup"><span data-stu-id="7002d-118">The [Peer Grouping API](grouping-api.md) combines and enhances the Peer [PNRP](#pnrp-namespace-provider-api) and [Graphing](#peer-graphing-api) APIs, and adds the following two components:</span></span>

-   <span data-ttu-id="7002d-119">Уровень мультиплексирования, позволяющий нескольким приложениям, выполняющимся на одной одноранговой сущности, подключаться к группе</span><span class="sxs-lookup"><span data-stu-id="7002d-119">A multiplexing layer that allows multiple applications running on one peer entity to connect to a group</span></span>
-   <span data-ttu-id="7002d-120">Конкретная модель безопасности, которая гарантирует, что только одноранговые узлы, приглашенные в группу, смогут подключаться к группе через время существования группы.</span><span class="sxs-lookup"><span data-stu-id="7002d-120">A specific security model that ensures only peers invited to a group can connect to the group through the lifetime of the group</span></span>

<span data-ttu-id="7002d-121">API однорангового группирования можно использовать для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7002d-121">You can use the Peer Grouping API to do the following:</span></span>

-   <span data-ttu-id="7002d-122">Создание безопасных одноранговых групп и управление ими</span><span class="sxs-lookup"><span data-stu-id="7002d-122">Create and manage secure peer groups</span></span>
-   <span data-ttu-id="7002d-123">Перечисление и взаимодействие с другими одноранговыми узлами в группе</span><span class="sxs-lookup"><span data-stu-id="7002d-123">Enumerate and interact with other peers in a group</span></span>
-   <span data-ttu-id="7002d-124">Отправка данных в виде [записи](records.md) на каждый узел одноранговой группы</span><span class="sxs-lookup"><span data-stu-id="7002d-124">Send data in the form of a [record](records.md) to each node in a peer group</span></span>

## <a name="peer-identity-manager-api"></a><span data-ttu-id="7002d-125">API диспетчера одноранговых удостоверений</span><span class="sxs-lookup"><span data-stu-id="7002d-125">Peer Identity Manager API</span></span>

<span data-ttu-id="7002d-126">С помощью [API однорангового диспетчера удостоверений](identity-manager-api.md) можно создать безопасные [имена одноранговых узлов](peer-names.md) , которые могут использоваться протоколом PNRP, чтобы гарантировать, что имя пользователя, публикующий имя, официально принадлежит имени.</span><span class="sxs-lookup"><span data-stu-id="7002d-126">By using the [Peer Identity Manager API](identity-manager-api.md) you can create secure [peer names](peer-names.md) that PNRP can use to ensure that a person publishing a name officially owns the name.</span></span> <span data-ttu-id="7002d-127">Одноранговые имена также называются удостоверениями и используются в API однорангового группирования для идентификации отдельных пользователей в группе.</span><span class="sxs-lookup"><span data-stu-id="7002d-127">Peer names are also called identities, and they are used in the Peer Grouping API to identify the individuals in a group.</span></span>

<span data-ttu-id="7002d-128">[API диспетчера одноранговых удостоверений](identity-manager-api.md) можно использовать для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="7002d-128">You can use the [Peer Identity Manager API](identity-manager-api.md) to do the following:</span></span>

-   <span data-ttu-id="7002d-129">Создание, перечисление и управление идентификаторами одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="7002d-129">Create, enumerate, and manage peer identities.</span></span>

## <a name="pnrp-namespace-provider-api"></a><span data-ttu-id="7002d-130">API поставщика пространства имен PNRP</span><span class="sxs-lookup"><span data-stu-id="7002d-130">PNRP Namespace Provider API</span></span>

<span data-ttu-id="7002d-131">Одноранговая инфраструктура предоставляет бессерверную технологию разрешения имен, называемую [API поставщика пространства имен PNRP](pnrp-namespace-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="7002d-131">The Peer Infrastructure provides a serverless name resolution technology called the [PNRP Namespace Provider API](pnrp-namespace-provider-api.md).</span></span> <span data-ttu-id="7002d-132">Используя API поставщика пространства имен PNRP 2, одноранговая, служба, вычислительная группа и конечная точка одноранговой группы могут управлять, регистрировать, отменять регистрацию и разрешать другую конечную точку в [облаке](clouds.md)PNRP.</span><span class="sxs-lookup"><span data-stu-id="7002d-132">By using the Winsock 2 PNRP Namespace Provider API, a peer, service, computing device, and peer group endpoint can manage, register, unregister, and resolve another endpoint in a PNRP [cloud](clouds.md).</span></span>

> [!Note]  
> <span data-ttu-id="7002d-133">Протокол PNRP является акронимом для **протокола разрешения имен одноранговых узлов**.</span><span class="sxs-lookup"><span data-stu-id="7002d-133">PNRP is an acronym for **peer name resolution protocol**.</span></span>

 

 

 



