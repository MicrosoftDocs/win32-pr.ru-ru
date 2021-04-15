---
description: Начиная с Windows Server 2008 и Windows Vista, API WinHTTP был усовершенствован для включения следующих функций.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Новые возможности Windows Server 2008 и Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497499"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Новые возможности Windows Server 2008 и Windows Vista

Начиная с Windows Server 2008 и Windows Vista, API WinHTTP был усовершенствован для включения следующих функций.

## <a name="greater-than-4-gb-upload"></a>Отправка превышает 4 ГБ.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) может передавать только 4 ГБ данных из-за ограничений в значении параметра общей длины DWORD. Чтобы позволить приложениям передавать более 4 ГБ данных, в запрос добавляется заголовок Content-Length, указывающий данные в виде большого \_ целого числа (2 ^ 64 байта). Дополнительные сведения см. в разделе **WinHttpSendRequest**. Эта функция не поддерживается в COM-объекте [**ивинхттпрекуест**](iwinhttprequest-interface.md) .

## <a name="transfer-encoding-header"></a>Заголовок Transfer-Encoding

Заголовок Transfer-Encoding позволяет приложениям передавать фрагментированные данные на сервер. Если в запросе имеется заголовок Transfer-Encoding, приложение отправляет запрос с телом сущности нулевой длины в вызове [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Тело сущности отправляется в последующих вызовах [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Эта функция не поддерживается в COM-объекте [**ивинхттпрекуест**](iwinhttprequest-interface.md) .

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Получение списка издателей SSL-сертификатов клиентов

Приложение может получить список издателей сертификата клиента SSL, когда [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) завершается с **ошибкой \_ , \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**. Новый параметр, **\_ \_ \_ \_ \_ список издателей сертификатов клиента**, позволяет приложениям получать список издателей сертификатов и фильтровать список для оптимального сертификата. Дополнительные сведения см. в разделах [**Параметры**](option-flags.md) и [Получение списка поставщиков для проверки подлинности клиента SSL](ssl-in-winhttp.md) . Эта функция не поддерживается в COM-объекте [**ивинхттпрекуест**](iwinhttprequest-interface.md) .

## <a name="optional-client-certificates"></a>Необязательные сертификаты клиента

Когда [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) завершается с **ошибкой \_ , \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**, сервер может не требовать SSL-сертификата клиента. Сервер может иметь возможность вернуться к другой форме проверки подлинности или разрешить клиенту продолжать анонимный доступ. Приложение задает параметр " **\_ \_ \_ \_ контекст сертификата клиента" для параметра WinHTTP** и указывает макрос, используемый WinHTTP для определения необходимости в сертификате клиента. Дополнительные сведения см. в разделе [**флаги параметров**](option-flags.md). Эта функция не поддерживается в COM-объекте [**ивинхттпрекуест**](iwinhttprequest-interface.md) .

## <a name="source-and-destination-ip-addresses"></a>Исходный и конечный IP-адреса

После завершения [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) приложение может получить исходный и конечный IP-адрес и порт запроса, создавшего ответ. Доступна новая структура для получения адресов источника и назначения, если установлен параметр **\_ \_ \_ сведения о соединении с параметром WinHTTP** . Дополнительные сведения см. в разделе [**флаги параметров**](option-flags.md). Эта функция не поддерживается в COM-объекте [**ивинхттпрекуест**](iwinhttprequest-interface.md) .

## <a name="additional-ssl-client-authentication-errors"></a>Дополнительные ошибки проверки подлинности клиента SSL

Дополнительные сведения об ошибках проверки подлинности клиента SSL см. в этой статье. **Ошибка при \_ Сертификат \_ клиента \_ WinHTTP \_ без \_ закрытого \_ ключа** и **Ошибка \_ WinHTTP сертификат \_ \_ без доступа к сертификату клиента \_ \_ закрытый \_ ключ** — это новая ошибка для Windows Server 2008 и Windows Vista. COM-объект [**ивинхттпрекуест**](iwinhttprequest-interface.md) возвращает эти ошибки в HRESULT.

 

 



