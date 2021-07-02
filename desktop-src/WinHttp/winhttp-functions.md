---
description: В этом разделе определяются функции, предоставляемые WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Функции WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174972"
---
# <a name="winhttp-functions"></a><span data-ttu-id="ad162-103">Функции WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ad162-103">WinHTTP Functions</span></span>

<span data-ttu-id="ad162-104">Службы WinHTTP предоставляют следующие функции.</span><span class="sxs-lookup"><span data-stu-id="ad162-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="ad162-105">**винхттпаддрекуессеадерс**</span><span class="sxs-lookup"><span data-stu-id="ad162-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="ad162-106">Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="ad162-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-107">**винхттпаддрекуессеадерсекс**</span><span class="sxs-lookup"><span data-stu-id="ad162-107">**WinHttpAddRequestHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

<span data-ttu-id="ad162-108">Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запросов, что позволяет использовать отдельные строки имени и значения.</span><span class="sxs-lookup"><span data-stu-id="ad162-108">Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-109">**винхттпчеккплатформ**</span><span class="sxs-lookup"><span data-stu-id="ad162-109">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="ad162-110">Определяет, поддерживается ли в WinHTTP текущая платформа.</span><span class="sxs-lookup"><span data-stu-id="ad162-110">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-111">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="ad162-111">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="ad162-112">Закрывает один [хинтернет](hinternet-handles-in-winhttp.md) -маркер.</span><span class="sxs-lookup"><span data-stu-id="ad162-112">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-113">**винхттпконнект**</span><span class="sxs-lookup"><span data-stu-id="ad162-113">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="ad162-114">Указывает начальный целевой сервер HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="ad162-114">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-115">**винхттпкраккурл**</span><span class="sxs-lookup"><span data-stu-id="ad162-115">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="ad162-116">Разделяет URL-адрес на части его компонентов, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="ad162-116">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-117">**винхттпкреатепроксиресолвер**</span><span class="sxs-lookup"><span data-stu-id="ad162-117">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="ad162-118">Создает маркер для использования [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="ad162-118">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-119">**винхттпкреатеурл**</span><span class="sxs-lookup"><span data-stu-id="ad162-119">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="ad162-120">Создает URL-адрес из частей компонента, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="ad162-120">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-121">**винхттпдетектаутопроксиконфигурл**</span><span class="sxs-lookup"><span data-stu-id="ad162-121">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="ad162-122">Поиск URL-адреса для файла автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="ad162-122">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="ad162-123">Эта функция сообщает URL-адрес файла PAC, но не скачивает файл.</span><span class="sxs-lookup"><span data-stu-id="ad162-123">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-124">**винхттпфрипроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="ad162-124">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="ad162-125">Освобождает данные, полученные из предыдущего вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="ad162-125">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-126">**винхттпфрикуериконнектионграупресулт**</span><span class="sxs-lookup"><span data-stu-id="ad162-126">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="ad162-127">Освобождает память, выделенную предыдущим вызовом [винхттпкуериконнектионграуп](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span><span class="sxs-lookup"><span data-stu-id="ad162-127">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-128">**винхттпжетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="ad162-128">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="ad162-129">Извлекает конфигурацию прокси WinHTTP по умолчанию из реестра.</span><span class="sxs-lookup"><span data-stu-id="ad162-129">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-130">**винхттпжетиепроксиконфигфоркуррентусер**</span><span class="sxs-lookup"><span data-stu-id="ad162-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="ad162-131">Получает конфигурацию прокси-сервера Internet Explorer (IE) для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad162-131">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-132">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="ad162-132">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="ad162-133">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ad162-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-134">**винхттпжетпроксифорурлекс**</span><span class="sxs-lookup"><span data-stu-id="ad162-134">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="ad162-135">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ad162-135">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-136">**винхттпжетпроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="ad162-136">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="ad162-137">Получает результаты вызова [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="ad162-137">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-138">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="ad162-138">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="ad162-139">Инициализирует использование приложением функций WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ad162-139">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-140">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="ad162-140">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="ad162-141">Создает обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="ad162-141">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-142">**винхттпкуеряуссчемес**</span><span class="sxs-lookup"><span data-stu-id="ad162-142">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="ad162-143">Возвращает схемы авторизации, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="ad162-143">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-144">**винхттпкуериконнектионграуп**</span><span class="sxs-lookup"><span data-stu-id="ad162-144">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="ad162-145">Извлекает описание текущего состояния соединений WinHttp.</span><span class="sxs-lookup"><span data-stu-id="ad162-145">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-146">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="ad162-146">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="ad162-147">Возвращает число байтов данных, которые сразу же читаются с помощью [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="ad162-147">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-148">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="ad162-148">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="ad162-149">Получает сведения о заголовке, связанные с HTTP-запросом.</span><span class="sxs-lookup"><span data-stu-id="ad162-149">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-150">**винхттпкуерихеадерсекс**</span><span class="sxs-lookup"><span data-stu-id="ad162-150">**WinHttpQueryHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

