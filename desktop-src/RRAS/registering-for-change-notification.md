---
title: Регистрация для уведомления об изменениях
description: Клиент может зарегистрироваться для получения уведомлений об изменениях в сведениях о маршрутизации, которые хранятся в диспетчере таблиц маршрутизации. Этот запрос может быть сделан только после того, как клиент зарегистрировался в диспетчере таблиц маршрутизации.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329603"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="3fa8f-104">Регистрация для уведомления об изменениях</span><span class="sxs-lookup"><span data-stu-id="3fa8f-104">Registering for Change Notification</span></span>

<span data-ttu-id="3fa8f-105">Клиент может зарегистрироваться для получения уведомлений об изменениях в сведениях о маршрутизации, которые хранятся в диспетчере таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="3fa8f-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="3fa8f-106">Этот запрос может быть сделан только после того, как клиент зарегистрировался в диспетчере таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="3fa8f-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="3fa8f-107">Чтобы зарегистрироваться для получения уведомлений об изменениях, клиент должен вызвать [**ртмрегистерфорчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), указав типы изменений, для которых клиент должен получить уведомление.</span><span class="sxs-lookup"><span data-stu-id="3fa8f-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="3fa8f-108">Если клиент должен получать уведомления об изменении конкретных назначений, клиент вызывает [**ртммаркдестфорчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) один раз для каждого назначения.</span><span class="sxs-lookup"><span data-stu-id="3fa8f-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="3fa8f-109">Клиент может прерывать получение уведомлений об изменениях, вызывая [**ртмдерегистерфромчанженотификатион**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span><span class="sxs-lookup"><span data-stu-id="3fa8f-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="3fa8f-110">Пример кода, демонстрирующий использование этих функций, см. в разделе [Регистрация для уведомления об изменениях](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="3fa8f-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




