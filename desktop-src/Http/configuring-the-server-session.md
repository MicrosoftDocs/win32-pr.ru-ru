---
title: Настройка сеанса сервера
description: Настройка сеанса сервера
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090942"
---
# <a name="configuring-the-server-session"></a><span data-ttu-id="185cc-103">Настройка сеанса сервера</span><span class="sxs-lookup"><span data-stu-id="185cc-103">Configuring the Server Session</span></span>

<span data-ttu-id="185cc-104">Идентификатор сеанса сервера создается с помощью функции [**хттпкреатесерверсессион**](/windows/desktop/api/Http/nf-http-httpcreateserversession) и используется в вызове [**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="185cc-104">The server session ID is created with the [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) function, and used in the call to [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).</span></span> <span data-ttu-id="185cc-105">Параметр *ппропертинформатион* указывает на структуру конфигурации для заданного типа свойства.</span><span class="sxs-lookup"><span data-stu-id="185cc-105">The *pPropertyInformation* parameter points to the configuration structure for the property type that is set.</span></span> <span data-ttu-id="185cc-106">Параметр *пропертинформатионленгс* задает размер (в байтах) структуры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="185cc-106">The *PropertyInformationLength* parameter specifies the size, in bytes, of the configuration structure.</span></span> <span data-ttu-id="185cc-107">Например, при задании параметра **хттпсервертимеаутспроперти** параметр **ппропертинформатион** должен указывать на буфер, который не меньше размера структуры данных [**\_ \_ \_ об ограничении времени ожидания HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .</span><span class="sxs-lookup"><span data-stu-id="185cc-107">For example, when setting the **HttpServerTimeoutsProperty** the **pPropertyInformation** parameter must point to a buffer that is at least the size of the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure.</span></span>

<span data-ttu-id="185cc-108">Обычно приложение HTTP создает сеанс с одним сервером и может устанавливать свойства уровня приложения, такие как ограничение глобальной полосы пропускания или включить централизованное ведение журнала в этом сеансе сервера.</span><span class="sxs-lookup"><span data-stu-id="185cc-108">Typically an HTTP application creates a single server session and may set application wide properties such as global bandwidth throttling limit or enable centralized logging on this server session.</span></span> <span data-ttu-id="185cc-109">[**Хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) переопределяет конфигурации API-сервера HTTP для вызывающего приложения; Он не влияет на свойства HTTP-сервера на уровне API.</span><span class="sxs-lookup"><span data-stu-id="185cc-109">[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) overrides the HTTP Server API configurations for the calling application; it does not affect the HTTP Server API-wide properties.</span></span> <span data-ttu-id="185cc-110">Запросы к конфигурациям сеансов сервера запрашиваются путем вызова [**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span><span class="sxs-lookup"><span data-stu-id="185cc-110">The server session configurations are queried by calling [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).</span></span>

 

 




