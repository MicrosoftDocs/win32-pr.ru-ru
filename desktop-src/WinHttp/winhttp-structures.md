---
description: В этом разделе определяются структуры, используемые WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Структуры WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587975"
---
# <a name="winhttp-structures"></a><span data-ttu-id="a5c13-103">Структуры WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a5c13-103">WinHTTP structures</span></span>

<span data-ttu-id="a5c13-104">WinHTTP использует следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="a5c13-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="a5c13-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="a5c13-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="a5c13-106">Содержит глобальную версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="a5c13-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="a5c13-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="a5c13-108">Содержит составные части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a5c13-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="a5c13-109">Эта структура используется с функциями [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="a5c13-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a5c13-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="a5c13-111">Содержит результат вызова асинхронной функции.</span><span class="sxs-lookup"><span data-stu-id="a5c13-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="a5c13-112">Эта структура используется с прототипом [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="a5c13-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="a5c13-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="a5c13-114">Используется для указания функции [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , следует ли указывать URL-адрес файла автоматической настройки прокси-сервера (PAC) или автоматически размещать URL-адреса с запросами DHCP или DNS к сети.</span><span class="sxs-lookup"><span data-stu-id="a5c13-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="a5c13-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="a5c13-116">Содержит сведения о сертификате, возвращенные с сервера.</span><span class="sxs-lookup"><span data-stu-id="a5c13-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="a5c13-117">Эта структура используется функцией [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="a5c13-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="a5c13-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="a5c13-119">Представляет группу соединений.</span><span class="sxs-lookup"><span data-stu-id="a5c13-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="a5c13-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="a5c13-121">Содержит исходный и конечный IP-адрес запроса, создавшего ответ.</span><span class="sxs-lookup"><span data-stu-id="a5c13-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="a5c13-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="a5c13-123">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="a5c13-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="a5c13-124">Эта структура устарела.</span><span class="sxs-lookup"><span data-stu-id="a5c13-124">This structure has been deprecated.</span></span> <span data-ttu-id="a5c13-125">Вместо этого рекомендуется использовать структуру [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="a5c13-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="a5c13-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="a5c13-127">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="a5c13-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="a5c13-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="a5c13-129">Содержит сведения о конфигурации прокси-сервера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a5c13-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-130">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="a5c13-130">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="a5c13-131">Представляет коллекцию групп соединений.</span><span class="sxs-lookup"><span data-stu-id="a5c13-131">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-132">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="a5c13-132">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="a5c13-133">Представляет идентификатор GUID соединения в целях сопоставления соединений.</span><span class="sxs-lookup"><span data-stu-id="a5c13-133">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-134">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a5c13-134">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="a5c13-135">Содержит конфигурацию сеанса или прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5c13-135">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-136">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a5c13-136">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="a5c13-137">Коллекция записей результатов прокси-сервера, предоставляемых [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="a5c13-137">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-138">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="a5c13-138">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="a5c13-139">Результирующая запись из вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="a5c13-139">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a5c13-140">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="a5c13-141">Представляет описание текущего состояния соединений WinHttp.</span><span class="sxs-lookup"><span data-stu-id="a5c13-141">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-142">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="a5c13-142">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="a5c13-143">Содержит статистику для запроса.</span><span class="sxs-lookup"><span data-stu-id="a5c13-143">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-144">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="a5c13-144">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="a5c13-145">Содержит сведения о времени для запроса.</span><span class="sxs-lookup"><span data-stu-id="a5c13-145">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-146">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="a5c13-146">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="a5c13-147">Содержит подключение SChannel и сведения о шифровании для запроса.</span><span class="sxs-lookup"><span data-stu-id="a5c13-147">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="a5c13-148">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="a5c13-149">Состояние результата операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a5c13-149">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="a5c13-150">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="a5c13-150">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="a5c13-151">Состояние операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="a5c13-151">Status of a WebSocket operation.</span></span>

</dd> </dl>
