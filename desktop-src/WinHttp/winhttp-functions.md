---
description: В этом разделе определяются функции, предоставляемые WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Функции WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587749"
---
# <a name="winhttp-functions"></a><span data-ttu-id="80510-103">Функции WinHTTP</span><span class="sxs-lookup"><span data-stu-id="80510-103">WinHTTP Functions</span></span>

<span data-ttu-id="80510-104">Службы WinHTTP предоставляют следующие функции.</span><span class="sxs-lookup"><span data-stu-id="80510-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="80510-105">**винхттпаддрекуессеадерс**</span><span class="sxs-lookup"><span data-stu-id="80510-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="80510-106">Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="80510-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-107">**винхттпчеккплатформ**</span><span class="sxs-lookup"><span data-stu-id="80510-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="80510-108">Определяет, поддерживается ли в WinHTTP текущая платформа.</span><span class="sxs-lookup"><span data-stu-id="80510-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="80510-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="80510-110">Закрывает один [хинтернет](hinternet-handles-in-winhttp.md) -маркер.</span><span class="sxs-lookup"><span data-stu-id="80510-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-111">**винхттпконнект**</span><span class="sxs-lookup"><span data-stu-id="80510-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="80510-112">Указывает начальный целевой сервер HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="80510-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-113">**винхттпкраккурл**</span><span class="sxs-lookup"><span data-stu-id="80510-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="80510-114">Разделяет URL-адрес на части его компонентов, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="80510-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-115">**винхттпкреатепроксиресолвер**</span><span class="sxs-lookup"><span data-stu-id="80510-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="80510-116">Создает маркер для использования [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="80510-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-117">**винхттпкреатеурл**</span><span class="sxs-lookup"><span data-stu-id="80510-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="80510-118">Создает URL-адрес из частей компонента, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="80510-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-119">**винхттпдетектаутопроксиконфигурл**</span><span class="sxs-lookup"><span data-stu-id="80510-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="80510-120">Поиск URL-адреса для файла автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="80510-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="80510-121">Эта функция сообщает URL-адрес файла PAC, но не скачивает файл.</span><span class="sxs-lookup"><span data-stu-id="80510-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-122">**винхттпфрипроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="80510-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="80510-123">Освобождает данные, полученные из предыдущего вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="80510-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-124">**винхттпфрикуериконнектионграупресулт**</span><span class="sxs-lookup"><span data-stu-id="80510-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="80510-125">Освобождает память, выделенную предыдущим вызовом [винхттпкуериконнектионграуп](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span><span class="sxs-lookup"><span data-stu-id="80510-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-126">**винхттпжетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="80510-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="80510-127">Извлекает конфигурацию прокси WinHTTP по умолчанию из реестра.</span><span class="sxs-lookup"><span data-stu-id="80510-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-128">**винхттпжетиепроксиконфигфоркуррентусер**</span><span class="sxs-lookup"><span data-stu-id="80510-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="80510-129">Получает конфигурацию прокси-сервера Internet Explorer (IE) для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="80510-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="80510-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="80510-131">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="80510-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-132">**винхттпжетпроксифорурлекс**</span><span class="sxs-lookup"><span data-stu-id="80510-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="80510-133">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="80510-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-134">**винхттпжетпроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="80510-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="80510-135">Получает результаты вызова [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="80510-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="80510-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="80510-137">Инициализирует использование приложением функций WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="80510-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="80510-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="80510-139">Создает обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="80510-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-140">**винхттпкуеряуссчемес**</span><span class="sxs-lookup"><span data-stu-id="80510-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="80510-141">Возвращает схемы авторизации, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="80510-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-142">**винхттпкуериконнектионграуп**</span><span class="sxs-lookup"><span data-stu-id="80510-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="80510-143">Извлекает описание текущего состояния соединений WinHttp.</span><span class="sxs-lookup"><span data-stu-id="80510-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="80510-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="80510-145">Возвращает число байтов данных, которые сразу же читаются с помощью [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="80510-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="80510-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="80510-147">Получает сведения о заголовке, связанные с HTTP-запросом.</span><span class="sxs-lookup"><span data-stu-id="80510-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-148">**винхттпкуерйоптион**</span><span class="sxs-lookup"><span data-stu-id="80510-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="80510-149">Запрашивает параметр Интернета для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="80510-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="80510-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="80510-151">Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="80510-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="80510-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="80510-153">Завершает HTTP-запрос, инициированный [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="80510-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-154">**винхттпресетаутопрокси**</span><span class="sxs-lookup"><span data-stu-id="80510-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="80510-155">Сбрасывает параметр Auto-proxy.</span><span class="sxs-lookup"><span data-stu-id="80510-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="80510-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="80510-157">Отправляет указанный запрос на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="80510-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-158">**винхттпсеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="80510-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="80510-159">Передает на сервер необходимые учетные данные авторизации.</span><span class="sxs-lookup"><span data-stu-id="80510-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-160">**винхттпсетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="80510-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="80510-161">Задает конфигурацию WinHTTP прокси по умолчанию в реестре.</span><span class="sxs-lookup"><span data-stu-id="80510-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-162">**винхттпсетоптион**</span><span class="sxs-lookup"><span data-stu-id="80510-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="80510-163">Задает параметр Интернета.</span><span class="sxs-lookup"><span data-stu-id="80510-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="80510-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="80510-165">Настраивает функцию обратного вызова, которую WinHTTP может вызвать во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="80510-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-166">**винхттпсеттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="80510-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="80510-167">Задает различные тайм-ауты, связанные с HTTP-транзакциями.</span><span class="sxs-lookup"><span data-stu-id="80510-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-168">**винхттптимефромсистемтиме**</span><span class="sxs-lookup"><span data-stu-id="80510-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="80510-169">Форматирует дату и время согласно спецификации HTTP версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="80510-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-170">**винхттптиметосистемтиме**</span><span class="sxs-lookup"><span data-stu-id="80510-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="80510-171">Принимает строку времени или даты HTTP и преобразует ее в структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="80510-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="80510-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="80510-173">Записывает данные запроса на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="80510-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-174">**винхттпвебсоккетклосе**</span><span class="sxs-lookup"><span data-stu-id="80510-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="80510-175">Закрывает соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="80510-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-176">**винхттпвебсоккеткомплетеупграде**</span><span class="sxs-lookup"><span data-stu-id="80510-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="80510-177">Завершает подтверждение соединения WebSocket, запущенное [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="80510-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="80510-178">**винхттпвебсоккеткуериклосестатус**</span><span class="sxs-lookup"><span data-stu-id="80510-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="80510-179">Возвращает состояние закрытия, отправленное сервером.</span><span class="sxs-lookup"><span data-stu-id="80510-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-180">**винхттпвебсоккетрецеиве**</span><span class="sxs-lookup"><span data-stu-id="80510-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="80510-181">Получает данные из соединения WebSocket.</span><span class="sxs-lookup"><span data-stu-id="80510-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-182">**винхттпвебсоккетсенд**</span><span class="sxs-lookup"><span data-stu-id="80510-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="80510-183">Отправляет данные через соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="80510-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="80510-184">**винхттпвебсоккетшутдовн**</span><span class="sxs-lookup"><span data-stu-id="80510-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="80510-185">Отправляет закрывающий кадр в соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="80510-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
