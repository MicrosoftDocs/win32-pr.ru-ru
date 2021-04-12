---
description: В этом разделе определяются структуры, используемые WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Структуры WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263089"
---
# <a name="winhttp-structures"></a><span data-ttu-id="87a1c-103">Структуры WinHTTP</span><span class="sxs-lookup"><span data-stu-id="87a1c-103">WinHTTP structures</span></span>

<span data-ttu-id="87a1c-104">WinHTTP использует следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="87a1c-104">WinHTTP uses the following structures:</span></span>

<dl> <dt>

[<span data-ttu-id="87a1c-105">**HTTP_VERSION_INFO**</span><span class="sxs-lookup"><span data-stu-id="87a1c-105">**HTTP_VERSION_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

<span data-ttu-id="87a1c-106">Содержит глобальную версию HTTP.</span><span class="sxs-lookup"><span data-stu-id="87a1c-106">Contains the global HTTP version.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-107">**URL_COMPONENTS**</span><span class="sxs-lookup"><span data-stu-id="87a1c-107">**URL_COMPONENTS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

<span data-ttu-id="87a1c-108">Содержит составные части URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="87a1c-108">Contains the constituent parts of a URL.</span></span> <span data-ttu-id="87a1c-109">Эта структура используется с функциями [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .</span><span class="sxs-lookup"><span data-stu-id="87a1c-109">This structure is used with the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-110">**WINHTTP_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="87a1c-110">**WINHTTP_ASYNC_RESULT**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

<span data-ttu-id="87a1c-111">Содержит результат вызова асинхронной функции.</span><span class="sxs-lookup"><span data-stu-id="87a1c-111">Contains the result of a call to an asynchronous function.</span></span> <span data-ttu-id="87a1c-112">Эта структура используется с прототипом [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="87a1c-112">This structure is used with the [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototype.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-113">**WINHTTP_AUTOPROXY_OPTIONS**</span><span class="sxs-lookup"><span data-stu-id="87a1c-113">**WINHTTP_AUTOPROXY_OPTIONS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

<span data-ttu-id="87a1c-114">Используется для указания функции [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , следует ли указывать URL-адрес файла автоматической настройки прокси-сервера (PAC) или автоматически размещать URL-адреса с запросами DHCP или DNS к сети.</span><span class="sxs-lookup"><span data-stu-id="87a1c-114">Used to indicate to the [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function whether to specify the URL of the Proxy Auto-Configuration (PAC) file or to automatically locate the URL with DHCP or DNS queries to the network.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-115">**WINHTTP_CERTIFICATE_INFO**</span><span class="sxs-lookup"><span data-stu-id="87a1c-115">**WINHTTP_CERTIFICATE_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

<span data-ttu-id="87a1c-116">Содержит сведения о сертификате, возвращенные с сервера.</span><span class="sxs-lookup"><span data-stu-id="87a1c-116">Contains certificate information returned from the server.</span></span> <span data-ttu-id="87a1c-117">Эта структура используется функцией [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .</span><span class="sxs-lookup"><span data-stu-id="87a1c-117">This structure is used by the [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) function.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-118">**WINHTTP_CONNECTION_INFO**</span><span class="sxs-lookup"><span data-stu-id="87a1c-118">**WINHTTP_CONNECTION_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

<span data-ttu-id="87a1c-119">Содержит исходный и конечный IP-адрес запроса, создавшего ответ.</span><span class="sxs-lookup"><span data-stu-id="87a1c-119">Contains the source and destination IP address of the request that generated the response.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-120">**WINHTTP_CREDS**</span><span class="sxs-lookup"><span data-stu-id="87a1c-120">**WINHTTP_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

<span data-ttu-id="87a1c-121">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="87a1c-121">Contains user credential information used for server and proxy authentication.</span></span>

> [!Note]
> <span data-ttu-id="87a1c-122">Эта структура устарела.</span><span class="sxs-lookup"><span data-stu-id="87a1c-122">This structure has been deprecated.</span></span> <span data-ttu-id="87a1c-123">Вместо этого рекомендуется использовать структуру [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .</span><span class="sxs-lookup"><span data-stu-id="87a1c-123">Instead, the use of the [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure is recommended.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-124">**WINHTTP_CREDS_EX**</span><span class="sxs-lookup"><span data-stu-id="87a1c-124">**WINHTTP_CREDS_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

<span data-ttu-id="87a1c-125">Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.</span><span class="sxs-lookup"><span data-stu-id="87a1c-125">Contains user credential information used for server and proxy authentication.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span><span class="sxs-lookup"><span data-stu-id="87a1c-126">**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

<span data-ttu-id="87a1c-127">Содержит сведения о конфигурации прокси-сервера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="87a1c-127">Contains the Internet Explorer proxy configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-128">**WINHTTP_PROXY_INFO**</span><span class="sxs-lookup"><span data-stu-id="87a1c-128">**WINHTTP_PROXY_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

<span data-ttu-id="87a1c-129">Содержит конфигурацию сеанса или прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87a1c-129">Contains the session or default proxy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-130">**WINHTTP_PROXY_RESULT**</span><span class="sxs-lookup"><span data-stu-id="87a1c-130">**WINHTTP_PROXY_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

<span data-ttu-id="87a1c-131">Коллекция записей результатов прокси-сервера, предоставляемых [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="87a1c-131">A collection of proxy result entries provided by [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-132">**WINHTTP_PROXY_RESULT_ENTRY**</span><span class="sxs-lookup"><span data-stu-id="87a1c-132">**WINHTTP_PROXY_RESULT_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

<span data-ttu-id="87a1c-133">Результирующая запись из вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="87a1c-133">A result entry from a call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-134">**WINHTTP_REQUEST_STATS**</span><span class="sxs-lookup"><span data-stu-id="87a1c-134">**WINHTTP_REQUEST_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

<span data-ttu-id="87a1c-135">Содержит статистику для запроса.</span><span class="sxs-lookup"><span data-stu-id="87a1c-135">Contains statistics for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-136">**WINHTTP_REQUEST_TIMES**</span><span class="sxs-lookup"><span data-stu-id="87a1c-136">**WINHTTP_REQUEST_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

<span data-ttu-id="87a1c-137">Содержит сведения о времени для запроса.</span><span class="sxs-lookup"><span data-stu-id="87a1c-137">Contains timing information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-138">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="87a1c-138">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

<span data-ttu-id="87a1c-139">Содержит подключение SChannel и сведения о шифровании для запроса.</span><span class="sxs-lookup"><span data-stu-id="87a1c-139">Contains SChannel connection and cipher information for a request.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span><span class="sxs-lookup"><span data-stu-id="87a1c-140">**WINHTTP_WEB_SOCKET_ASYNC_RESULT**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

<span data-ttu-id="87a1c-141">Состояние результата операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="87a1c-141">Result status of a WebSocket operation.</span></span>

</dd> <dt>

[<span data-ttu-id="87a1c-142">**WINHTTP_WEB_SOCKET_STATUS**</span><span class="sxs-lookup"><span data-stu-id="87a1c-142">**WINHTTP_WEB_SOCKET_STATUS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

<span data-ttu-id="87a1c-143">Состояние операции WebSocket.</span><span class="sxs-lookup"><span data-stu-id="87a1c-143">Status of a WebSocket operation.</span></span>

</dd> </dl>
