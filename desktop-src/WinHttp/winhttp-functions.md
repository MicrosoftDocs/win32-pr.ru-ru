---
description: В этом разделе определяются функции, предоставляемые WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Функции WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701578"
---
# <a name="winhttp-functions"></a><span data-ttu-id="014ab-103">Функции WinHTTP</span><span class="sxs-lookup"><span data-stu-id="014ab-103">WinHTTP Functions</span></span>

<span data-ttu-id="014ab-104">Службы WinHTTP предоставляют следующие функции.</span><span class="sxs-lookup"><span data-stu-id="014ab-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="014ab-105">**винхттпаддрекуессеадерс**</span><span class="sxs-lookup"><span data-stu-id="014ab-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="014ab-106">Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="014ab-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-107">**винхттпчеккплатформ**</span><span class="sxs-lookup"><span data-stu-id="014ab-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="014ab-108">Определяет, поддерживается ли в WinHTTP текущая платформа.</span><span class="sxs-lookup"><span data-stu-id="014ab-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="014ab-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="014ab-110">Закрывает один [хинтернет](hinternet-handles-in-winhttp.md) -маркер.</span><span class="sxs-lookup"><span data-stu-id="014ab-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-111">**винхттпконнект**</span><span class="sxs-lookup"><span data-stu-id="014ab-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="014ab-112">Указывает начальный целевой сервер HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="014ab-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-113">**винхттпкраккурл**</span><span class="sxs-lookup"><span data-stu-id="014ab-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="014ab-114">Разделяет URL-адрес на части его компонентов, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="014ab-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-115">**винхттпкреатепроксиресолвер**</span><span class="sxs-lookup"><span data-stu-id="014ab-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="014ab-116">Создает маркер для использования [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="014ab-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-117">**винхттпкреатеурл**</span><span class="sxs-lookup"><span data-stu-id="014ab-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="014ab-118">Создает URL-адрес из частей компонента, например имя узла и путь.</span><span class="sxs-lookup"><span data-stu-id="014ab-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-119">**винхттпдетектаутопроксиконфигурл**</span><span class="sxs-lookup"><span data-stu-id="014ab-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="014ab-120">Поиск URL-адреса для файла автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="014ab-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="014ab-121">Эта функция сообщает URL-адрес файла PAC, но не скачивает файл.</span><span class="sxs-lookup"><span data-stu-id="014ab-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-122">**винхттпфрипроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="014ab-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="014ab-123">Освобождает данные, полученные из предыдущего вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="014ab-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-124">**винхттпжетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="014ab-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="014ab-125">Извлекает конфигурацию прокси WinHTTP по умолчанию из реестра.</span><span class="sxs-lookup"><span data-stu-id="014ab-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-126">**винхттпжетиепроксиконфигфоркуррентусер**</span><span class="sxs-lookup"><span data-stu-id="014ab-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="014ab-127">Получает конфигурацию прокси-сервера Internet Explorer (IE) для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="014ab-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="014ab-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="014ab-129">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="014ab-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-130">**винхттпжетпроксифорурлекс**</span><span class="sxs-lookup"><span data-stu-id="014ab-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="014ab-131">Получает сведения о прокси-сервере для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="014ab-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-132">**винхттпжетпроксиресулт**</span><span class="sxs-lookup"><span data-stu-id="014ab-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="014ab-133">Получает результаты вызова [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="014ab-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="014ab-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="014ab-135">Инициализирует использование приложением функций WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="014ab-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-136">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="014ab-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="014ab-137">Создает обработчик HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="014ab-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-138">**винхттпкуеряуссчемес**</span><span class="sxs-lookup"><span data-stu-id="014ab-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="014ab-139">Возвращает схемы авторизации, поддерживаемые сервером.</span><span class="sxs-lookup"><span data-stu-id="014ab-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="014ab-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="014ab-141">Возвращает число байтов данных, которые сразу же читаются с помощью [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="014ab-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="014ab-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="014ab-143">Получает сведения о заголовке, связанные с HTTP-запросом.</span><span class="sxs-lookup"><span data-stu-id="014ab-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-144">**винхттпкуерйоптион**</span><span class="sxs-lookup"><span data-stu-id="014ab-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="014ab-145">Запрашивает параметр Интернета для указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="014ab-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="014ab-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="014ab-147">Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="014ab-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="014ab-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="014ab-149">Завершает HTTP-запрос, инициированный [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="014ab-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-150">**винхттпресетаутопрокси**</span><span class="sxs-lookup"><span data-stu-id="014ab-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="014ab-151">Сбрасывает параметр Auto-proxy.</span><span class="sxs-lookup"><span data-stu-id="014ab-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="014ab-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="014ab-153">Отправляет указанный запрос на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="014ab-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-154">**винхттпсеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="014ab-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="014ab-155">Передает на сервер необходимые учетные данные авторизации.</span><span class="sxs-lookup"><span data-stu-id="014ab-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-156">**винхттпсетдефаултпроксиконфигуратион**</span><span class="sxs-lookup"><span data-stu-id="014ab-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="014ab-157">Задает конфигурацию WinHTTP прокси по умолчанию в реестре.</span><span class="sxs-lookup"><span data-stu-id="014ab-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-158">**винхттпсетоптион**</span><span class="sxs-lookup"><span data-stu-id="014ab-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="014ab-159">Задает параметр Интернета.</span><span class="sxs-lookup"><span data-stu-id="014ab-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-160">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="014ab-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="014ab-161">Настраивает функцию обратного вызова, которую WinHTTP может вызвать во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="014ab-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-162">**винхттпсеттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="014ab-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="014ab-163">Задает различные тайм-ауты, связанные с HTTP-транзакциями.</span><span class="sxs-lookup"><span data-stu-id="014ab-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-164">**винхттптимефромсистемтиме**</span><span class="sxs-lookup"><span data-stu-id="014ab-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="014ab-165">Форматирует дату и время согласно спецификации HTTP версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="014ab-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-166">**винхттптиметосистемтиме**</span><span class="sxs-lookup"><span data-stu-id="014ab-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="014ab-167">Принимает строку времени или даты HTTP и преобразует ее в структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="014ab-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-168">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="014ab-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="014ab-169">Записывает данные запроса на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="014ab-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-170">**винхттпвебсоккетклосе**</span><span class="sxs-lookup"><span data-stu-id="014ab-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="014ab-171">Закрывает соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="014ab-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-172">**винхттпвебсоккеткомплетеупграде**</span><span class="sxs-lookup"><span data-stu-id="014ab-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="014ab-173">Завершает подтверждение соединения WebSocket, запущенное [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="014ab-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-174">**винхттпвебсоккеткуериклосестатус**</span><span class="sxs-lookup"><span data-stu-id="014ab-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="014ab-175">Возвращает состояние закрытия, отправленное сервером.</span><span class="sxs-lookup"><span data-stu-id="014ab-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-176">**винхттпвебсоккетрецеиве**</span><span class="sxs-lookup"><span data-stu-id="014ab-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="014ab-177">Получает данные из соединения WebSocket.</span><span class="sxs-lookup"><span data-stu-id="014ab-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-178">**винхттпвебсоккетсенд**</span><span class="sxs-lookup"><span data-stu-id="014ab-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="014ab-179">Отправляет данные через соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="014ab-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="014ab-180">**винхттпвебсоккетшутдовн**</span><span class="sxs-lookup"><span data-stu-id="014ab-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="014ab-181">Отправляет закрывающий кадр в соединение WebSocket.</span><span class="sxs-lookup"><span data-stu-id="014ab-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