<span data-ttu-id="ad162-151">Получает сведения о заголовке, связанные с HTTP-запросом; предоставляет способ получения проанализированных строк имени и значения заголовка.</span><span class="sxs-lookup"><span data-stu-id="ad162-151">Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-152">**винхттпкуерйоптион**</span><span class="sxs-lookup"><span data-stu-id="ad162-152">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="ad162-153">Запрашивает параметр Интернета для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="ad162-153">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-154">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="ad162-154">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="ad162-155">Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="ad162-155">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-156">**винхттпреаддатаекс**</span><span class="sxs-lookup"><span data-stu-id="ad162-156">**WinHttpReadDataEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

<span data-ttu-id="ad162-157">Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="ad162-157">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-158">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="ad162-158">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="ad162-159">Завершает HTTP-запрос, инициированный [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ad162-159">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-160">**винхттпресетаутопрокси**</span><span class="sxs-lookup"><span data-stu-id="ad162-160">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="ad162-161">Сбрасывает параметр Auto-proxy.</span><span class="sxs-lookup"><span data-stu-id="ad162-161">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-162">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="ad162-162">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="ad162-163">Отправляет указанный запрос на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="ad162-163">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-164">**винхттпсеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="ad162-164">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="ad162-165">Передает на сервер необходимые учетные данные авторизации.</span><span class="sxs-lookup"><span data-stu-id="ad162-165">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-166">**винхттпсетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="ad162-166">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="ad162-167">Задает конфигурацию WinHTTP прокси по умолчанию в реестре.</span><span class="sxs-lookup"><span data-stu-id="ad162-167">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-168">**винхттпсетоптион**</span><span class="sxs-lookup"><span data-stu-id="ad162-168">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="ad162-169">Задает параметр Интернета.</span><span class="sxs-lookup"><span data-stu-id="ad162-169">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-170">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="ad162-170">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="ad162-171">Настраивает функцию обратного вызова, которую WinHTTP может вызвать во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ad162-171">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-172">**винхттпсеттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="ad162-172">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="ad162-173">Задает различные тайм-ауты, связанные с HTTP-транзакциями.</span><span class="sxs-lookup"><span data-stu-id="ad162-173">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-174">**винхттптимефромсистемтиме**</span><span class="sxs-lookup"><span data-stu-id="ad162-174">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="ad162-175">Форматирует дату и время согласно спецификации HTTP версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad162-175">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-176">**винхттптиметосистемтиме**</span><span class="sxs-lookup"><span data-stu-id="ad162-176">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="ad162-177">Принимает строку времени или даты HTTP и преобразует ее в структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="ad162-177">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-178">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="ad162-178">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="ad162-179">Записывает данные запроса на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="ad162-179">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-180">**винхттпвебсоккетклосе**</span><span class="sxs-lookup"><span data-stu-id="ad162-180">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="ad162-181">Закрывает соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad162-181">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-182">**винхттпвебсоккеткомплетеупграде**</span><span class="sxs-lookup"><span data-stu-id="ad162-182">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="ad162-183">Завершает подтверждение соединения WebSocket, запущенное [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="ad162-183">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-184">**винхттпвебсоккеткуериклосестатус**</span><span class="sxs-lookup"><span data-stu-id="ad162-184">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="ad162-185">Возвращает состояние закрытия, отправленное сервером.</span><span class="sxs-lookup"><span data-stu-id="ad162-185">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-186">**винхттпвебсоккетрецеиве**</span><span class="sxs-lookup"><span data-stu-id="ad162-186">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="ad162-187">Получает данные из соединения WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad162-187">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-188">**винхттпвебсоккетсенд**</span><span class="sxs-lookup"><span data-stu-id="ad162-188">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="ad162-189">Отправляет данные через соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad162-189">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ad162-190">**винхттпвебсоккетшутдовн**</span><span class="sxs-lookup"><span data-stu-id="ad162-190">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="ad162-191">Отправляет закрывающий кадр в соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="ad162-191">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>


