---
title: Структуры API HTTP-сервера версии 1,0
description: Структуры API HTTP-сервера версии 1,0
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- Структуры API-сервера HTTP
- Структуры HTTP, API сервера HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412919"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="1cb12-105">Структуры API HTTP-сервера версии 1,0</span><span class="sxs-lookup"><span data-stu-id="1cb12-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="1cb12-106">API сервера HTTP предоставляет следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="1cb12-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="1cb12-107">**\_версия HTTPAPI**</span><span class="sxs-lookup"><span data-stu-id="1cb12-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="1cb12-108">**\_диапазон БАЙТОВ \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="1cb12-109">**\_Политика кэша \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="1cb12-110">**\_ \_ URL-адрес HTTP обработанные**</span><span class="sxs-lookup"><span data-stu-id="1cb12-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="1cb12-111">**\_фрагмент данных \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="1cb12-112">**\_известный \_ заголовок HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="1cb12-113">[**HTTP- \_ запрос**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1cb12-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="1cb12-114">**заголовки HTTP- \_ запросов \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="1cb12-115">**HTTP- \_ ответ**</span><span class="sxs-lookup"><span data-stu-id="1cb12-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="1cb12-116">**\_заголовки ответа \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="1cb12-117">**\_ \_ \_ \_ параметр прослушивания IP-адреса в конфигурации службы HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="1cb12-118">**\_запрос на \_ \_ \_ прослушивание IP-адреса конфигурации службы HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="1cb12-119">**\_ \_ ключ SSL для конфигурации службы \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="1cb12-120">**\_ \_ \_ параметр SSL конфигурации службы \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="1cb12-121">**\_SSL- \_ \_ запрос конфигурации \_ службы HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="1cb12-122">**\_ \_ \_ набор SSL конфигурации HTTP-службы \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="1cb12-123">**\_ \_ Настройка SSL- \_ \_ ключа SNI \_ для конфигурации службы HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="1cb12-124">**\_SSL- \_ \_ \_ \_ запрос конфигурации службы HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="1cb12-125">**\_ \_ \_ Настройка SSL для конфигурации \_ HTTP \_ -службы**</span><span class="sxs-lookup"><span data-stu-id="1cb12-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="1cb12-126">**\_ \_ \_ URLACL \_ ключ конфигурации службы HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="1cb12-127">**\_ \_ \_ параметр URLACL конфигурации службы \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="1cb12-128">**\_запрос конфигурации HTTP-службы \_ \_ URLACL \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="1cb12-129">**\_ \_ Настройка URLACL для конфигурации службы \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="1cb12-130">**\_ \_ сведения о SSL- \_ сертификате клиента \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="1cb12-131">**\_ \_ сведения о SSL HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="1cb12-132">**\_адрес транспорта \_ http**</span><span class="sxs-lookup"><span data-stu-id="1cb12-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="1cb12-133">**\_заголовок HTTP Unknown \_**</span><span class="sxs-lookup"><span data-stu-id="1cb12-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="1cb12-134">**\_Версия HTTP**</span><span class="sxs-lookup"><span data-stu-id="1cb12-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="1cb12-135">См. также</span><span class="sxs-lookup"><span data-stu-id="1cb12-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cb12-136">Функции API сервера HTTP версии 1,0</span><span class="sxs-lookup"><span data-stu-id="1cb12-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 