---
Description: В этом разделе содержатся сведения об использовании COM-объекта WinHTTP WinHttpRequest с языками сценариев.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Объект WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704455"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="1d19f-103">Объект WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="1d19f-103">WinHttpRequest object</span></span>

<span data-ttu-id="1d19f-104">В этом разделе содержатся сведения об использовании COM-объекта WinHTTP **WinHttpRequest** с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="1d19f-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="1d19f-105">Дополнительные сведения, включая API C++ (WinHTTP), см. в статье [о WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="1d19f-106">Сравнение этих интерфейсов см. в разделе [Выбор интерфейса WinHTTP](choosing-a-winhttp-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="1d19f-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="1d19f-107">Пример</span><span class="sxs-lookup"><span data-stu-id="1d19f-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="1d19f-108">Примеры кода, взятые из [Свойства ивинхттпрекуест:: Status](iwinhttprequest-status.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="1d19f-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="1d19f-109">Members</span></span>

<span data-ttu-id="1d19f-110">Объект **WinHttpRequest** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1d19f-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="1d19f-111">События</span><span class="sxs-lookup"><span data-stu-id="1d19f-111">Events</span></span>](#events)
-   [<span data-ttu-id="1d19f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1d19f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d19f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d19f-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="1d19f-114">События</span><span class="sxs-lookup"><span data-stu-id="1d19f-114">Events</span></span>

<span data-ttu-id="1d19f-115">Объект **WinHttpRequest** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="1d19f-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="1d19f-116">Событие</span><span class="sxs-lookup"><span data-stu-id="1d19f-116">Event</span></span>                                                                            | <span data-ttu-id="1d19f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1d19f-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="1d19f-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="1d19f-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="1d19f-119">Происходит при возникновении ошибки времени выполнения в приложении.</span><span class="sxs-lookup"><span data-stu-id="1d19f-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="1d19f-120">**онреспонседатааваилабле**</span><span class="sxs-lookup"><span data-stu-id="1d19f-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="1d19f-121">Происходит при доступе к данным из ответа.</span><span class="sxs-lookup"><span data-stu-id="1d19f-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="1d19f-122">**онреспонсефинишед**</span><span class="sxs-lookup"><span data-stu-id="1d19f-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="1d19f-123">Происходит при завершении данных ответа.</span><span class="sxs-lookup"><span data-stu-id="1d19f-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="1d19f-124">**онреспонсестарт**</span><span class="sxs-lookup"><span data-stu-id="1d19f-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="1d19f-125">Происходит при начале получения данных ответа.</span><span class="sxs-lookup"><span data-stu-id="1d19f-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="1d19f-126">Методы</span><span class="sxs-lookup"><span data-stu-id="1d19f-126">Methods</span></span>

<span data-ttu-id="1d19f-127">Объект **WinHttpRequest** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1d19f-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="1d19f-128">Метод</span><span class="sxs-lookup"><span data-stu-id="1d19f-128">Method</span></span>                                                                 | <span data-ttu-id="1d19f-129">Описание</span><span class="sxs-lookup"><span data-stu-id="1d19f-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d19f-130">**Рвал**</span><span class="sxs-lookup"><span data-stu-id="1d19f-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="1d19f-131">Прерывает метод Send [WinHTTP](about-winhttp.md) [](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="1d19f-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="1d19f-132">**жеталлреспонсехеадерс**</span><span class="sxs-lookup"><span data-stu-id="1d19f-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="1d19f-133">Извлекает все заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d19f-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="1d19f-134">**жетреспонсехеадер**</span><span class="sxs-lookup"><span data-stu-id="1d19f-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="1d19f-135">Извлекает заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="1d19f-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="1d19f-136">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="1d19f-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="1d19f-137">Открывает HTTP-соединение с HTTP-ресурсом.</span><span class="sxs-lookup"><span data-stu-id="1d19f-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="1d19f-138">**Отправить**</span><span class="sxs-lookup"><span data-stu-id="1d19f-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="1d19f-139">Отправляет HTTP-запрос на сервер HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d19f-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="1d19f-140">**сетаутологонполици**</span><span class="sxs-lookup"><span data-stu-id="1d19f-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="1d19f-141">Задает текущую [политику автоматического входа в систему](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="1d19f-142">**сетклиентцертификате**</span><span class="sxs-lookup"><span data-stu-id="1d19f-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="1d19f-143">Выбирает сертификат клиента для отправки на HTTPS-сервер.</span><span class="sxs-lookup"><span data-stu-id="1d19f-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="1d19f-144">**сеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="1d19f-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="1d19f-145">Задает учетные данные для использования с HTTP-сервером либо исходным, либо прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="1d19f-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="1d19f-146">**сетпрокси**</span><span class="sxs-lookup"><span data-stu-id="1d19f-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="1d19f-147">Задает сведения о прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="1d19f-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="1d19f-148">**сетрекуессеадер**</span><span class="sxs-lookup"><span data-stu-id="1d19f-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="1d19f-149">Добавляет, изменяет или удаляет заголовок HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="1d19f-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="1d19f-150">**сеттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="1d19f-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="1d19f-151">Указывает в миллисекундах отдельные компоненты времени ожидания операции отправки и получения.</span><span class="sxs-lookup"><span data-stu-id="1d19f-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="1d19f-152">**ваитфорреспонсе**</span><span class="sxs-lookup"><span data-stu-id="1d19f-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="1d19f-153">Указывает время ожидания для завершения асинхронного метода [**отправки**](iwinhttprequest-send.md) (в секундах) с необязательным значением времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="1d19f-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d19f-154">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d19f-154">Properties</span></span>

<span data-ttu-id="1d19f-155">Объект **WinHttpRequest** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d19f-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="1d19f-156">Свойство</span><span class="sxs-lookup"><span data-stu-id="1d19f-156">Property</span></span>                                                            | <span data-ttu-id="1d19f-157">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="1d19f-157">Access type</span></span>           | <span data-ttu-id="1d19f-158">Описание</span><span class="sxs-lookup"><span data-stu-id="1d19f-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1d19f-159">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="1d19f-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="1d19f-160">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1d19f-160">Read/write</span></span><br/> | <span data-ttu-id="1d19f-161">Задает или получает значение параметра WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1d19f-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="1d19f-162">**респонсебоди**</span><span class="sxs-lookup"><span data-stu-id="1d19f-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="1d19f-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d19f-163">Read-only</span></span><br/>  | <span data-ttu-id="1d19f-164">Извлекает тело объекта ответа в виде массива байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="1d19f-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="1d19f-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="1d19f-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="1d19f-166">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d19f-166">Read-only</span></span><br/>  | <span data-ttu-id="1d19f-167">Извлекает тело объекта ответа в виде [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="1d19f-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="1d19f-168">**респонсетекст**</span><span class="sxs-lookup"><span data-stu-id="1d19f-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="1d19f-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d19f-169">Read-only</span></span><br/>  | <span data-ttu-id="1d19f-170">Извлекает текст объекта ответа в виде текста.</span><span class="sxs-lookup"><span data-stu-id="1d19f-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="1d19f-171">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1d19f-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="1d19f-172">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d19f-172">Read-only</span></span><br/>  | <span data-ttu-id="1d19f-173">Извлекает код состояния HTTP из последнего ответа.</span><span class="sxs-lookup"><span data-stu-id="1d19f-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="1d19f-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="1d19f-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="1d19f-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1d19f-175">Read-only</span></span><br/>  | <span data-ttu-id="1d19f-176">Получает текст состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d19f-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="1d19f-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d19f-177">Remarks</span></span>

<span data-ttu-id="1d19f-178">Объект **WinHttpRequest** использует интерфейс [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) для предоставления данных об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1d19f-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="1d19f-179">Описание и числовое значение ошибки можно получить с помощью объекта [Err](/previous-versions//sbf5ze0e(v=vs.85)) в Microsoft Visual Basic Scripting Edition (VBScript) и объекта [ошибки](https://msdn.microsoft.com/library/dww52sbt.aspx) в Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="1d19f-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="1d19f-180">Младшие 16 разрядов номера ошибки соответствуют значениям, находящихся в [**сообщениях об ошибках**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="1d19f-181">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d19f-182">Требования</span><span class="sxs-lookup"><span data-stu-id="1d19f-182">Requirements</span></span>



| <span data-ttu-id="1d19f-183">Требование</span><span class="sxs-lookup"><span data-stu-id="1d19f-183">Requirement</span></span> | <span data-ttu-id="1d19f-184">Значение</span><span class="sxs-lookup"><span data-stu-id="1d19f-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d19f-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d19f-185">Minimum supported client</span></span><br/> | <span data-ttu-id="1d19f-186">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d19f-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1d19f-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d19f-187">Minimum supported server</span></span><br/> | <span data-ttu-id="1d19f-188">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d19f-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1d19f-189">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1d19f-189">Redistributable</span></span><br/>          | <span data-ttu-id="1d19f-190">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1d19f-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1d19f-191">IDL</span><span class="sxs-lookup"><span data-stu-id="1d19f-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d19f-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d19f-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d19f-193">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d19f-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d19f-194"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d19f-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="1d19f-195">DLL</span><span class="sxs-lookup"><span data-stu-id="1d19f-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d19f-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d19f-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1d19f-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d19f-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d19f-198">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1d19f-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

