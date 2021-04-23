---
description: Большинство операций Get и Set работают только с одним компонентом информации. Функция Фонежетстатус возвращает полные сведения о состоянии телефонного устройства в приложение.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Состояние (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909616"
---
# <a name="status-telephony-api"></a><span data-ttu-id="5a721-104">Состояние (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="5a721-104">Status (Telephony API)</span></span>

<span data-ttu-id="5a721-105">Большинство операций Get и Set работают только с одним компонентом информации.</span><span class="sxs-lookup"><span data-stu-id="5a721-105">Most of the get and set operations deal with one component of information only.</span></span> <span data-ttu-id="5a721-106">Функция [**фонежетстатус**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) возвращает полные сведения о состоянии телефонного устройства в приложение.</span><span class="sxs-lookup"><span data-stu-id="5a721-106">The [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) function returns complete status information about a phone device to an application.</span></span>

<span data-ttu-id="5a721-107">Как упоминалось ранее, при изменении элемента состояния на телефонном устройстве в функцию приложения отправляется сообщение о [**\_ состоянии телефона**](phone-state.md) .</span><span class="sxs-lookup"><span data-stu-id="5a721-107">As mentioned earlier, whenever a status item changes on the phone device, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function.</span></span> <span data-ttu-id="5a721-108">Параметры этого сообщения включают в себя маркер телефонного устройства и сведения об изменении элемента состояния.</span><span class="sxs-lookup"><span data-stu-id="5a721-108">This message's parameters include a handle to the phone device and an indication of the status item that changed.</span></span>

<span data-ttu-id="5a721-109">Приложение может использовать [**фонесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) для выбора конкретных изменений состояния, для которых требуется получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="5a721-109">An application can use [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) to select the specific status changes for which it wants to be notified.</span></span> <span data-ttu-id="5a721-110">В соответствии с этим [**фонежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) возвращает изменения состояния, для которых приложение хочет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="5a721-110">Correspondingly, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) returns the status changes for which the application wants to be notified.</span></span>

 

 



