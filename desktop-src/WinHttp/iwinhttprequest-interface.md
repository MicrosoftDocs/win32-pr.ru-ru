---
description: Интерфейс Ивинхттпрекуест предоставляет все нечетные методы для служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Интерфейс Ивинхттпрекуест
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264807"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="2fcf0-103">Интерфейс Ивинхттпрекуест</span><span class="sxs-lookup"><span data-stu-id="2fcf0-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="2fcf0-104">Интерфейс **ивинхттпрекуест** предоставляет все нечетные методы для [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="2fcf0-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="2fcf0-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="2fcf0-105">Members</span></span>

<span data-ttu-id="2fcf0-106">Интерфейс **ивинхттпрекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2fcf0-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2fcf0-107">**Ивинхттпрекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2fcf0-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="2fcf0-108">Методы</span><span class="sxs-lookup"><span data-stu-id="2fcf0-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="2fcf0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="2fcf0-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2fcf0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2fcf0-110">Methods</span></span>

<span data-ttu-id="2fcf0-111">Интерфейс **ивинхттпрекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="2fcf0-112">Метод</span><span class="sxs-lookup"><span data-stu-id="2fcf0-112">Method</span></span>                                                                 | <span data-ttu-id="2fcf0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2fcf0-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fcf0-114">**Рвал**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="2fcf0-115">Прерывает метод Send [WinHTTP](about-winhttp.md) [](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="2fcf0-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="2fcf0-116">**жеталлреспонсехеадерс**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="2fcf0-117">Извлекает все заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2fcf0-118">**жетреспонсехеадер**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="2fcf0-119">Извлекает заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="2fcf0-120">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="2fcf0-121">Открывает HTTP-соединение с HTTP-ресурсом.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="2fcf0-122">**Отправить**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="2fcf0-123">Отправляет HTTP-запрос на сервер HTTP.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="2fcf0-124">**сетаутологонполици**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="2fcf0-125">Задает текущую [политику автоматического входа в систему](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="2fcf0-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="2fcf0-126">**сетклиентцертификате**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="2fcf0-127">Выбирает сертификат клиента для отправки на HTTPS-сервер.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="2fcf0-128">**сеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="2fcf0-129">Задает учетные данные для использования с сервером HTTP, прокси-сервером или исходным сервером.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="2fcf0-130">**сетпрокси**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="2fcf0-131">Задает сведения о прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2fcf0-132">**сетрекуессеадер**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="2fcf0-133">Добавляет, изменяет или удаляет заголовок HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="2fcf0-134">**сеттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="2fcf0-135">Задает отдельные компоненты времени ожидания операции отправки и получения в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="2fcf0-136">**ваитфорреспонсе**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="2fcf0-137">Ожидает завершения асинхронного метода [**Send**](iwinhttprequest-send.md) с необязательным значением времени ожидания в секундах.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2fcf0-138">Свойства</span><span class="sxs-lookup"><span data-stu-id="2fcf0-138">Properties</span></span>

<span data-ttu-id="2fcf0-139">Интерфейс **ивинхттпрекуест** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="2fcf0-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="2fcf0-140">Property</span></span>                                                            | <span data-ttu-id="2fcf0-141">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2fcf0-141">Access type</span></span>           | <span data-ttu-id="2fcf0-142">Описание</span><span class="sxs-lookup"><span data-stu-id="2fcf0-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="2fcf0-143">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="2fcf0-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2fcf0-144">Read/write</span></span><br/> | <span data-ttu-id="2fcf0-145">Значение параметра WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="2fcf0-146">**респонсебоди**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="2fcf0-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fcf0-147">Read-only</span></span><br/>  | <span data-ttu-id="2fcf0-148">Тело сущности ответа в виде массива байтов без знака.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="2fcf0-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="2fcf0-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fcf0-150">Read-only</span></span><br/>  | <span data-ttu-id="2fcf0-151">Тело сущности ответа в виде [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="2fcf0-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="2fcf0-152">**респонсетекст**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="2fcf0-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fcf0-153">Read-only</span></span><br/>  | <span data-ttu-id="2fcf0-154">Тело объекта ответа.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="2fcf0-155">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="2fcf0-156">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fcf0-156">Read-only</span></span><br/>  | <span data-ttu-id="2fcf0-157">Код состояния HTTP из последнего ответа.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="2fcf0-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="2fcf0-159">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2fcf0-159">Read-only</span></span><br/>  | <span data-ttu-id="2fcf0-160">Текст состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="2fcf0-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fcf0-161">Remarks</span></span>

<span data-ttu-id="2fcf0-162">Интерфейс **ивинхттпрекуест** , определенный в HttpRequest. idl, реализуется классом с идентификатором **CLSID \_ WinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="2fcf0-163">Приложение получает этот интерфейс, вызывая [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ WinHttpRequest** и идентификатором интерфейса **IID \_ ивинхттпрекуест**.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="2fcf0-164">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2fcf0-165">Требования</span><span class="sxs-lookup"><span data-stu-id="2fcf0-165">Requirements</span></span>



| <span data-ttu-id="2fcf0-166">Требование</span><span class="sxs-lookup"><span data-stu-id="2fcf0-166">Requirement</span></span> | <span data-ttu-id="2fcf0-167">Значение</span><span class="sxs-lookup"><span data-stu-id="2fcf0-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcf0-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fcf0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcf0-169">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2fcf0-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2fcf0-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fcf0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcf0-171">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2fcf0-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2fcf0-172">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2fcf0-172">Redistributable</span></span><br/>          | <span data-ttu-id="2fcf0-173">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2fcf0-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2fcf0-174">IDL</span><span class="sxs-lookup"><span data-stu-id="2fcf0-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fcf0-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf0-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2fcf0-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2fcf0-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fcf0-177"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf0-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2fcf0-178">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcf0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcf0-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf0-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2fcf0-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fcf0-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcf0-181">**ивинхттпрекуестевентс**</span><span class="sxs-lookup"><span data-stu-id="2fcf0-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="2fcf0-182">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2fcf0-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

