---
description: В этом разделе определяются структуры, используемые WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Структуры WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174984"
---
# <a name="winhttp-structures"></a>Структуры WinHTTP

WinHTTP использует следующие структуры:

<dl> <dt>

[**HTTP_VERSION_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

Содержит глобальную версию HTTP.

</dd> <dt>

[**URL_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

Содержит составные части URL-адреса. Эта структура используется с функциями [**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) и [**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .

</dd> <dt>

[**WINHTTP_ASYNC_RESULT**](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

Содержит результат вызова асинхронной функции. Эта структура используется с прототипом [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .

</dd> <dt>

[**WINHTTP_AUTOPROXY_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

Используется для указания функции [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , следует ли указывать URL-адрес файла автоматической настройки прокси-сервера (PAC) или автоматически размещать URL-адреса с запросами DHCP или DNS к сети.

</dd> <dt>

[**WINHTTP_CERTIFICATE_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

Содержит сведения о сертификате, возвращенные с сервера. Эта структура используется функцией [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) .

</dd> <dt>

[**WINHTTP_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

Представляет группу соединений.

</dd> <dt>

[**WINHTTP_CONNECTION_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

Содержит исходный и конечный IP-адрес запроса, создавшего ответ.

</dd> <dt>

[**WINHTTP_CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.

> [!Note]
> Эта структура устарела. Вместо этого рекомендуется использовать структуру [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) .

</dd> <dt>

[**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

Содержит учетные данные пользователя, используемые для проверки подлинности сервера и прокси.

</dd> <dt>

[**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

Содержит сведения о конфигурации прокси-сервера Internet Explorer.

</dd> <dt>

[**WINHTTP_EXTENDED_HEADER**](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

Представляет заголовок HTTP-запроса в виде пары "имя-значение".

</dd> <dt>

[**WINHTTP_HEADER_NAME**](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

Представляет имя заголовка HTTP-запроса.

</dd> <dt>

[**WINHTTP_HOST_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

Представляет коллекцию групп соединений.

</dd> <dt>

[**WINHTTP_MATCH_CONNECTION_GUID**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

Представляет идентификатор GUID соединения в целях сопоставления соединений.

</dd> <dt>

[**WINHTTP_PROXY_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

Содержит конфигурацию сеанса или прокси-сервера по умолчанию.

</dd> <dt>

[**WINHTTP_PROXY_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

Коллекция записей результатов прокси-сервера, предоставляемых [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).

</dd> <dt>

[**WINHTTP_PROXY_RESULT_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

Результирующая запись из вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).

</dd> <dt>

[**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

Представляет описание текущего состояния соединений WinHttp.

</dd> <dt>

[**WINHTTP_REQUEST_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

Содержит статистику для запроса.

</dd> <dt>

[**WINHTTP_REQUEST_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

Содержит сведения о времени для запроса.

</dd> <dt>

[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

Содержит подключение SChannel и сведения о шифровании для запроса.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_ASYNC_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

Состояние результата операции WebSocket.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_STATUS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

Состояние операции WebSocket.

</dd> </dl>
