---
title: Получение изменений
description: После регистрации клиента для получения уведомлений об определенных изменениях и возникновения одного или нескольких этих изменений клиент получает уведомление от диспетчера таблиц маршрутизации.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532003"
---
# <a name="retrieving-changes"></a><span data-ttu-id="8d3fe-103">Получение изменений</span><span class="sxs-lookup"><span data-stu-id="8d3fe-103">Retrieving Changes</span></span>

<span data-ttu-id="8d3fe-104">После регистрации клиента для получения уведомлений об определенных изменениях и возникновения одного или нескольких этих изменений клиент получает уведомление от диспетчера таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="8d3fe-104">Once a client has registered for notification of certain changes and one or more of these changes occurs, the client receives a notification from the routing table manager.</span></span> <span data-ttu-id="8d3fe-105">Диспетчер таблиц маршрутизации использует обратный вызов [**\_ \_ обратного вызова для события RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) , который был передан в предыдущем вызове [**ртмрегистерентити**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span><span class="sxs-lookup"><span data-stu-id="8d3fe-105">The routing table manager uses the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback that was supplied in a previous call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span></span> <span data-ttu-id="8d3fe-106">Диспетчер таблиц маршрутизации указывает, что \_ \_ произошло событие уведомления об изменении RTM.</span><span class="sxs-lookup"><span data-stu-id="8d3fe-106">The routing table manager indicates that a RTM\_CHANGE\_NOTIFICATION event has occurred.</span></span>

<span data-ttu-id="8d3fe-107">Пример кода, демонстрирующий использование этих функций, см. [в разделе Использование обратного вызова уведомления о событии](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="8d3fe-107">For sample code that shows how to use these functions, see [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




