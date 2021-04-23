---
title: Использование диспетчера таблиц маршрутизации версии 2
description: Перед началом разработки клиентов, использующих API RTMv2, ознакомьтесь с проблемами программирования RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- Служба маршрутизации и удаленного доступа RRAS, диспетчер таблиц маршрутизации, версия 2, задачи
- Диспетчер таблиц маршрутизации, службы RRAS версии 2, задачи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986580"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="8c869-105">Использование диспетчера таблиц маршрутизации версии 2</span><span class="sxs-lookup"><span data-stu-id="8c869-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="8c869-106">Перед началом разработки клиентов, использующих API RTMv2, ознакомьтесь с [проблемами программирования RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8c869-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="8c869-107">В этом разделе содержится пример кода, который можно использовать при разработке клиентов, таких как протоколы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8c869-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="8c869-108">Проблемы программирования RTMv2</span><span class="sxs-lookup"><span data-stu-id="8c869-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="8c869-109">Регистрация в диспетчере таблиц маршрутизации</span><span class="sxs-lookup"><span data-stu-id="8c869-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="8c869-110">Перечисление зарегистрированных сущностей</span><span class="sxs-lookup"><span data-stu-id="8c869-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="8c869-111">Получение и вызов экспортированных методов для клиента</span><span class="sxs-lookup"><span data-stu-id="8c869-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="8c869-112">Регистрация для получения уведомлений об изменениях</span><span class="sxs-lookup"><span data-stu-id="8c869-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="8c869-113">Добавление и обновление маршрутов с помощью Ртмаддраутетодест</span><span class="sxs-lookup"><span data-stu-id="8c869-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="8c869-114">Обновление маршрута с помощью Ртмупдатеандунлоккрауте</span><span class="sxs-lookup"><span data-stu-id="8c869-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="8c869-115">Использование состояния Hold-Down маршрута</span><span class="sxs-lookup"><span data-stu-id="8c869-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="8c869-116">Перечислить все назначения</span><span class="sxs-lookup"><span data-stu-id="8c869-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="8c869-117">Перечисление всех маршрутов</span><span class="sxs-lookup"><span data-stu-id="8c869-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="8c869-118">Поиск лучшего маршрута</span><span class="sxs-lookup"><span data-stu-id="8c869-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="8c869-119">Поиск маршрутов с помощью дерева префиксов</span><span class="sxs-lookup"><span data-stu-id="8c869-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="8c869-120">Доступ к непрозрачному указателю в месте назначения</span><span class="sxs-lookup"><span data-stu-id="8c869-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="8c869-121">Использование списка маршрутов Client-Specific</span><span class="sxs-lookup"><span data-stu-id="8c869-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="8c869-122">Использование обратного вызова уведомления о событиях</span><span class="sxs-lookup"><span data-stu-id="8c869-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




