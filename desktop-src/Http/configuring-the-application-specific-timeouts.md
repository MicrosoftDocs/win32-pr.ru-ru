---
title: Настройка времени ожидания для конкретного приложения
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Настройка HTTP, связанных с временем ожидания приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067913"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="8912c-104">Настройка времени ожидания для конкретного приложения</span><span class="sxs-lookup"><span data-stu-id="8912c-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="8912c-105">Параметры API HTTP-сервера применяются ко всем сеансам сервера и группам URL-адресов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8912c-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="8912c-106">Эти конфигурации можно переопределить с помощью приложения, задав значения времени ожидания для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="8912c-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="8912c-107">Время ожидания сеансов сервера переопределяет время ожидания для HTTP-сервера на уровне API и применяется ко всем созданным в них группам URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="8912c-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="8912c-108">Настройка свойства Timeouts в группе URL-адресов переопределяет время ожидания сеанса сервера для всех URL-адресов в группе.</span><span class="sxs-lookup"><span data-stu-id="8912c-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="8912c-109">Указание нуля для любого таймера в структуре [**\_ \_ \_ сведений о ограничении времени ожидания HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) для группы URL-адресов приводит к тому, что API сервера HTTP возвращается к истечению времени ожидания сеансов сервера, если они существуют, или по умолчанию HTTP-API сервера, если время ожидания сеанса сервера не существует.</span><span class="sxs-lookup"><span data-stu-id="8912c-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="8912c-110">Например, если свойство времени ожидания сервера имеется в группе URL-адресов, а таймер **ентитибоди** равен нулю, то используется время ожидания сеанса сервера.</span><span class="sxs-lookup"><span data-stu-id="8912c-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="8912c-111">Если свойство Timeouts не задано в сеансе сервера, используется конфигурация API HTTP-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8912c-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="8912c-112">Чтобы отключить таймер, задайте значение **максушорт**, за исключением таймера **минсендрате** , для которого задано **максулонг**.</span><span class="sxs-lookup"><span data-stu-id="8912c-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="8912c-113">API-интерфейс сервера HTTP может настраивать только **хеадерваит** , зависящие от приложения, а таймеры **идлеконнектион** действуют только после получения первого запроса.</span><span class="sxs-lookup"><span data-stu-id="8912c-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="8912c-114">Перед получением первого запроса применяются значения времени ожидания на уровне API HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="8912c-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="8912c-115">После того как первый запрос прибывает и связан с очередью запросов, можно применять таймеры **хеадерваит** и **идлеконнектион** для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="8912c-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="8912c-116">Таймеры конкретного приложения применяются ко всем последующим запросам, поступающим в очередь запросов, для подключения проверки активности.</span><span class="sxs-lookup"><span data-stu-id="8912c-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="8912c-117">Дополнительные сведения о настройке таймеров см. в разделах [Настройка группы URL-адресов](configuring-the-url-group.md) и [Настройка сеанса сервера](configuring-the-server-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8912c-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




