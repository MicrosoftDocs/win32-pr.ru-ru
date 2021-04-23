---
title: Структуры API HTTP-сервера версии 2,0
description: API сервера HTTP версии 2,0 предоставляет следующие структуры для написания приложений.
ms.assetid: 5a8e28e9-f85b-4550-929e-53f38eca6a8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5e41016592e16fcf159188cc1ebc760568f807
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410977"
---
# <a name="http-server-api-version-20-structures"></a><span data-ttu-id="1c4a8-103">Структуры API HTTP-сервера версии 2,0</span><span class="sxs-lookup"><span data-stu-id="1c4a8-103">HTTP Server API Version 2.0 Structures</span></span>

<span data-ttu-id="1c4a8-104">API сервера HTTP версии 2,0 предоставляет следующие структуры для написания приложений:</span><span class="sxs-lookup"><span data-stu-id="1c4a8-104">The HTTP Server API version 2.0 provides the following structures for writing applications:</span></span>

-   [<span data-ttu-id="1c4a8-105">**\_ \_ сведения о лимите пропускной способности HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-105">**HTTP\_BANDWIDTH\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)
-   [<span data-ttu-id="1c4a8-106">**\_сведения о привязке HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-106">**HTTP\_BINDING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_binding_info)
-   [<span data-ttu-id="1c4a8-107">**\_ \_ сведения о привязке канала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-107">**HTTP\_CHANNEL\_BIND\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_channel_bind_info)
-   [<span data-ttu-id="1c4a8-108">**\_ \_ сведения о ЛИМИТЕ HTTP-подключений \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-108">**HTTP\_CONNECTION\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_connection_limit_info)
-   [<span data-ttu-id="1c4a8-109">**\_ \_ сведения о фловрате HTTP**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-109">**HTTP\_FLOWRATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_flowrate_info)
-   [<span data-ttu-id="1c4a8-110">**\_ \_ сведения о конечной точке ПРОСЛУШИВАНИя HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-110">**HTTP\_LISTEN\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_listen_endpoint_info)
-   [<span data-ttu-id="1c4a8-111">**\_данные журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-111">**HTTP\_LOG\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_data)
-   [<span data-ttu-id="1c4a8-112">**\_ \_ данные полей журнала \_ http**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-112">**HTTP\_LOG\_FIELDS\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_fields_data)
-   [<span data-ttu-id="1c4a8-113">**\_сведения о ведении журнала HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-113">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
-   [<span data-ttu-id="1c4a8-114">**\_несколько \_ известных \_ ЗАголовков HTTP**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-114">**HTTP\_MULTIPLE\_KNOWN\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)
-   [<span data-ttu-id="1c4a8-115">**\_ \_ флаги свойств HTTP**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-115">**HTTP\_PROPERTY\_FLAGS**</span></span>](/windows/desktop/api/Http/ns-http-http_property_flags)
-   [<span data-ttu-id="1c4a8-116">**\_ \_ сведения о параметрах качества обслуживания HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-116">**HTTP\_QOS\_SETTING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_qos_setting_info)
-   [<span data-ttu-id="1c4a8-117">**\_ \_ сведения о проверке подлинности HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-117">**HTTP\_REQUEST\_AUTH\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_auth_info)
-   [<span data-ttu-id="1c4a8-118">**\_ \_ \_ состояние привязки канала HTTP-запроса \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-118">**HTTP\_REQUEST\_CHANNEL\_BIND\_STATUS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_channel_bind_status)
-   [<span data-ttu-id="1c4a8-119">**\_ \_ сведения о HTTP-запросе**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-119">**HTTP\_REQUEST\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_info)
-   [<span data-ttu-id="1c4a8-120">**HTTP- \_ запрос \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-120">**HTTP\_REQUEST\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v1)
-   [<span data-ttu-id="1c4a8-121">**HTTP- \_ запрос \_ v2**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-121">**HTTP\_REQUEST\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v2)
-   [<span data-ttu-id="1c4a8-122">**\_сведения об ответе HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-122">**HTTP\_RESPONSE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_response_info)
-   [<span data-ttu-id="1c4a8-123">**HTTP- \_ ответ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-123">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
-   [<span data-ttu-id="1c4a8-124">**HTTP- \_ ответ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-124">**HTTP\_RESPONSE\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v2)
-   [<span data-ttu-id="1c4a8-125">**\_ \_ \_ Основные параметры проверки подлинности HTTP-сервера \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-125">**HTTP\_SERVER\_AUTHENTICATION\_BASIC\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_basic_params)
-   [<span data-ttu-id="1c4a8-126">**\_ \_ \_ Параметры дайджеста проверки подлинности HTTP-сервера \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-126">**HTTP\_SERVER\_AUTHENTICATION\_DIGEST\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_digest_params)
-   [<span data-ttu-id="1c4a8-127">**\_ \_ сведения о проверке подлинности HTTP-сервера \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-127">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
-   [<span data-ttu-id="1c4a8-128">**\_Привязка службы \_ HTTP \_ A**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-128">**HTTP\_SERVICE\_BINDING\_A**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_a)
-   [<span data-ttu-id="1c4a8-129">**\_Привязка службы \_ HTTP \_ W**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-129">**HTTP\_SERVICE\_BINDING\_W**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_w)
-   [<span data-ttu-id="1c4a8-130">**\_ \_ база привязки службы \_ http**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-130">**HTTP\_SERVICE\_BINDING\_BASE**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_base)
-   [<span data-ttu-id="1c4a8-131">**\_ \_ тип привязки службы \_ http**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-131">**HTTP\_SERVICE\_BINDING\_TYPE**</span></span>](/windows/desktop/api/Http/ne-http-http_service_binding_type)
-   [<span data-ttu-id="1c4a8-132">**\_ \_ \_ набор кэша конфигурации службы \_ http**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-132">**HTTP\_SERVICE\_CONFIG\_CACHE\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_cache_set)
-   [<span data-ttu-id="1c4a8-133">**\_ \_ \_ задано время ожидания конфигурации службы HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-133">**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)
-   [<span data-ttu-id="1c4a8-134">**\_ \_ сведения о состоянии HTTP**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-134">**HTTP\_STATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_state_info)
-   [<span data-ttu-id="1c4a8-135">**\_ \_ сведения об ограничении времени ожидания HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="1c4a8-135">**HTTP\_TIMEOUT\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

 

 




