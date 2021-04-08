---
description: Одним из наиболее распространенных способов получения события является выполнение работающего приложения, например приложения управления, собирающего и отображающего события для пользователя.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Получение событий для длительности вашего приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080534"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a><span data-ttu-id="b8a89-103">Получение событий для длительности вашего приложения</span><span class="sxs-lookup"><span data-stu-id="b8a89-103">Receiving Events for the Duration of Your Application</span></span>

<span data-ttu-id="b8a89-104">Одним из наиболее распространенных способов получения события является выполнение работающего приложения, например приложения управления, собирающего и отображающего события для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8a89-104">One of the most common ways to receive an event is through a running application, such as a management application that collects and displays events to a user.</span></span> <span data-ttu-id="b8a89-105">Такие приложения называются временными, так как временный потребитель не получает уведомления о событиях при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="b8a89-105">Such applications are called "temporary" because a temporary consumer does not receive event notifications when shut down.</span></span>

<span data-ttu-id="b8a89-106">Временный потребитель вызывает [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) в скрипте или [**IWbemServices.Exeкнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) в C++, чтобы подписываться на события в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="b8a89-106">A temporary consumer calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in script or [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ to subscribe to events in a namespace.</span></span> <span data-ttu-id="b8a89-107">Удостоверением, связанным с этой подпиской, является вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="b8a89-107">The identity associated with this subscription is the caller.</span></span>

<span data-ttu-id="b8a89-108">Временный потребитель событий может получать уведомления либо асинхронно, либо полусинхронном в сценариях и C++.</span><span class="sxs-lookup"><span data-stu-id="b8a89-108">A temporary event consumer can receive notifications either asynchronously or semisynchronously in both scripts and C++.</span></span>

> [!Note]  
> <span data-ttu-id="b8a89-109">По соображениям безопасности важно отметить, что асинхронные уведомления о событиях не рекомендуются.</span><span class="sxs-lookup"><span data-stu-id="b8a89-109">For security reasons, it is important to note that asynchronous event notifications are not recommended.</span></span> <span data-ttu-id="b8a89-110">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="b8a89-110">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span> <span data-ttu-id="b8a89-111">Потребители событий обладают особыми проблемами безопасности.</span><span class="sxs-lookup"><span data-stu-id="b8a89-111">Event consumers have special security concerns.</span></span> <span data-ttu-id="b8a89-112">Дополнительные сведения см. в разделе [Защита событий WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="b8a89-112">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

 

<span data-ttu-id="b8a89-113">Дополнительные сведения о получении асинхронных и семисинчронаус уведомлений о событиях см. в разделе [Получение асинхронных уведомлений о событиях](receiving-asynchronous-event-notifications.md) и [Получение уведомлений о событиях семисинчронаус](receiving-synchronous-and-semisynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b8a89-113">For more information about receiving asynchronous and semisynchronous event notifications, see [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md) and [Receiving Semisynchronous Event Notifications](receiving-synchronous-and-semisynchronous-event-notifications.md).</span></span>

 

 



