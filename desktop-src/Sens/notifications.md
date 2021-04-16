---
description: Служба уведомлений о системных событиях позволяет приложениям, поддерживающим мобильные приложения, получать уведомления от системных событий, Сенс мониторы. Когда происходит запрошенное событие, Сенс уведомляет приложение.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Уведомления (служба уведомлений о системных событиях)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664213"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="63af3-104">Уведомления (служба уведомлений о системных событиях)</span><span class="sxs-lookup"><span data-stu-id="63af3-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="63af3-105">Служба уведомлений о системных событиях позволяет приложениям, поддерживающим мобильные приложения, получать уведомления от системных событий, Сенс мониторы.</span><span class="sxs-lookup"><span data-stu-id="63af3-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="63af3-106">Когда происходит запрошенное событие, Сенс уведомляет приложение.</span><span class="sxs-lookup"><span data-stu-id="63af3-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="63af3-107">Сенс может уведомлять приложения о трех классах системных событий:</span><span class="sxs-lookup"><span data-stu-id="63af3-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="63af3-108">Сетевые события TCP/IP, такие как состояние сетевого подключения TCP/IP или качество подключения.</span><span class="sxs-lookup"><span data-stu-id="63af3-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="63af3-109">События входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="63af3-109">User logon events.</span></span>
-   <span data-ttu-id="63af3-110">События аккумулятора и питания от сети.</span><span class="sxs-lookup"><span data-stu-id="63af3-110">Battery and AC power events.</span></span>

<span data-ttu-id="63af3-111">Например, приложение может подписываться на любые из следующих системных событий:</span><span class="sxs-lookup"><span data-stu-id="63af3-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="63af3-112">Установка сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="63af3-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="63af3-113">Уведомление, когда можно достигнуть указанного места назначения в указанных параметрах качества подключения (КОК)</span><span class="sxs-lookup"><span data-stu-id="63af3-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="63af3-114">Компьютер переключился на питание от аккумулятора</span><span class="sxs-lookup"><span data-stu-id="63af3-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="63af3-115">Процент оставшегося аккумулятора в указанном параметре</span><span class="sxs-lookup"><span data-stu-id="63af3-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="63af3-116">Выполняются запланированные события с помощью диспетчера синхронизации</span><span class="sxs-lookup"><span data-stu-id="63af3-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="63af3-117">**Windows Server 2008 R2 и Windows 7:** У подписчика должно быть не более 3 минут для ответа на уведомление в интерфейсах [**исенслогон**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) и [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) .</span><span class="sxs-lookup"><span data-stu-id="63af3-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="63af3-118">Через 3 минуты Сенс отменяет вызов подписчиков и разблокирует поток уведомлений.</span><span class="sxs-lookup"><span data-stu-id="63af3-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="63af3-119">Если требуется длительная операция для ответа на уведомление, вернитесь из **исенслогон** или **ISensLogon2** как можно быстрее и откройте другой поток для обработки.</span><span class="sxs-lookup"><span data-stu-id="63af3-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



