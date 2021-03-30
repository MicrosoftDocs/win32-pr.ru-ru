---
description: Значения ошибок, описанные в этом разделе, возвращаются функцией GetLastError при сбое одной из функций служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Сообщения об ошибках (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910851"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="7b77b-103">Сообщения об ошибках (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="7b77b-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="7b77b-104">Приведенные ниже значения ошибок возвращаются функцией [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) , если одна из функций служб Microsoft Windows HTTP (WinHTTP) завершается сбоем, и они также возвращаются в младших 16 битах возвращаемых ошибок [**HRESULT**](../com/structure-of-com-error-codes.md) из объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="7b77b-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="7b77b-105">Значения ошибок, имена которых начинаются с "ERROR \_ WinHTTP \_ ", относятся к функциям WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7b77b-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="7b77b-106">При необходимости функции WinHTTP также возвращают сообщения об ошибках Windows.</span><span class="sxs-lookup"><span data-stu-id="7b77b-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="7b77b-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**Ошибка \_ \_ службы автоматического \_ прокси-сервера WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-108">12178</span><span class="sxs-lookup"><span data-stu-id="7b77b-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-109">Возвращается функцией [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , если не удается найти прокси-сервер для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7b77b-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**Ошибка \_ \_ при автообнаружении WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-111">12180</span><span class="sxs-lookup"><span data-stu-id="7b77b-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-112">Возвращается функцией [**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) , если службе WinHTTP не удалось обнаружить URL-адрес файла автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="7b77b-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**Ошибка \_ WinHTTP \_ неверный \_ \_ Скрипт автоматического прокси \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-114">12166</span><span class="sxs-lookup"><span data-stu-id="7b77b-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-115">Произошла ошибка при исполнении кода скрипта в файле автоматической настройки прокси-сервера (PAC).</span><span class="sxs-lookup"><span data-stu-id="7b77b-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**Ошибка \_ WinHTTP \_ не удается \_ вызвать \_ после \_ открытия**</span><span class="sxs-lookup"><span data-stu-id="7b77b-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-117">12103</span><span class="sxs-lookup"><span data-stu-id="7b77b-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-118">Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается запросить указанный параметр после вызова метода [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7b77b-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**Ошибка \_ WinHTTP \_ не удается \_ вызвать \_ после \_ отправки**</span><span class="sxs-lookup"><span data-stu-id="7b77b-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-120">12102</span><span class="sxs-lookup"><span data-stu-id="7b77b-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-121">Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию после вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="7b77b-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**Ошибка \_ WinHTTP \_ не может \_ вызвать \_ перед \_ открытием**</span><span class="sxs-lookup"><span data-stu-id="7b77b-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-123">12100</span><span class="sxs-lookup"><span data-stu-id="7b77b-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-124">Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию до вызова метода [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7b77b-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**Ошибка \_ WinHTTP \_ не может \_ вызвать \_ перед \_ отправкой**</span><span class="sxs-lookup"><span data-stu-id="7b77b-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-126">12101</span><span class="sxs-lookup"><span data-stu-id="7b77b-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-127">Возвращается объектом [**HttpRequest**](winhttprequest.md) , если не удается выполнить запрошенную операцию до вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="7b77b-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**Ошибка \_ WinHTTP \_ не удается \_ подключиться**</span><span class="sxs-lookup"><span data-stu-id="7b77b-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-129">12029</span><span class="sxs-lookup"><span data-stu-id="7b77b-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-130">Возвращается при сбое соединения с сервером.</span><span class="sxs-lookup"><span data-stu-id="7b77b-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-132">Сервер требует проверки подлинности клиента SSL.</span><span class="sxs-lookup"><span data-stu-id="7b77b-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="7b77b-133">Приложение получает список издателей сертификатов, вызывая [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP Certificate \_ \_ Client \_ CERT \_ \_ List** .</span><span class="sxs-lookup"><span data-stu-id="7b77b-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="7b77b-134">Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .</span><span class="sxs-lookup"><span data-stu-id="7b77b-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="7b77b-135">Если сервер запрашивает сертификат клиента, но не требует его, приложение может дополнительно вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с параметром **\_ контекста WinHTTP параметр \_ \_ сертификата \_ клиента** .</span><span class="sxs-lookup"><span data-stu-id="7b77b-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="7b77b-136">В этом случае в приложении указывается \_ \_ Контекстный макрос WinHTTP No Client Certificate \_ \_ в параметре *лпбуффер* объекта **винхттпсетоптион**.</span><span class="sxs-lookup"><span data-stu-id="7b77b-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="7b77b-137">Дополнительные сведения см. в описании параметра службы **WinHTTP \_ параметр \_ \_ \_ контекста сертификата клиента** .</span><span class="sxs-lookup"><span data-stu-id="7b77b-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="7b77b-138">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**Ошибка \_ WinHTTP \_ \_ сертификат клиента \_ без \_ доступа \_ закрытый \_ ключ**</span><span class="sxs-lookup"><span data-stu-id="7b77b-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-140">У приложения нет необходимых привилегий для доступа к закрытому ключу, связанному с сертификатом клиента.</span><span class="sxs-lookup"><span data-stu-id="7b77b-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="7b77b-141">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**Ошибка \_ WinHTTP \_ \_ сертификат клиента \_ без \_ закрытого \_ ключа**</span><span class="sxs-lookup"><span data-stu-id="7b77b-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-143">Контекст для SSL-сертификата клиента не связан с закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="7b77b-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="7b77b-144">Сертификат клиента мог быть импортирован на компьютер без закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="7b77b-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="7b77b-145">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**Ошибка \_ при \_ \_ \_ \_ переполнении размера заголовка фрагментированной кодировки WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-147">12183</span><span class="sxs-lookup"><span data-stu-id="7b77b-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-148">Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) при обнаружении условия переполнения в процессе синтаксического анализа фрагментированной кодировки.</span><span class="sxs-lookup"><span data-stu-id="7b77b-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**Ошибка \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-150">12044</span><span class="sxs-lookup"><span data-stu-id="7b77b-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-151">Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , когда сервер запрашивает проверку подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="7b77b-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="7b77b-152">**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Эта ошибка не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**Ошибка \_ \_ подключения WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-154">12030</span><span class="sxs-lookup"><span data-stu-id="7b77b-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-155">Подключение к серверу было сброшено или прервано, или обнаружен несовместимый протокол SSL.</span><span class="sxs-lookup"><span data-stu-id="7b77b-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="7b77b-156">Например, служба WinHTTP версии 5,1 не поддерживает SSL2, если только клиент явно не включит ее.</span><span class="sxs-lookup"><span data-stu-id="7b77b-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**\_заголовок ошибки \_ WinHTTP \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="7b77b-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-158">12155</span><span class="sxs-lookup"><span data-stu-id="7b77b-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-159">Устаревшие больше не используется.</span><span class="sxs-lookup"><span data-stu-id="7b77b-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**Ошибка \_ при \_ \_ превышении числа заголовков WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-161">12181</span><span class="sxs-lookup"><span data-stu-id="7b77b-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-162">Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , если в ответе было больше заголовков, чем может получить WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7b77b-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена заголовок WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-164">12150</span><span class="sxs-lookup"><span data-stu-id="7b77b-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-165">Не удается найти запрошенный заголовок.</span><span class="sxs-lookup"><span data-stu-id="7b77b-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**Ошибка \_ \_ \_ переполнения размера заголовка WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-167">12182</span><span class="sxs-lookup"><span data-stu-id="7b77b-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-168">Возвращается функцией [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , если размер полученных заголовков превышает предельное значение для маркера запроса.</span><span class="sxs-lookup"><span data-stu-id="7b77b-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**Ошибка \_ WinHTTP \_ неправильное \_ состояние обработчика \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-170">12019</span><span class="sxs-lookup"><span data-stu-id="7b77b-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-171">Не удается выполнить запрошенную операцию, так как указанный обработчик находится в неправильном состоянии.</span><span class="sxs-lookup"><span data-stu-id="7b77b-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**Ошибка \_ WinHTTP \_ неверный \_ тип обработчика \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-173">12018</span><span class="sxs-lookup"><span data-stu-id="7b77b-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-174">Для этой операции указан недопустимый тип обработчика.</span><span class="sxs-lookup"><span data-stu-id="7b77b-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**Ошибка \_ \_ внутренней \_ ошибки WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-176">12004</span><span class="sxs-lookup"><span data-stu-id="7b77b-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-177">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b77b-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**</span><span class="sxs-lookup"><span data-stu-id="7b77b-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-179">12009</span><span class="sxs-lookup"><span data-stu-id="7b77b-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-180">Запрос к [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) или [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) указал недопустимое значение параметра.</span><span class="sxs-lookup"><span data-stu-id="7b77b-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ \_ запрос запроса**</span><span class="sxs-lookup"><span data-stu-id="7b77b-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-182">12154</span><span class="sxs-lookup"><span data-stu-id="7b77b-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-183">Устаревшие больше не используется.</span><span class="sxs-lookup"><span data-stu-id="7b77b-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ \_ ответ сервера**</span><span class="sxs-lookup"><span data-stu-id="7b77b-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-185">12152</span><span class="sxs-lookup"><span data-stu-id="7b77b-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-186">Не удается выполнить синтаксический анализ ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="7b77b-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**Ошибка \_ WinHTTP \_ Недопустимый \_ URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="7b77b-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-188">12005</span><span class="sxs-lookup"><span data-stu-id="7b77b-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-189">URL-адрес является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="7b77b-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**Ошибка \_ \_ при попытке входа WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-191">12015</span><span class="sxs-lookup"><span data-stu-id="7b77b-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-192">Ошибка при попытке входа.</span><span class="sxs-lookup"><span data-stu-id="7b77b-192">The login attempt failed.</span></span> <span data-ttu-id="7b77b-193">При обнаружении этой ошибки обработчик запроса должен быть закрыт с помощью [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span><span class="sxs-lookup"><span data-stu-id="7b77b-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="7b77b-194">Перед повторной попыткой функции, вызвавшей эту ошибку, должен быть создан новый обработчик запроса.</span><span class="sxs-lookup"><span data-stu-id="7b77b-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**Ошибка \_ \_ имя WinHTTP \_ не \_ разрешено**</span><span class="sxs-lookup"><span data-stu-id="7b77b-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-196">12007</span><span class="sxs-lookup"><span data-stu-id="7b77b-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-197">Не удается разрешить имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7b77b-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**Ошибка \_ WinHTTP \_ не \_ инициализирована**</span><span class="sxs-lookup"><span data-stu-id="7b77b-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-199">12172</span><span class="sxs-lookup"><span data-stu-id="7b77b-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-200">Устаревшие больше не используется.</span><span class="sxs-lookup"><span data-stu-id="7b77b-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**Ошибка \_ \_ операции WinHTTP \_ отменена**</span><span class="sxs-lookup"><span data-stu-id="7b77b-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-202">12017</span><span class="sxs-lookup"><span data-stu-id="7b77b-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-203">Операция была отменена, как правило, из-за того, что обработчик, на котором был запущен запрос, был закрыт до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7b77b-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**Ошибка \_ , \_ \_ не устанавливаемая параметром WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-205">12011</span><span class="sxs-lookup"><span data-stu-id="7b77b-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-206">Невозможно задать запрошенный параметр, выполняется только запрос.</span><span class="sxs-lookup"><span data-stu-id="7b77b-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**Ошибка \_ WinHTTP \_ вне \_ \_ дескрипторов**</span><span class="sxs-lookup"><span data-stu-id="7b77b-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-208">12001</span><span class="sxs-lookup"><span data-stu-id="7b77b-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-209">Устаревшие больше не используется.</span><span class="sxs-lookup"><span data-stu-id="7b77b-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**Ошибка \_ \_ при перенаправлении WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-211">12156</span><span class="sxs-lookup"><span data-stu-id="7b77b-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-212">Перенаправление завершилось сбоем, так как либо изменилась схема, либо все попытки перенаправления завершились неудачей (по умолчанию пять попыток).</span><span class="sxs-lookup"><span data-stu-id="7b77b-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**Ошибка \_ \_ запроса повторной отправки WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-214">12032</span><span class="sxs-lookup"><span data-stu-id="7b77b-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-215">Сбой функции WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7b77b-215">The WinHTTP function failed.</span></span> <span data-ttu-id="7b77b-216">Нужная функция может быть выполнена повторно с тем же маркером запроса.</span><span class="sxs-lookup"><span data-stu-id="7b77b-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**Ошибка \_ \_ \_ переполнения очистки ответа WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-218">12184</span><span class="sxs-lookup"><span data-stu-id="7b77b-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-219">Возвращается, когда входящий ответ превышает ограничение внутреннего размера WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7b77b-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**Ошибка \_ \_ при выполнении скрипта WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-221">12177</span><span class="sxs-lookup"><span data-stu-id="7b77b-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-222">При выполнении скрипта произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="7b77b-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**Ошибка \_ WinHTTP \_ \_ \_ \_ Недопустимый CN Secure CERT**</span><span class="sxs-lookup"><span data-stu-id="7b77b-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-224">12038</span><span class="sxs-lookup"><span data-stu-id="7b77b-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-225">Возвращается, если различающееся имя сертификата не соответствует переданному значению (что эквивалентно ошибке " **\_ \_ CN \_ без \_ сопоставления" сертификата E** ).</span><span class="sxs-lookup"><span data-stu-id="7b77b-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**Ошибка \_ \_ \_ \_ Недопустимая дата безопасного сертификата WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-227">12037</span><span class="sxs-lookup"><span data-stu-id="7b77b-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-228">Указывает, что требуемый сертификат не находится в течение срока действия при проверке по текущему системному времени или отметке времени в подписанном файле, а также в том, что срок действия цепочки сертификатов не вкладывается правильно (аналогично **сертификату \_ электронной почты с \_ истекшим** периодом действия или валидитипериоднестинг ошибке **CERT \_ e \_** ).</span><span class="sxs-lookup"><span data-stu-id="7b77b-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**Ошибка \_ \_ \_ \_ \_ при попытке установить безопасный сертификат WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-230">12057</span><span class="sxs-lookup"><span data-stu-id="7b77b-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-231">Указывает, что отзыв не может быть проверен, так как сервер отзыва был отключен (что эквивалентно **шифрованию \_ \_ отзыва \_ E**).</span><span class="sxs-lookup"><span data-stu-id="7b77b-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**Ошибка \_ при \_ \_ отзыве безопасного сертификата WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-233">12170</span><span class="sxs-lookup"><span data-stu-id="7b77b-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-234">Указывает, что сертификат был отозван (эквивалентно **шифрованию \_ E \_ REVOKE**).</span><span class="sxs-lookup"><span data-stu-id="7b77b-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**Ошибка \_ при \_ \_ \_ неправильном \_ использовании безопасного сертификата WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-236">12179</span><span class="sxs-lookup"><span data-stu-id="7b77b-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-237">Указывает, что сертификат недействителен для запрошенного использования (аналогично **\_ \_ неправильному \_ использованию CERT E**).</span><span class="sxs-lookup"><span data-stu-id="7b77b-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**Ошибка \_ при \_ \_ ошибке безопасного канала WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-239">12157</span><span class="sxs-lookup"><span data-stu-id="7b77b-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-240">Указывает, что при возникновении ошибки в защищенном канале (эквиваленты кодам ошибок, которые начинаются с "с \_ E \_ " и "сек \_ I", \_ перечисленные в файле заголовка Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="7b77b-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**Ошибка \_ \_ безопасного \_ сбоя WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-242">12175</span><span class="sxs-lookup"><span data-stu-id="7b77b-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-243">В сертификате SSL (SSL), отправленном сервером, обнаружена одна или несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="7b77b-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="7b77b-244">Чтобы определить тип обнаруженной ошибки, проверьте [**\_ состояние обратного вызова WinHTTP на \_ \_ \_**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) наличие уведомления о сбое в функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="7b77b-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="7b77b-245">Дополнительные сведения см. в [**разделе \_ \_ обратный вызов состояния WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="7b77b-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**Ошибка \_ WinHTTP \_ безопасный \_ Недопустимый \_ ЦС**</span><span class="sxs-lookup"><span data-stu-id="7b77b-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-247">12045</span><span class="sxs-lookup"><span data-stu-id="7b77b-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-248">Указывает, что цепочка сертификатов была обработана, но была прервана в корневом сертификате, который не является доверенным для поставщика доверия (эквивалентно **CERT \_ E \_ унтрустедрут**).</span><span class="sxs-lookup"><span data-stu-id="7b77b-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**Ошибка \_ WinHTTP \_ безопасный \_ Недопустимый \_ сертификат**</span><span class="sxs-lookup"><span data-stu-id="7b77b-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-250">12169</span><span class="sxs-lookup"><span data-stu-id="7b77b-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-251">Указывает, что сертификат является недопустимым (аналогично таким ошибкам, как **\_ \_ роль CERT e**, **CERT \_ e \_ пасленконст**, **CERT \_ e \_ Critical**, **CERT \_ e \_**, **CERT \_ e \_ иссуерчаининг**, **CERT \_ e \_ неправильный формат** и **\_ \_ цепочка сертификатов e**).</span><span class="sxs-lookup"><span data-stu-id="7b77b-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**Ошибка \_ при \_ завершении работы WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-253">12012</span><span class="sxs-lookup"><span data-stu-id="7b77b-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-254">Поддержка функции WinHTTP завершается или выгружается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**Ошибка \_ при \_ истечении времени ожидания WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="7b77b-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-256">12002</span><span class="sxs-lookup"><span data-stu-id="7b77b-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-257">Истекло время ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="7b77b-257">The request has timed out.</span></span>

<span data-ttu-id="7b77b-258">Эта ошибка может быть возвращена в результате истечения времени ожидания TCP/IP, независимо от значений времени ожидания, заданных в службах HTTP Windows.</span><span class="sxs-lookup"><span data-stu-id="7b77b-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**Ошибка \_ WinHTTP \_ не \_ удалось \_ скачать \_ Скрипт**</span><span class="sxs-lookup"><span data-stu-id="7b77b-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-260">12167</span><span class="sxs-lookup"><span data-stu-id="7b77b-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-261">Не удается скачать файл PAC.</span><span class="sxs-lookup"><span data-stu-id="7b77b-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="7b77b-262">Например, сервер, на который ссылается URL-адрес PAC, может быть недоступен, или сервер вернул ответ 404 не найден.</span><span class="sxs-lookup"><span data-stu-id="7b77b-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**Ошибка \_ \_ необработанного \_ типа скрипта WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="7b77b-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-264">12176</span><span class="sxs-lookup"><span data-stu-id="7b77b-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-265">Тип скрипта не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b77b-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**Ошибка \_ WinHTTP \_ Нераспознанная \_ схема**</span><span class="sxs-lookup"><span data-stu-id="7b77b-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b77b-267">12006</span><span class="sxs-lookup"><span data-stu-id="7b77b-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="7b77b-268">В URL-адресе указана схема, отличная от "http:" или "https:".</span><span class="sxs-lookup"><span data-stu-id="7b77b-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Ошибка \_ не \_ хватает \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="7b77b-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-270">Недостаточно памяти для завершения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="7b77b-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="7b77b-271">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="7b77b-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-273">Размер (в байтах) буфера, предоставленного функции, недостаточно для того, чтобы он содержал возвращенные данные.</span><span class="sxs-lookup"><span data-stu-id="7b77b-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="7b77b-274">Дополнительные сведения см. в разделе конкретная функция.</span><span class="sxs-lookup"><span data-stu-id="7b77b-274">For more information, see the specific function.</span></span>

<span data-ttu-id="7b77b-275">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Ошибка \_ недопустимого \_ маркера**</span><span class="sxs-lookup"><span data-stu-id="7b77b-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-277">Маркер, переданный в интерфейс прикладного программирования (API), был либо недействительным, либо закрытым.</span><span class="sxs-lookup"><span data-stu-id="7b77b-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="7b77b-278">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Ошибка \_ больше \_ нет \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="7b77b-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-280">Больше файлов не найдено.</span><span class="sxs-lookup"><span data-stu-id="7b77b-280">No more files have been found.</span></span>

<span data-ttu-id="7b77b-281">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Ошибка \_ больше \_ нет \_ элементов**</span><span class="sxs-lookup"><span data-stu-id="7b77b-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-283">Больше элементов не найдено.</span><span class="sxs-lookup"><span data-stu-id="7b77b-283">No more items have been found.</span></span>

<span data-ttu-id="7b77b-284">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7b77b-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Ошибка \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="7b77b-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7b77b-286">Необходимый стек протокола не загружен, и приложение не может запустить WinSock.</span><span class="sxs-lookup"><span data-stu-id="7b77b-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="7b77b-287">**Заголовок:** Объявлено в файле Winerror. h</span><span class="sxs-lookup"><span data-stu-id="7b77b-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b77b-288">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b77b-288">Remarks</span></span>

<span data-ttu-id="7b77b-289">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7b77b-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b77b-290">Требования</span><span class="sxs-lookup"><span data-stu-id="7b77b-290">Requirements</span></span>



| <span data-ttu-id="7b77b-291">Требование</span><span class="sxs-lookup"><span data-stu-id="7b77b-291">Requirement</span></span> | <span data-ttu-id="7b77b-292">Значение</span><span class="sxs-lookup"><span data-stu-id="7b77b-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b77b-293">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b77b-293">Minimum supported client</span></span><br/> | <span data-ttu-id="7b77b-294">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b77b-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7b77b-295">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b77b-295">Minimum supported server</span></span><br/> | <span data-ttu-id="7b77b-296">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b77b-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7b77b-297">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7b77b-297">Redistributable</span></span><br/>          | <span data-ttu-id="7b77b-298">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7b77b-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7b77b-299">Header</span><span class="sxs-lookup"><span data-stu-id="7b77b-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b77b-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b77b-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7b77b-301">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b77b-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b77b-302">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7b77b-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

