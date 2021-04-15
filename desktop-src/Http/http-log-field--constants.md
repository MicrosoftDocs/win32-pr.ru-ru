---
title: Константы HTTP_LOG_FIELD_ (HTTP. h)
description: Определите поля в журнале W3C и в журналах ошибок.
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661866"
---
# <a name="http_log_field_-constants"></a>\_ \_ Константы поля журнала HTTP \_

Константы **\_ \_ поля \_ журнала HTTP** определяют поля в журнале W3C и в журналах ошибок.

Эти константы используются в структуре [**\_ \_ сведений о ведении журнала HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**\_ \_ Дата поля журнала \_ http**
</dt> <dd> <dl> <dt>



Дата, когда произошло действие.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**\_время для \_ поля \_ журнала HTTP**
</dt> <dd> <dl> <dt>



Время, в течение которого произошло действие, в формате UTC.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**\_ \_ \_ \_ IP-адрес клиента для поля журнала HTTP**
</dt> <dd> <dl> <dt>



IP-адрес отправившего запрос клиента.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**\_ \_ имя пользователя для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Имя пользователя, прошедшего проверку подлинности, который получил доступ к серверу. Анонимные пользователи обозначаются дефисом.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**\_ \_ имя сайта для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Имя сайта, на котором была создана запись файла журнала.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**Протокол HTTP \_ \_ \_ \_ имя компьютера для поля журнала**
</dt> <dd> <dl> <dt>



Имя компьютера, на котором была создана запись файла журнала.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**\_ \_ \_ \_ IP-адрес сервера для поля журнала HTTP**
</dt> <dd> <dl> <dt>



IP-адрес сервера, на котором была создана запись файла журнала.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**\_ \_ метод поля журнала \_ http**
</dt> <dd> <dl> <dt>



Запрошенное действие, например метод Get.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**Протокол HTTP \_ \_ \_ \_ ресурс URI поля журнала**
</dt> <dd> <dl> <dt>



Целевой объект действия, например Default.htm.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**\_ \_ запрос URI для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Запрос, если таковой имеется, который клиент пытался выполнить. Запрос универсального кода ресурса (URI) требуется только для динамических страниц.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**\_ \_ состояние поля журнала \_ http**
</dt> <dd> <dl> <dt>



Код состояния HTTP.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**\_Поле журнала \_ HTTP \_ \_ состояние Win32**
</dt> <dd> <dl> <dt>



Код состояния Windows.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**\_ \_ \_ Отправлено байт для поля журнала \_ http**
</dt> <dd> <dl> <dt>



Число в байтах, отправленное сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**\_байтов для \_ поля журнала HTTP \_ \_ recv**
</dt> <dd> <dl> <dt>



Число в байтах, полученное сервером.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**\_ \_ \_ затраченное время для поля журнала \_ http**
</dt> <dd> <dl> <dt>



Время (в миллисекундах) действия.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**\_ \_ \_ порт сервера полей журнала \_ http**
</dt> <dd> <dl> <dt>



Номер порта сервера, настроенного для службы.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**Протокол HTTP \_ \_ \_ \_ Агент пользователя поля журнала**
</dt> <dd> <dl> <dt>



Приложение, используемое клиентом.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**\_ \_ файл cookie поля журнала HTTP \_**
</dt> <dd> <dl> <dt>



Содержимое отправленного или полученного файла cookie, если таковое имеется.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**\_ \_ ссылка на поле журнала HTTP \_**
</dt> <dd> <dl> <dt>



Сайт, который последний раз посещал пользователь. Этот сайт предоставил ссылку на текущий сайт.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**\_ \_ версия поля журнала \_ http**
</dt> <dd> <dl> <dt>



Версия протокола HTTP, используемая клиентом.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**\_ \_ узел поля журнала \_ http**
</dt> <dd> <dl> <dt>



Имя заголовка узла, если оно есть.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**\_подсостояние \_ поля \_ журнала \_ http**
</dt> <dd> <dl> <dt>



Код ошибки подсостояния.


</dt> </dl> </dd> </dl>

Для ведения журнала ошибок HTTP используются следующие константы.

<dl> <dt>

<span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**\_ \_ порт клиента для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Номер порта клиента, с которого получен запрос. Это поле журнала используется только для ведения журнала ошибок.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**\_ \_ URI поля журнала \_ http**
</dt> <dd> <dl> <dt>



URI, полученный в запросе, включая часть запроса. Это поле журнала используется только для ведения журнала ошибок.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**\_ \_ идентификатор сайта для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Зависящий от приложения числовой идентификатор группы URL-адресов, в которой направляется запрос. Это поле журнала используется только для ведения журнала ошибок.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**\_Причина для \_ поля \_ журнала HTTP**
</dt> <dd> <dl> <dt>



Причина ошибки. Это поле журнала используется только для ведения журнала ошибок.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**\_ \_ имя очереди для поля журнала \_ HTTP \_**
</dt> <dd> <dl> <dt>



Имя очереди запросов, в которую отправляется запрос. Это поле журнала используется только для ведения журнала ошибок.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**\_ \_ STREAMID поля журнала \_ http**
</dt> <dd> <dl> <dt>



Идентификатор потока.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                              |
| Header<br/>                   | <dl> <dt>HTTP. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы API сервера HTTP версии 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_сведения о ведении журнала HTTP \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**хттпсетурлграуппроперти**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**хттпсетсерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**хттпкуерюрлграуппроперти**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**хттпкуерисерверсессионпроперти**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





