---
description: Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Получение уведомлений о сетевых событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682613"
---
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="c4de2-103">Получение уведомлений о сетевых событиях</span><span class="sxs-lookup"><span data-stu-id="c4de2-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="c4de2-104">Используйте следующие функции, чтобы убедиться, что приложение получает уведомления о некоторых сетевых событиях.</span><span class="sxs-lookup"><span data-stu-id="c4de2-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="c4de2-105">Используйте функцию [**нотифяддрчанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) для запроса уведомления об изменениях, происходящих в сопоставлении между IP-адресами и интерфейсами на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c4de2-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="c4de2-106">Аналогичным образом функция [**нотифираутечанже**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) позволяет приложению запрашивать уведомления о любых изменениях, происходящих в таблице маршрутизации IP.</span><span class="sxs-lookup"><span data-stu-id="c4de2-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="c4de2-107">Уведомления, предоставляемые этими функциями, не указывают, что изменилось; они просто указывают, что что-то изменилось.</span><span class="sxs-lookup"><span data-stu-id="c4de2-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="c4de2-108">Используйте другие вспомогательные функции IP, такие как [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) и [**жетбестрауте**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), чтобы определить точную природу изменения.</span><span class="sxs-lookup"><span data-stu-id="c4de2-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



