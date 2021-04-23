---
title: Обзор архитектуры служб очереди сообщений
description: Службы очередей сообщений (MSMQ) используют модель сайта или предприятия. Как правило, сайт — это физическое расположение, например сборка. Предприятие состоит из одного или нескольких сайтов и представляет собой организацию.
ms.assetid: f5c54c58-8ec5-49b7-a184-aed9a8100960
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2226c185d32cb628529b34ba33d5569bd51ac28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331368"
---
# <a name="overview-of-message-queuing-services-architecture"></a><span data-ttu-id="3d7b0-105">Обзор архитектуры служб очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="3d7b0-105">Overview of Message Queuing Services Architecture</span></span>

<span data-ttu-id="3d7b0-106">Службы очередей сообщений (MSMQ) используют модель сайта или предприятия.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-106">Message Queuing Services (MSMQ) uses a site/enterprise model.</span></span> <span data-ttu-id="3d7b0-107">Как правило, сайт — это физическое расположение, например сборка.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-107">Typically, a site is a physical location, such as a building.</span></span> <span data-ttu-id="3d7b0-108">Предприятие состоит из одного или нескольких сайтов и представляет собой организацию.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-108">An enterprise consists of one or more sites and represents an organization.</span></span>

<span data-ttu-id="3d7b0-109">На следующей схеме показана архитектура службы MSMQ.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-109">The following diagram illustrates the architecture of the MSMQ Service.</span></span>

![Архитектура MSMQ](images/msmq.png)

<span data-ttu-id="3d7b0-111">В основе MSMQ лежит база данных службы очередей сообщений (MQIS), которая работает поверх SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-111">At the heart of MSMQ is the Message Queue Information Service (MQIS) database, which runs on top of SQL Server.</span></span> <span data-ttu-id="3d7b0-112">На предприятии имеется единая Главная MQIS, называемая основным контроллером предприятия.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-112">An enterprise has a single master MQIS, called the Primary Enterprise Controller.</span></span> <span data-ttu-id="3d7b0-113">Каждый сайт имеет собственную MQIS, называемую *первичным контроллером сайта* и нулевым или более *резервным контроллером сайта*.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-113">Each site has its own MQIS, called a *primary site controller* and zero or more *backup site controllers*.</span></span> <span data-ttu-id="3d7b0-114">Наконец, существуют отдельные клиентские компьютеры, каждый из которых имеет собственный диспетчер очередей, реализованный как услуга.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-114">Finally, there are the individual client computers, each of which has its own queue manager, implemented as a service.</span></span> <span data-ttu-id="3d7b0-115">Основной контроллер предприятия также может быть основным контроллером сайта, а любой контроллер также может быть клиентом.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-115">The Primary Enterprise Controller can also be a Primary Site Controller, and any controller can also be a client.</span></span>

<span data-ttu-id="3d7b0-116">Очереди сообщений могут быть либо открытыми, либо закрытыми.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-116">Message queues can be either public or private.</span></span> <span data-ttu-id="3d7b0-117">Общие очереди регистрируются в Active Directory и доступны по сети.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-117">Public queues are registered in Active Directory and are accessible across the network.</span></span> <span data-ttu-id="3d7b0-118">Сообщения в общей очереди направляются по всему предприятию под управлением MSMQ.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-118">Messages in a public queue are routed throughout the enterprise, under the control of MSMQ.</span></span> <span data-ttu-id="3d7b0-119">Сообщения клиентских приложений перемещаются из диспетчера очередей клиента в очередь назначения путем перемещения между диспетчерами очереди контроллеров сайта.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-119">Client application messages move from the client's queue manager to the destination queue by traveling between the queue managers of the site controllers.</span></span>

<span data-ttu-id="3d7b0-120">Частные очереди обслуживаются диспетчером локальных очередей и не регистрируются в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-120">Private queues are maintained by the local queue manager and are not registered in Active Directory.</span></span> <span data-ttu-id="3d7b0-121">Область сообщений частной очереди ограничена компьютером, на котором они находятся.</span><span class="sxs-lookup"><span data-stu-id="3d7b0-121">The scope of private queue messages is limited to the computer on which they reside.</span></span>

 

 




