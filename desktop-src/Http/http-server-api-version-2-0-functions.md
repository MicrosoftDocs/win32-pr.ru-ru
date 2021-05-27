---
title: Функции API сервера HTTP версии 2,0
description: API сервера HTTP версии 2,0 предоставляет следующие функции.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Функции API сервера HTTP версии 2,0
- Функции HTTP, API HTTP-сервера версии 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549079"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="f5747-105">Функции API сервера HTTP версии 2,0</span><span class="sxs-lookup"><span data-stu-id="f5747-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="f5747-106">API сервера HTTP версии 2,0 предоставляет следующие функции.</span><span class="sxs-lookup"><span data-stu-id="f5747-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="f5747-107">Функция</span><span class="sxs-lookup"><span data-stu-id="f5747-107">Function</span></span> | <span data-ttu-id="f5747-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f5747-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="f5747-109">**хттпделегатерекуестекс**</span><span class="sxs-lookup"><span data-stu-id="f5747-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="f5747-110">Делегирует запрос от исходной очереди запросов к целевой очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="f5747-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="f5747-111">**хттпфиндурлграупид**</span><span class="sxs-lookup"><span data-stu-id="f5747-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="f5747-112">Извлекает идентификатор группы URL-адресов и очередь запросов.</span><span class="sxs-lookup"><span data-stu-id="f5747-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="f5747-113">**хттписфеатуресуппортед**</span><span class="sxs-lookup"><span data-stu-id="f5747-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="f5747-114">Проверяет, поддерживается ли определенный компонент.</span><span class="sxs-lookup"><span data-stu-id="f5747-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="f5747-115">Сеанс сервера</span><span class="sxs-lookup"><span data-stu-id="f5747-115">Server session</span></span>

| <span data-ttu-id="f5747-116">Функция</span><span class="sxs-lookup"><span data-stu-id="f5747-116">Function</span></span> | <span data-ttu-id="f5747-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f5747-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="f5747-118">**хттпклосесерверсессион**</span><span class="sxs-lookup"><span data-stu-id="f5747-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="f5747-119">**хттпкреатесерверсессион**</span><span class="sxs-lookup"><span data-stu-id="f5747-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="f5747-120">**хттпкуерисерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="f5747-121">**хттпсетсерверсессионпроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="f5747-122">Группы URL-адресов</span><span class="sxs-lookup"><span data-stu-id="f5747-122">URL Groups</span></span>

| <span data-ttu-id="f5747-123">Функция</span><span class="sxs-lookup"><span data-stu-id="f5747-123">Function</span></span> | <span data-ttu-id="f5747-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f5747-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="f5747-125">**хттпаддурлтаурлграуп**</span><span class="sxs-lookup"><span data-stu-id="f5747-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="f5747-126">**хттпкреатеурлграуп**</span><span class="sxs-lookup"><span data-stu-id="f5747-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="f5747-127">**хттпклосеурлграуп**</span><span class="sxs-lookup"><span data-stu-id="f5747-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="f5747-128">**хттпкуерюрлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="f5747-129">**хттпремовеурлфромурлграуп**</span><span class="sxs-lookup"><span data-stu-id="f5747-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="f5747-130">**хттпсетурлграуппроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="f5747-131">Очередь запросов</span><span class="sxs-lookup"><span data-stu-id="f5747-131">Request Queue</span></span>

| <span data-ttu-id="f5747-132">Функция</span><span class="sxs-lookup"><span data-stu-id="f5747-132">Function</span></span> | <span data-ttu-id="f5747-133">Описание</span><span class="sxs-lookup"><span data-stu-id="f5747-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="f5747-134">**хттпклосерекуесткуеуе**</span><span class="sxs-lookup"><span data-stu-id="f5747-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="f5747-135">**хттпкреатерекуесткуеуе**</span><span class="sxs-lookup"><span data-stu-id="f5747-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="f5747-136">**хттпкуерирекуесткуеуепроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="f5747-137">**хттпсетрекуесткуеуепроперти**</span><span class="sxs-lookup"><span data-stu-id="f5747-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="f5747-138">**хттпшутдовнрекуесткуеуе**</span><span class="sxs-lookup"><span data-stu-id="f5747-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="f5747-139">**хттпваитфордемандстарт**</span><span class="sxs-lookup"><span data-stu-id="f5747-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="f5747-140">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f5747-140">Related topics</span></span>

[<span data-ttu-id="f5747-141">Структуры API HTTP-сервера версии 2,0</span><span class="sxs-lookup"><span data-stu-id="f5747-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
