---
description: API группирования одноранговых узлов сочетает в себе технологию API поставщика пространства имен PNRP и API Graph.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Сведения об API группирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663370"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="17c0a-103">Сведения об API группирования</span><span class="sxs-lookup"><span data-stu-id="17c0a-103">About the Grouping API</span></span>

<span data-ttu-id="17c0a-104">API группирования одноранговых узлов сочетает в себе технологию [API поставщика пространства имен PNRP](pnrp-namespace-provider-api.md) и [API Graph](graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="17c0a-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="17c0a-105">Группирование добавляет следующие две технологии:</span><span class="sxs-lookup"><span data-stu-id="17c0a-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="17c0a-106">Уровень мультиплексирования, позволяющий нескольким приложениям использовать один график, один порт и одну базу данных записей.</span><span class="sxs-lookup"><span data-stu-id="17c0a-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="17c0a-107">Безопасность, которая гарантирует, что только одноранговые узлы, приглашенные в группу, могут присоединиться и подключиться в течение всего времени существования группы.</span><span class="sxs-lookup"><span data-stu-id="17c0a-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="17c0a-108">Группирование предоставляет удобный и простой подход к одноранговой сети благодаря простому потоку вызовов и защищенному обмену сообщениями.</span><span class="sxs-lookup"><span data-stu-id="17c0a-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="17c0a-109">Этот API использует PNRP для обнаружения групп и стандартный поставщик безопасности на основе PKI, а не требует, чтобы разработчик реализовал его.</span><span class="sxs-lookup"><span data-stu-id="17c0a-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="17c0a-110">Однако если приложение требует большей гибкости с точки зрения безопасности, рассмотрите возможность использования [API Graph](about-the-graphing-api.md).</span><span class="sxs-lookup"><span data-stu-id="17c0a-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="17c0a-111">В следующей таблице приведены разделы в этом разделе API группирования.</span><span class="sxs-lookup"><span data-stu-id="17c0a-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="17c0a-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="17c0a-112">Topic</span></span>                                                                | <span data-ttu-id="17c0a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="17c0a-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17c0a-114">Работа с группами</span><span class="sxs-lookup"><span data-stu-id="17c0a-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="17c0a-115">Описывает поток вызова в приложении однорангового группирования от запуска до завершения работы.</span><span class="sxs-lookup"><span data-stu-id="17c0a-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="17c0a-116">Принципы работы группы безопасности</span><span class="sxs-lookup"><span data-stu-id="17c0a-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="17c0a-117">Описание защиты членства и обмена данными между одноранговыми группами.</span><span class="sxs-lookup"><span data-stu-id="17c0a-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="17c0a-118">Приглашение однорангового узла в группу</span><span class="sxs-lookup"><span data-stu-id="17c0a-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="17c0a-119">Описывает процесс, по которому приглашенные узлы приглашаются и добавляются в одноранговую группу.</span><span class="sxs-lookup"><span data-stu-id="17c0a-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="17c0a-120">Подключение к одноранговой группе</span><span class="sxs-lookup"><span data-stu-id="17c0a-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="17c0a-121">Описывает, как одноранговый узел подключается к одноранговой группе и взаимодействует с ней.</span><span class="sxs-lookup"><span data-stu-id="17c0a-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="17c0a-122">Управление записями групп</span><span class="sxs-lookup"><span data-stu-id="17c0a-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="17c0a-123">Описывает записи одноранговых групп и управление ими как участником и администратором.</span><span class="sxs-lookup"><span data-stu-id="17c0a-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="17c0a-124">Приложениям, использующим API группирования в среде с брандмауэром, требуются группы исключений, охватывающие порт, характерный для приложения, а также порт "3587-TCP" для API группирования и порт "3540-UDP" для PNRP.</span><span class="sxs-lookup"><span data-stu-id="17c0a-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="17c0a-125">Эти группы исключений должны быть включены при каждом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="17c0a-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



