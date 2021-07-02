---
description: В этом разделе определяются структуры, используемые WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Структуры WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174984"
---
# <a name="winhttp-structures"></a><span data-ttu-id="5c034-103">Структуры WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5c034-103">WinHTTP structures</span></span>

<span data-ttu-id="5c034-104">WinHTTP использует следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="5c034-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="5c034-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c034-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="5c034-106">Содержит глобальную версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="5c034-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="5c034-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="5c034-108">Содержит составные части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5c034-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="5c034-109">Эта структура используется с функциями [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="5c034-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c034-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="5c034-111">Содержит результат вызова асинхронной функции.</span><span class="sxs-lookup"><span data-stu-id="5c034-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="5c034-112">Эта структура используется с прототипом [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="5c034-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5c034-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="5c034-114">Используется для указания функции [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , следует ли указывать URL-адрес файла автоматической настройки прокси-сервера (PAC) или автоматически размещать URL-адреса с запросами DHCP или DNS к сети.</span><span class="sxs-lookup"><span data-stu-id="5c034-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c034-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="5c034-116">Содержит сведения о сертификате, возвращенные с сервера.</span><span class="sxs-lookup"><span data-stu-id="5c034-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="5c034-117">Эта структура используется функцией [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="5c034-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-118">**WINHTTP_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="5c034-118">**WINHTTP_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

<span data-ttu-id="5c034-119">Представляет группу соединений.</span><span class="sxs-lookup"><span data-stu-id="5c034-119">Represents a connection group.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-120">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c034-120">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="5c034-121">Содержит исходный и конечный IP-адрес запроса, создавшего ответ.</span><span class="sxs-lookup"><span data-stu-id="5c034-121">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-122">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="5c034-122">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="5c034-123">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="5c034-123">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="5c034-124">Эта структура устарела.</span><span class="sxs-lookup"><span data-stu-id="5c034-124">This structure has been deprecated.</span></span> <span data-ttu-id="5c034-125">Вместо этого рекомендуется использовать структуру [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="5c034-125">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-126">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="5c034-126">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="5c034-127">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="5c034-127">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="5c034-128">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="5c034-129">Содержит сведения о конфигурации прокси-сервера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c034-129">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-130">**WINHTTP_EXTENDED_HEADER**</span><span class="sxs-lookup"><span data-stu-id="5c034-130">**WINHTTP_EXTENDED_HEADER**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

<span data-ttu-id="5c034-131">Представляет заголовок HTTP-запроса в виде пары "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="5c034-131">Represents an HTTP request header as a name/value string pair.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-132">**WINHTTP_HEADER_NAME**</span><span class="sxs-lookup"><span data-stu-id="5c034-132">**WINHTTP_HEADER_NAME**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

<span data-ttu-id="5c034-133">Представляет имя заголовка HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="5c034-133">Represents an HTTP request header name.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-134">**WINHTTP_HOST_CONNECTION_GROUP**</span><span class="sxs-lookup"><span data-stu-id="5c034-134">**WINHTTP_HOST_CONNECTION_GROUP**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

<span data-ttu-id="5c034-135">Представляет коллекцию групп соединений.</span><span class="sxs-lookup"><span data-stu-id="5c034-135">Represents a collection of connection groups.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-136">**WINHTTP_MATCH_CONNECTION_GUID**</span><span class="sxs-lookup"><span data-stu-id="5c034-136">**WINHTTP_MATCH_CONNECTION_GUID**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

<span data-ttu-id="5c034-137">Представляет идентификатор GUID соединения в целях сопоставления соединений.</span><span class="sxs-lookup"><span data-stu-id="5c034-137">Represents the GUID of a connection, for purposes of connection-matching.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-138">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c034-138">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="5c034-139">Содержит конфигурацию сеанса или прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c034-139">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-140">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c034-140">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="5c034-141">Коллекция записей результатов прокси-сервера, предоставляемых [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="5c034-141">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-142">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="5c034-142">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="5c034-143">Результирующая запись из вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="5c034-143">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c034-144">**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**</span></span>](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

<span data-ttu-id="5c034-145">Представляет описание текущего состояния соединений WinHttp.</span><span class="sxs-lookup"><span data-stu-id="5c034-145">Represents a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-146">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="5c034-146">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="5c034-147">Содержит статистику для запроса.</span><span class="sxs-lookup"><span data-stu-id="5c034-147">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-148">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="5c034-148">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="5c034-149">Содержит сведения о времени для запроса.</span><span class="sxs-lookup"><span data-stu-id="5c034-149">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-150">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="5c034-150">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="5c034-151">Содержит подключение SChannel и сведения о шифровании для запроса.</span><span class="sxs-lookup"><span data-stu-id="5c034-151">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="5c034-152">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="5c034-153">Состояние результата операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5c034-153">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="5c034-154">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="5c034-154">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="5c034-155">Состояние операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5c034-155">Status of a WebSocket operation.</span></span>

</dd> </dl>
