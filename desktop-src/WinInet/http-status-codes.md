---
title: Коды состояния HTTP (WinInet. h)
description: В следующей таблице содержатся константы и соответствующие значения для кодов состояния HTTP, возвращаемых серверами в Интернете.
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c6a8fecf7d1c7b3f95c1d4ce8040b9ba25e7d72ee4a41c8cbbcd24cd0da4bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743812"
---
# <a name="http-status-codes-winineth"></a>Коды состояния HTTP (WinInet. h)

В следующей таблице содержатся константы и соответствующие значения для кодов состояния HTTP, возвращаемых серверами в Интернете.

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**\_продолжение состояния \_ http**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Запрос можно продолжить.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**\_ \_ протоколы переключения состояния HTTP \_**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Сервер переключил протоколы в заголовке обновления.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**состояние HTTP " \_ \_ ОК"**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



Запрос успешно выполнен.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**\_состояние HTTP \_ создано**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



Запрос был выполнен и привел к созданию нового ресурса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**\_состояние HTTP \_ принято**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



Запрос принят на обработку, но обработка не завершена.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**\_ \_ частичное состояние HTTP**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



Возвращенные метаданные в заголовке сущности не являются определяющим набором, доступным на сервере-источнике.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**\_состояние HTTP \_ без \_ содержимого**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



Сервер выполнил запрос, но нет новых данных для отправки обратно.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**\_ \_ содержимое сброса состояния \_ http**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



Запрос завершен, и клиентская программа должна сбросить представление документа, вызвавшее отправку запроса, чтобы позволить пользователю легко инициировать другое Входное действие.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**\_ \_ частичное содержимое состояния HTTP \_**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



Сервер выполнил частичный запрос GET для ресурса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**\_неоднозначное состояние HTTP \_**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



Серверу не удалось определить возвращаемые значения.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**\_состояние HTTP \_ перемещено**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



Запрошенному ресурсу был назначен новый постоянный универсальный код ресурса (URI), и все будущие ссылки на этот ресурс следует выполнять с помощью одного из возвращенных URI.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**\_Перенаправление состояния HTTP \_**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



Запрошенный ресурс временно находится под другим URI (универсальный идентификатор ресурса).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**\_ \_ метод ПЕРЕНАПРАВЛЕНИЯ HTTP-состояния \_**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



Ответ на запрос можно найти по другому универсальному коду ресурса (URI), и его следует получить с помощью команды GET HTTP для этого ресурса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_состояние HTTP \_ не \_ изменено**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



Запрошенный ресурс не был изменен.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**\_ \_ использование \_ прокси-сервера состояния HTTP**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



Доступ к запрошенному ресурсу должен осуществляться через прокси-сервер, заданный в поле Location.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**\_команда сохранения состояния HTTP- \_ перенаправления \_ \_**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



Перенаправленный запрос сохраняет ту же команду HTTP. Поведение HTTP/1.1.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**\_ \_ неправильный запрос состояния \_ http**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



Серверу не удалось обработать запрос из-за недопустимого синтаксиса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**состояние HTTP " \_ \_ отклонено"**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



Запрошенный ресурс требует проверки подлинности пользователя.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**\_ \_ Заявка на оплату состояния HTTP \_**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



В настоящее время не реализовано в протоколе HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**\_состояние HTTP \_ запрещено**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



Сервер понял запрос, но отказывается его выполнить.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_состояние HTTP \_ не \_ Найдено**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



Сервер не нашел ничего, соответствующего запрошенному URI (универсальный идентификатор ресурса).


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**\_ \_ неправильный метод состояния \_ http**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



Используемая команда HTTP не разрешена.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**состояние HTTP " \_ \_ нет \_ допустимого"**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



Не найдены ответы, приемлемые для клиента.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**\_состояние HTTP \_ \_ Проверка подлинности прокси \_**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



Требуется проверка подлинности прокси-сервера.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**\_ \_ время ожидания запроса состояния HTTP \_**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



Истекло время ожидания запроса сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**\_конфликт состояния \_ http**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



Не удалось выполнить запрос из-за конфликта с текущим состоянием ресурса. Пользователю следует повторить отправку с дополнительными сведениями.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**\_состояние HTTP \_ пропала**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



Запрошенный ресурс больше не доступен на сервере, и адрес пересылки неизвестен.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_ \_ требуется длина состояния \_ http**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



Сервер отказывается принимать запрос без определенной длины содержимого.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**\_Ошибка HTTP Status \_ преконд \_**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



Предусловие, заданное в одном или нескольких полях заголовка запроса, выдает значение false при проверке на сервере.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**\_ \_ \_ слишком \_ большой запрос состояния HTTP**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



Сервер отказывается обработать запрос, так как сущность запроса больше, чем сервер готов или может обработать.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**\_ \_ \_ слишком \_ длинный URI состояния HTTP**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



Сервер отказывается обслуживать запрос, так как URI запроса (универсальный идентификатор ресурса) длиннее, чем сервер может интерпретироваться.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**\_ \_ неподдерживаемый носитель состояния \_ http**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



Сервер отказывается обслуживать запрос, так как сущность запроса имеет формат, не поддерживаемый запрошенным ресурсом для запрошенного метода.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**\_Повтор состояния HTTP \_ \_ с**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



После выполнения соответствующего действия запрос должен быть выполнен повторно.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**\_ \_ Ошибка сервера состояния \_ http**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



Сервер обнаружил непредвиденное условие, препятствующее выполнению запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_состояние HTTP \_ не \_ поддерживается**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



Сервер не поддерживает функции, необходимые для выполнения запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**\_ \_ неправильный шлюз состояния \_ http**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



Сервер, выполняющий роль шлюза или прокси-сервера, получил недопустимый ответ от вышестоящего сервера, к которому он обращался при попытке выполнения запроса.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**недоступный для \_ службы состояния HTTP \_ \_**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



Служба временно перегружена.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**\_ \_ время ожидания шлюза состояния HTTP \_**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



При выполнении запроса было превышено время ожидания шлюза.


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**\_версия состояния \_ HTTP \_ не \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



Сервер не поддерживает или отказывается поддерживать версию протокола HTTP, которая использовалась в сообщении запроса.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

