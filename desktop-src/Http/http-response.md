---
title: HTTP_RESPONSE (HTTP. h)
description: Версия структуры HTTP- \_ ответа зависит от версии очереди запросов, используемой в качестве приведенной в очереди запросов HTTP-сервера версии 1,0. это структура HTTP- \_ запроса \_ v1. API HTTP-сервера версия 2,0 очередь запросов. это структура HTTP- \_ запроса \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415273"
---
# <a name="http_response"></a><span data-ttu-id="740a1-106">HTTP- \_ ответ</span><span class="sxs-lookup"><span data-stu-id="740a1-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="740a1-107">Версия структуры **\_ ответа HTTP** зависит от версии очереди запросов, используемой следующим образом:</span><span class="sxs-lookup"><span data-stu-id="740a1-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="740a1-108">API HTTP-сервера версия 1,0 очередь запросов: это структура [**HTTP- \_ запроса \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .</span><span class="sxs-lookup"><span data-stu-id="740a1-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="740a1-109">API HTTP-сервера версия 2,0 очередь запросов: это структура [**HTTP- \_ запроса \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .</span><span class="sxs-lookup"><span data-stu-id="740a1-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="740a1-110">Не используйте [**HTTP- \_ запрос \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) и [**HTTP- \_ запрос \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) непосредственно в коде; использование **HTTP- \_ ответа** гарантирует правильную версию структуры на основе версии очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="740a1-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="740a1-111">**HTTP- \_ ответ**</span><span class="sxs-lookup"><span data-stu-id="740a1-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="740a1-112">Запрос был получен из очереди запросов v1.</span><span class="sxs-lookup"><span data-stu-id="740a1-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="740a1-113">**HTTP- \_ ответ**</span><span class="sxs-lookup"><span data-stu-id="740a1-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="740a1-114">Запрос был получен из очереди запросов v2.</span><span class="sxs-lookup"><span data-stu-id="740a1-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="740a1-115">**\_ответ ФТТП**</span><span class="sxs-lookup"><span data-stu-id="740a1-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="740a1-116">Указатель на структуру **HTTP- \_ ответа** .</span><span class="sxs-lookup"><span data-stu-id="740a1-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="740a1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="740a1-117">Requirements</span></span>



| <span data-ttu-id="740a1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="740a1-118">Requirement</span></span> | <span data-ttu-id="740a1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="740a1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="740a1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="740a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="740a1-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="740a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="740a1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="740a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="740a1-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="740a1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="740a1-124">Header</span><span class="sxs-lookup"><span data-stu-id="740a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="740a1-125"><dt>HTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="740a1-125"><dt>Http.h</dt></span></span> </dl> |



 

 





