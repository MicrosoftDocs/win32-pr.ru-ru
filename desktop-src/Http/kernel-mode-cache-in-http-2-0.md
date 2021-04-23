---
title: Кэш режима ядра
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068514"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="936fb-103">Кэш режима ядра</span><span class="sxs-lookup"><span data-stu-id="936fb-103">Kernel Mode Cache</span></span>

<span data-ttu-id="936fb-104">API-интерфейс версии 2,0 сервера HTTP позволяет приложениям кэшировать ответы со статическим содержимым в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="936fb-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="936fb-105">Повышение производительности достигается, когда запросы обслуживаются из кэша ядра без перехода в пользовательский режим.</span><span class="sxs-lookup"><span data-stu-id="936fb-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="936fb-106">API сервера HTTP применяет соответствующие конфигурации свойств ко всем запросам, которые обрабатываются из кэша ядра, включая ответы на журналы.</span><span class="sxs-lookup"><span data-stu-id="936fb-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="936fb-107">Однако запросы, требующие проверки подлинности, не будут обслуживаться из кэша.</span><span class="sxs-lookup"><span data-stu-id="936fb-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="936fb-108">API сервера HTTP ограничивает кэш в режиме ядра запросами, которые отвечают следующим условиям:</span><span class="sxs-lookup"><span data-stu-id="936fb-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="936fb-109">Команда запроса получает значение GET, и получается весь запрос.</span><span class="sxs-lookup"><span data-stu-id="936fb-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="936fb-110">Запрос не должен содержать тело сущности.</span><span class="sxs-lookup"><span data-stu-id="936fb-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="936fb-111">Протокол HTTP имеет версию 1,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="936fb-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="936fb-112">Заголовок "перевод: f" отсутствует.</span><span class="sxs-lookup"><span data-stu-id="936fb-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="936fb-113">Требуются заголовки, отличные от "предположительно: 100-Continue".</span><span class="sxs-lookup"><span data-stu-id="936fb-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="936fb-114">Заголовок авторизации отсутствует.</span><span class="sxs-lookup"><span data-stu-id="936fb-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="936fb-115">Заголовки Range и If-Range отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="936fb-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="936fb-116">В дополнение к ограничениям на запрос ответ также должен соответствовать следующим условиям.</span><span class="sxs-lookup"><span data-stu-id="936fb-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="936fb-117">По умолчанию размер ответа ограничен 256 КБ.</span><span class="sxs-lookup"><span data-stu-id="936fb-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="936fb-118">Чтобы изменить размер кэшированного ответа, задайте для параметра реестра **уримаксурибитес** необходимое число байтов.</span><span class="sxs-lookup"><span data-stu-id="936fb-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="936fb-119">Весь ответ должен быть предоставлен в одном вызове [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span><span class="sxs-lookup"><span data-stu-id="936fb-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="936fb-120">Заголовок даты в ответе не должен быть подавлен.</span><span class="sxs-lookup"><span data-stu-id="936fb-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="936fb-121">Если заголовок Last-Modified имеется, значение заголовка должно иметь правильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="936fb-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="936fb-122">Значение времени в этом заголовке используется для проверки управления кэшем.</span><span class="sxs-lookup"><span data-stu-id="936fb-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="936fb-123">В кэше режима ядра осталось достаточно места для хранения ответа.</span><span class="sxs-lookup"><span data-stu-id="936fb-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="936fb-124">По умолчанию кэш ответов режима ядра включен.</span><span class="sxs-lookup"><span data-stu-id="936fb-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="936fb-125">Если какое либо условие для указанного выше запроса или ответа не выполнено, ответ будет отправлен, но не будет кэшироваться.</span><span class="sxs-lookup"><span data-stu-id="936fb-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="936fb-126">В API сервера HTTP версии 2,0 [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) включает необязательный параметр *пкачеполици* для передачи структуры [**\_ \_ политики кэша HTTP**](/windows/desktop/api/Http/ns-http-http_cache_policy) .</span><span class="sxs-lookup"><span data-stu-id="936fb-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="936fb-127">Приложения используют структуру политики кэша для настройки кэша.</span><span class="sxs-lookup"><span data-stu-id="936fb-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




