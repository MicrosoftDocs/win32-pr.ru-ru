---
Description: В Винхттпкуерйоптион и Винхттпсетоптион поддерживаются следующие флаги параметров.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Флаги параметров (WinHTTP. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9ca6b7c74d484a6bcac235b2396b2005c8c3260
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386683"
---
# <a name="option-flags"></a>Флаги параметров

В [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)поддерживаются следующие флаги параметров.

<dl> <dt>

<span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**\_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы**
</dt> <dd> <dl> <dt>



Значение по умолчанию — FALSE. Если задано значение TRUE, служба WinHTTP не гарантирует ход выполнения, если клиентское приложение блокирует обратные вызовы состояния.

Клиентское приложение должно соблюдать особое внимание для выполнения минимальных операций в обратном вызове без блокировки, возврата как можно быстрее, а в частности не должен ждать последующего вызова WinHTTP. Если это не соответствует этим рекомендациям, вероятно, это отрицательное воздействие на производительность или зависание приложения. Если используется заранее, этот параметр может повысить производительность.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**\_ \_ политика автоматического входа в службу WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает длинное целочисленное значение без знака, определяющее [политику автоматического входа в систему](authentication-in-winhttp.md) с одним из следующих значений.

| Термин | Описание |
|-|-|
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>\_ \_ \_ высокий уровень безопасности автоматического входа \_ WinHTTP | Учетные данные по умолчанию не используются. Обратите внимание, что этот флаг вступает в силу только в том случае, если сервер задается фактическим именем компьютера. Он не вступит в силу, если сервер указывается как localhost или IP-адрес. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>\_ \_ \_ низкий уровень безопасности автоматического входа \_ WinHTTP | Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется для всех запросов. |
| <span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>\_уровень безопасности автоматического входа WinHTTP — \_ \_ \_ средний | Вход с проверкой подлинности с использованием учетных данных по умолчанию выполняется только для запросов в локальной интрасети. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**\_ \_ обратный вызов параметра WinHTTP**
</dt> <dd> <dl> <dt>



Получает указатель на функцию обратного вызова, заданную с помощью [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**\_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает контекст сертификата клиента. Если приложение получает [**сообщение об ошибке " \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md)", он должен вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для предоставления сертификата, прежде чем повторять запрос. В ходе обработки этого параметра служба WinHttp вызывает [**цертдупликатецертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) в контексте сертификата, предоставленного вызывающим объектом, чтобы контекст сертификата можно было независимо освободить от вызывающего.

> [!Note]
> Приложению не следует попытаться закрыть хранилище сертификатов с помощью \_ флага "Close" ( \_ \_ Сбросить флаг принудительного восстановления сертификата) \_ в вызове [**цертклосесторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) в хранилище сертификатов, из которого был получен контекст сертификата. Может произойти нарушение прав доступа.

Когда сервер запрашивает сертификат клиента, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) возвращает [**ошибку, \_ \_ \_ \_ \_ требуется сертификат проверки подлинности клиента WinHTTP**](error-messages.md) . Если сервер запрашивает сертификат, но не требует его, приложение может указать этот параметр, чтобы указать, что у него нет сертификата. Сервер может выбрать другую схему проверки подлинности или разрешить анонимный доступ к серверу. Приложение предоставляет **\_ \_ \_ \_ Контекстный макрос WinHTTP No Client** Certificate в параметре *лпбуффер* объекта [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , как показано в следующем примере кода.

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

Если серверу требуется сертификат клиента, он может отправить код состояния HTTP 403 в ответе. Дополнительные сведения см. в описании параметра **WinHTTP Certificate \_ \_ Client \_ CERT \_ Issuer \_** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**\_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает структуру [**\_ иссуерлистинфоекс секпкгконтекст**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , когда ошибка из [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) или [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) является **ошибкой \_ \_ \_ сертификата проверки подлинности \_ \_ клиента WinHTTP**. Список издателей в структуре содержит список приемлемых центров сертификации (ЦС) с сервера. Клиентское приложение может отфильтровать список центров сертификации, чтобы получить сертификат клиента для проверки подлинности SSL.

Кроме того, если сервер запрашивает сертификат клиента, но не требует его, приложение может вызвать [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) с параметром **\_ контекста WinHTTP параметр \_ \_ сертификата \_ клиента** . Дополнительные сведения см. в описании параметра службы **WinHTTP \_ параметр \_ \_ \_ контекста сертификата клиента** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**\_ \_ кодовая страница параметра WinHTTP**
</dt> <dd> <dl> <dt>



Задает [*кодовую страницу*](glossary.md) , используемую для обработки URL-адреса (то есть строки запроса). По умолчанию используется значение UTF8.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**\_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта**
</dt> <dd> <dl> <dt>



Задает длинное целое число без знака, указывающее, включена ли [Проверка подлинности Passport при](passport-authentication-in-winhttp.md) проверке подлинности WinHTTP. Он может иметь одно из следующих значений:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>\_Служба WinHTTP отключает проверку \_ \_ подлинности Passport | Microsoft Passport проверка подлинности отключена. Это значение по умолчанию. |
| <span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ отключение \_ набора \_ ключей паспорта | Набор ключей паспорта отключен. Это значение по умолчанию. |
| <span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>\_Служба WinHTTP включает проверку \_ \_ подлинности паспорта | Проверка подлинности паспорта включена. |
| <span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>\_Служба WinHTTP включает набор \_ \_ ключей Passport | Набор ключей паспорта включен. |

</dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**\_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, которое содержит число попыток подключения к узлу Тимесвинхттп. Службы Microsoft Windows HTTP (WinHTTP) пытаются попытаться только один раз на IP-адрес. Например, при попытке подключиться к многосетевому узлу, имеющему 10 IP-адресов, а **\_ параметру WinHTTP \_ \_ попыток подключения** будет присвоено значение 7, служба WinHTTP попытается подключиться только к первым семи IP-адресам. Если один набор из 10 IP-адресов установлен в значение 20, то служба WinHTTP попытается выполнить каждую из 10 только один раз. **\_ \_ \_** Если попытка соединения по-прежнему завершается неудачей после указанного числа попыток или если время ожидания соединения истекло раньше, запрос отменяется. Значение по умолчанию **для \_ параметра \_ \_ WinHTTP** — пять попыток.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**\_ \_ время ожидания соединения для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее значение времени ожидания в миллисекундах. Если установить для этого параметра значение Infinite (0xFFFFFFFF), этот таймер будет отключен.

Если запрос на TCP-соединение длится дольше этого значения времени ожидания, запрос отменяется. Время ожидания по умолчанию — 60 секунд. При попытке подключения к нескольким IP-адресам для одного узла (многосетевой узел) для каждого отдельного соединения устанавливается ограничение времени ожидания.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**\_ \_ сведения о соединении параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает исходный и конечный IP-адрес и порт запроса, который создал ответ при возвращении [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . Приложение вызывает [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) с параметром **WinHTTP \_ \_ \_ сведения о соединении** и предоставляет структуру [**\_ \_ сведений о соединении WinHTTP**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) в параметре *лпбуффер* . Дополнительные сведения см. в **разделе \_ \_ сведения о подключении к WinHTTP**.

**Windows Server 2003 с пакетом обновления SP1 и Windows XP с пакетом обновления 2 (SP2):** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v0**
</dt> <dd> <dl> <dt>



Извлекает структуру [**TCP \_ info \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) для базового соединения, используемого запросом. Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.

> [!Note]
> Этот параметр был заменен **\_ параметром WinHTTP \_ Connection \_ stats \_ v1**.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**\_Параметр WinHTTP \_ Connection \_ stats \_ v1**
</dt> <dd> <dl> <dt>



Извлекает структуру [**TCP \_ \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) для базового соединения, используемого запросом. Возвращаемая структура может содержать статистику предыдущих запросов, отправленных по тому же соединению.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**\_ \_ значение контекста WinHTTP для параметра \_**
</dt> <dd> <dl> <dt>



Задает или получает **двойное слово \_ типа DWORD** , содержащее указатель на значение контекста, связанное с этим [хинтернет](hinternet-handles-in-winhttp.md) -обработчиком. Используется значение, хранящееся в буфере, а для флага Option **\_ \_ \_ значения контекста WinHTTP** задано новое значение.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**\_ \_ распаковка параметров WinHTTP**
</dt> <dd> <dl> <dt>



Задает параметр DWORD флагов, который определяет, будет ли WinHTTP автоматически распаковывать текст ответа с сжатыми кодировками содержимого. WinHTTP также установит соответствующий заголовок Accept-Encoding, переопределив все, предоставленные вызывающим объектом. Поддерживаются значения:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>\_флаг распаковки \_ WinHTTP \_ | Распаковка содержимого в кодировке: отклики gzip. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>\_ДЕуплотнение \_ ФЛАГа РАСПАКОВКи WinHTTP \_ | Распаковка содержимого в кодировке: разворачивает ответы. |
| <span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>\_ \_ все ФЛАГи РАСПАКОВКи WinHTTP \_ | Распаковка ответов с любой поддерживаемой кодировкой содержимого. |

По умолчанию WinHTTP будет доставлять сжатые ответы вызывающему объекту без изменений.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**\_ \_ функция отключения параметров \_ WinHTTP**
</dt> <dd> <dl> <dt>



Задает длинное целочисленное значение без знака, указывающее, какие функции отключены с помощью одного или нескольких из следующих флагов. Имейте в виду, что эта функция должна передаваться только в [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) в дескрипторах запросов после создания дескриптора запроса с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)и перед отправкой запроса с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

| Термин | Описание |
|-|-|
| <span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ отключение \_ проверки подлинности | Автоматическая проверка подлинности отключена. |
| <span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ отключение \_ файлов cookie | Автоматическое добавление заголовков файлов cookie в запросы отключено. Кроме того, возвращенные файлы cookie не добавляются автоматически в базу данных cookie. Отключение файлов cookie может привести к низкой производительности проверки подлинности Passport. |
| <span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>\_отключение \_ поддержания \_ активности WinHTTP | Отключает семантику поддержания активности для соединения. Семантика проверки активности требуется для MSN, NTLM и других типов аутентификации. |
| <span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>\_отключение \_ ПЕРЕнаправлений WinHTTP | Автоматическое перенаправление отключено при отправке запросов с помощью [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Если автоматическое перенаправление отключено, приложение должно зарегистрировать функцию обратного вызова, чтобы обеспечить успешную проверку подлинности Passport. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**\_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_**
</dt> <dd> <dl> <dt>



Предотвращает повторное выполнение службой WinHTTP соединения с более ранней версией протокола безопасности при сбое согласования первоначального протокола.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**\_параметр WinHTTP \_ Отключить \_ \_ очередь потока**
</dt> <dd> <dl> <dt>



Позволяет новым запросам открывать дополнительное соединение HTTP/2 при достижении максимального количества одновременных потоков, а не ждать следующего доступного потока в существующем соединении.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**\_ \_ Включение \_ функции WinHTTP**
</dt> <dd> <dl> <dt>



Задает длинное целое число без знака, определяющее включенные в данный момент функции. Может принимать одно из следующих значений.

| Термин | Описание |
|-|-|
| <span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ Включение \_ \_ олицетворения при отмене SSL \_ | Если параметр включен, WinHTTP временно восстанавливает олицетворение клиента на время выполнения операций аутентификации SSL-сертификата. Это значение может быть задано только в обработчике сеанса. |
| <span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ Включение \_ \_ отзыва SSL | Если этот режим включен, WinHTTP разрешает отзыв SSL. Это значение можно задать только в обработчике запроса. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**\_параметр WinHTTP \_ Включение \_ \_ протокола HTTP**
</dt> <dd> <dl> <dt>



Задает битовую маску DWORD допустимых расширенных версий HTTP. Возможны следующие значения:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>\_Флаг протокола \_ WinHTTP \_ HTTP2 (0x1) | Включает HTTP/2 для запроса. |
| Нет (0x0) | Разрешает запрос в формате HTTP/1.1 и более ранних версиях. |

Устаревшие версии протокола HTTP (1,1 и более ранних версий) нельзя отключить с помощью этого параметра. Значение по умолчанию — 0x0.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**\_параметр WinHTTP \_ енаблетраЦинг**
</dt> <dd> <dl> <dt>



Задает **логическое** значение, указывающее, включена ли трассировка в данный момент. Дополнительные сведения о средстве трассировки в WinHTTP см. в разделе [средство трассировки WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md). Этот параметр можно задать только для **нулевого** маркера **хинтернет** .


</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**\_ \_ добавочная кодировка параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Включает кодировку URL в процентах для пути и строки запроса.

Кроме того, можно закодировать процент перед вызовом WinHttp.

</dt> </dl> </dd>

<dt>

<span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**\_ \_ срок действия соединения для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Этот параметр может быть установлен только для того обработчика запроса, который все еще активен (отправка или получение). Установка этого параметра сообщит службе WinHttp о необходимости прекращать обслуживание запросов в соединении, связанном с переданным маркером запроса. Соединение будет закрыто после того, как обработчик запроса вызывает этот параметр с завершенным. Этот параметр не принимает никаких параметров.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**\_ \_ Расширенная ошибка при выборе WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает длинное целое число без знака, содержащее код ошибки сокетов Microsoft Windows, сопоставленный с ошибкой сообщения WinHTTP, которые были \_ \_ \* возвращены в данном контексте потока. В качестве значения Handle можно передать значение **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**. Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**. Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**. Этот раздел реестра отсутствует по умолчанию. Когда она задана, WinINet отправит учетные данные на WinHTTP. Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet. Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_**
</dt> <dd> <dl> <dt>



Принимает указатель на структуру с указанием учетных данных [**\_ \_ WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) с параметром функции *хинтернет* , имеющим значение **null**. Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**. Если этот раздел реестра не задан, служба WinHTTP вернет ошибку **Ошибка \_ WinHTTP \_ Недопустимый \_ параметр**. Этот раздел реестра отсутствует по умолчанию. Когда она задана, WinINet отправит учетные данные на WinHTTP. Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet. Чтобы предоставить общий доступ к учетным данным сервера в дополнение к учетным данным прокси-сервера, пользователям необходимо задать **\_ параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**\_ \_ тип обработчика параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает длинное целочисленное значение без знака, содержащее тип переданного в [хинтернет](hinternet-handles-in-winhttp.md) маркера. Может возвращаться одно из следующих значений:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>\_тип обработчика WinHTTP \_ \_ Connect | Этот маркер является маркером соединения. |
| <span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>\_запрос типа для обработчика WinHTTP \_ \_ | Этот маркер является обработчиком запросов. |
| <span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>\_сеанс типа для обработчика WinHTTP \_ \_ | Этот обработчик является обработчиком сеанса. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Предотвращает использование в запросе версий протокола, отличных от, включенных **\_ параметром WinHTTP, \_ Включение \_ \_ протокола HTTP** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**\_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает значение типа DWORD, указывающее, какая расширенная версия HTTP использовалась для данного запроса. Список возможных значений см. в разделе **параметр WinHTTP \_ \_ включить \_ \_ протокол HTTP**.



</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**\_ \_ Версия HTTP параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Задает или получает структуру [**\_ \_ сведений о версии HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) , которая содержит поддерживаемую версию HTTP. Это параметр на уровне процесса; для этого маркера используйте **значение NULL** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**\_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме**
</dt> <dd> <dl> <dt>



Позволяет защищенным подключениям использовать сертификаты безопасности, для которых не удалось скачать список отзыва сертификатов.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**\_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6**
</dt> <dd> <dl> <dt>



Включает быстрое резервное восстановление IPv6 (более глаз) для подключения. Такое поведение аналогично поведению счастливого глаз, описанного в [RFC 6555](https://tools.ietf.org/html/rfc6555) , для повышения времени подключения в сетях, в которых IPv6 является ненадежным.
- Если адреса IPv6 и IPv4 разрешаются для данного узла, служба WinHttp начнет с подключения к первому разрешенному IPv6-адресу с коротким (300 мс) временем ожидания.
- Если соединение не будет выполнено, служба WinHttp попытается подключиться к первому разрешенному IPv4-адресу со стандартным временем ожидания.
- Если произойдет сбой второго подключения, служба WinHttp попытается повторить первый разрешенный IPv6-адрес со стандартным временем ожидания.
- В случае сбоя третьего подключения WinHttp вернется к поведению по умолчанию для оставшихся адресов, пытаясь подключиться к каждому из них со стандартным временем ожидания до тех пор, пока не будет установлено соединение или не останется ни одного адреса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**\_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_**
</dt> <dd> <dl> <dt>



Возвращает значение, указывающее, может ли быть получен ответ на возвращаемое соединение прокси-сервера.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер HTTP/1.0. Значение по умолчанию — **Infinite**.

**Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008:** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**\_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее максимально допустимое количество подключений на сервер. Значение по умолчанию — **Infinite**.

Если этот параметр имеет значение 0, WinHTTP устанавливает ограничение на число подключений равным 2.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**\_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP**
</dt> <dd> <dl> <dt>



Задает максимальное число перенаправлений, которые следует указать WinHTTP; значение по умолчанию — 10. Это ограничение не позволяет неавторизованным сайтам сделать остановку клиента WinHTTP после большого числа перенаправлений.

**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**\_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP**
</dt> <dd> <dl> <dt>



Максимальное число ответов с кодом состояния 100-199, которые игнорируются перед возвратом окончательного кода состояния клиенту WinHTTP. Коды состояния 100-199 могут отправляться сервером перед окончательным кодом состояния и описаны в спецификации HTTP/1.1 (Дополнительные сведения см. в [документе RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)). Значение по умолчанию равно 10.

**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_**
</dt> <dd> <dl> <dt>



Объект, привязанный к объему данных, остановленных из ответов для повторного использования соединения, указанного в байтах. Значение по умолчанию — 1 МБ.

**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**\_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа**
</dt> <dd> <dl> <dt>



Ограничивающий набор для максимального размера части заголовка ответа сервера, указанного в байтах. Эта привязка защищает клиента от неавторизованного сервера, пытающегося приостановки работы клиента, отправив ответ с бесконечным объемом данных заголовка. Значение по умолчанию — 64 КБ.

**Windows XP с SP1 и windows 2000 с пакетом обновления 3 (SP3):** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**\_ \_ родительский маркер параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Получает родительский маркер для этого маркера.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**\_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_**
</dt> <dd> <dl> <dt>



Извлекает строку, содержащую [*фирменный*](glossary.md) текст, предоставленный сервером входа Passport. Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401. Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**\_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает строку, содержащую URL-адрес [*фирменной символики*](glossary.md) , предоставляемой сервером входа Passport. Этот параметр следует получать сразу после ответа сервера входа с кодом состояния 401. Приложение должно передавать размер буфера в байтах, достаточно большой для хранения возвращаемой строки.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**\_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP**
</dt> <dd> <dl> <dt>



Устанавливает параметр "только для чтения" для обработчика запроса, который получает URL-адрес возврата Passport.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**\_команда WinHTTP \_ выход \_ \_ из паспорта**
</dt> <dd> <dl> <dt>



Задает параметр в обработчике сеанса для выхода из любых имен входа Passport. Приложение должно передать URL-адрес возврата Passport, полученный с помощью **\_ функции WinHTTP \_ \_ \_ URL-адрес возврата Passport**. Все файлы cookie, связанные с URL-адресом возврата, очищаются.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**\_пароль для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает строковое значение, содержащее пароль, связанный с обработчиком запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**\_ \_ прокси-сервер параметров WinHTTP**
</dt> <dd> <dl> <dt>



Задает или получает структуру [**\_ \_ сведений о прокси-сервере WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) , которая содержит данные прокси-сервера для существующего обработчика сеанса или обработчика запроса. При получении данных прокси-сервера приложение должно освободить строки **лпсзпрокси** и **лпсзпроксибипасс** , содержащиеся в этой структуре (если они не **равны NULL**), с помощью функции [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Приложение может запросить данные глобального прокси-сервера (прокси-сервер по умолчанию), передав маркер **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**\_ \_ пароль прокси-сервера для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает строковое значение, содержащее пароль, используемый для доступа к прокси-серверу.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**\_используется параметр WinHTTP \_ прокси- \_ службы \_**
</dt> <dd> <dl> <dt>



Возвращает имя участника прокси-сервера, предоставляемое WinHTTP для SSPI во время проверки подлинности. Это строковое значение является усефор передачей в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**\_параметр WinHTTP \_ \_ имя пользователя-посредника**
</dt> <dd> <dl> <dt>



Задает или получает строковое значение, содержащее имя пользователя, используемое для доступа к прокси-серверу.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**\_ \_ \_ Размер буфера чтения параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Этот параметр является устаревшим; Он не действует.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**\_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_**
</dt> <dd> <dl> <dt>



Задает, может ли быть получена сущность ответа прокси-сервера. Этот параметр отключен по умолчанию.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**\_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) ожидания получения всех заголовков ответа в запрос. Если служба WinHTTP не получает все заголовки в течение этого периода ожидания, запрос отменяется. Значение времени ожидания по умолчанию — 90 секунд.

Это время ожидания проверяется только при получении данных от сокета. В результате, по истечении времени ожидания клиентское приложение не получает уведомления, пока не поступают дополнительные данные с сервера. Если данные не поступают с сервера, задержка между истечением времени ожидания и уведомлением клиентского приложения может быть выше, чем значение времени ожидания, заданное с помощью параметра *дврецеиветимеаут* функции [**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**\_ \_ время ожидания получения параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, которое содержит значение времени ожидания (в миллисекундах) для получения частичного ответа на запрос или чтения некоторых данных. Если ответ длится дольше этого значения времени ожидания, запрос отменяется. По умолчанию время ожидания составляет 30 секунд.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**\_ \_ политика перенаправления для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает поведение WinHTTP в отношении обработки кода состояния перенаправления HTTP повышалась. Этот параметр может быть установлен для сеанса или в обработчике запроса на одно из следующих значений:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>\_параметр WinHTTP \_ политика перенаправления \_ \_ всегда | Все перенаправления выполняются автоматически. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>\_ \_ политика перенаправления параметра WinHTTP \_ \_ запретить \_ HTTPS \_ для \_ http | Все перенаправления выполняются, за исключением тех, которые исходят от защищенного URL-адреса (HTTPS) на небезопасный (http) URL-адрес. Это параметр по умолчанию. |
| <span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>\_параметр WinHTTP \_ Перенаправление \_ политики \_ никогда не | Перенаправления не идут. Состояние повышалась возвращается приложению. |


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**\_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе**
</dt> <dd> <dl> <dt>



Отклоняет URL-адреса, содержащие имя пользователя и пароль. Этот параметр также отклоняет URL-адреса, содержащие семантику *username: Password* , даже если имя пользователя или пароль не указаны. Например, " u:p@hostname ", " :@hostname ", " u:@hostname " и " :p@hostname " будут помечены как недопустимые. Если функции передан недопустимый URL-адрес, он возвращает [ошибку \_ WinHTTP \_ Недопустимый \_ URL-адрес](error-messages.md). По умолчанию этот параметр выключен.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**\_ \_ приоритет запроса параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Этот параметр является устаревшим; Он не действует.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**\_ \_ Статистика запросов параметров \_ WinHTTP**
</dt> <dd> <dl> <dt>



Статистика извлекает для запроса.  Список доступных статистических данных см. в разделе [**\_ \_ Статистика запросов WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**\_ \_ время запроса параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Сведения о времени извлекает для запроса. Список доступных времени см. в разделе [**\_ \_ время запроса WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**\_ \_ время ожидания разрешения параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для разрешения имени узла. Значение времени ожидания по умолчанию — **Infinite**. Если указано значение, отличное от значения по умолчанию, то для разрешения имен создается дополнительная нагрузка на один поток.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**Параметры WINHTTP для \_ \_ защищенных \_ протоколов**
</dt> <dd> <dl> <dt>



Задает длинное целое число без знака, которое указывает, какие безопасные протоколы приемлемы. По умолчанию в Windows 7 и Windows 8 включены только SSL3 и TLS1. По умолчанию в Windows 8.1 и Windows 10 включены только SSL3, TLS 1.0, TLS 1.1 и TLS 1.2. Значение может быть сочетанием одного или нескольких из следующих значений.

| Термин | Описание |
|-|-|
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>\_флаг WinHTTP \_ безопасный \_ протокол \_ | Можно использовать протоколы SSL (SSL) 2,0, SSL 3,0 и TLS 1,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>SSL2 протокола WINHTTP с \_ флагом \_ Secure \_ \_ | Можно использовать протокол SSL 2,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>SSL3 протокола WINHTTP с \_ флагом \_ Secure \_ \_ | Можно использовать протокол SSL 3,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>TLS1 протокола WINHTTP с \_ флагом \_ Secure \_ \_ | Можно использовать протокол TLS 1,0. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 1 | Можно использовать протокол TLS 1,1. |
| <span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>\_Флаг WinHTTP \_ \_ протокол Secure \_ TLS1 \_ 2 | Можно использовать протокол TLS 1,2. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**\_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает сертификат для сервера SSL/TLS в структуру [**\_ \_ сведений о сертификате WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) . Приложение должно освободить члены **лпсзсубжектинфо** и **Лпсзиссуеринфо** с помощью [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**\_ \_ Флаги безопасности для параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее флаги безопасности для маркера. Это может быть сочетание следующих значений:

| Термин | Описание |
|-|-|
| <span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>\_флаг безопасности \_ игнорирует \_ \_ недопустимое общее имя сертификата \_ |Разрешает недопустимое общее имя в сертификате; то есть имя сервера, указанное приложением, не соответствует общему имени в сертификате. Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ \_ \_ Недопустимый** обратный вызов для сертификата. |
| <span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>\_ \_ \_ \_ Недопустимый срок игнорирования даты сертификата \_ для флага безопасности |Разрешает недействительную дату сертификата, то есть просроченный или еще не действующий сертификат. Если этот флаг установлен, приложение не получает **\_ \_ \_ \_ \_ \_ Недопустимый обратный вызов для флага состояния обратного вызова WinHTTP** . |
| <span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>\_ \_ пропуск \_ неизвестного \_ ЦС в качестве флага безопасности | Разрешает недопустимый центр сертификации. Если этот флаг установлен, приложение не получает **\_ флаг состояния обратного вызова WinHTTP \_ \_ \_ Недопустимый \_** обратный вызов CA. |
| <span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>\_флаг безопасности \_ игнорирует \_ \_ неправильный способ \_ использования сертификата | Позволяет установить удостоверение сервера с помощью сертификата, не являющегося сервером (например, сертификата клиента). |
| <span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>\_флаг безопасности \_ игнорирует \_ слабую \_ подпись | Позволяет игнорировать слабую подпись.<br/>Этот флаг доступен в обновлении свертки для каждой ОС, начиная с Windows 7 и Windows Server 2008 R2. |
| <span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>\_безопасный флаг \_ безопасности | Использует безопасные передачи. Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>уровень \_ стойкости флага безопасности \_ \_ | Использует среднее (56-разрядное) шифрование. Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>\_сильная стойкость флага безопасности \_ \_ | Использует стойкое (128-разрядное) шифрование. Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |
| <span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>\_ \_ слабая стойкость ФЛАГа безопасности \_ | Использует слабое (40-разрядное) шифрование. Это значение возвращается только при вызове [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption). |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**\_ \_ сведения о безопасности параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает подключение SChannel и сведения о шифрах для запроса.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**\_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Извлекает длинное целое значение без знака, содержащее стойкость шифра ключа шифрования. Большее число означает более надежное шифрование стойкости шифра.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**\_ \_ время ожидания отправки для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает длинное целое число без знака, содержащее значение времени ожидания (в миллисекундах) для отправки запроса или записи некоторых данных. Если отправка запроса длится дольше, чем время ожидания, операция отправки отменяется. По умолчанию время ожидания составляет 30 секунд.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**\_ \_ CBT сервера параметров \_ WinHTTP**
</dt> <dd> <dl> <dt>



Возвращает указатель на структуру [**\_ привязок секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) , указывающую маркер привязки канала (CBT).

Токен привязки канала — это свойство защищенного канала транспорта, которое используется для привязки канала проверки подлинности к защищенному каналу транспорта. Этот маркер может быть получен только этим параметром после установки SSL-соединения.

> [!Note]
> При передаче этого параметра и значения **null** для *лпбуффер* в [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) будет возвращена ошибка \_ , недостаточная для буфера \_ , и необходимый размер в байтах для буфера в параметре *лпдвбуфферленгс* . Возвращаемое значение размера буфера можно передать при последующем вызове запроса для маркера привязки канала. Эти действия необходимы при обработке \_ запроса состояния обратного вызова WinHTTP, \_ \_ Если требуется изменить заголовки запроса на основе токена привязки канала. Обратите внимание, что Windows XP и Vista не поддерживают изменение заголовков запросов во время этого обратного вызова.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**\_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_**
</dt> <dd> <dl> <dt>



Извлекает контекст цепочки сертификатов сервера. Служба **WinHTTP \_ \_ \_ \_ \_ Контекст цепочки сертификатов сервера** может быть передан для получения повторяющегося указателя на **\_ \_ контекст цепочки** сертификатов для цепочки сертификата сервера, полученной во время согласованного SSL-соединения. Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**\_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP**
</dt> <dd> <dl> <dt>



Получает контекст сертификации сервера. Служба **WinHTTP \_ Для получения повторяющегося указателя на контекст сертификата сервера, полученного во время согласованного SSL-соединения, можно передать параметр \_ \_ \_ контекстного сертификата сервера** . [](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Клиент должен вызвать [**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) для возвращенного \_ указателя контекста пкцерт, который заполнен в буфере.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**\_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Возвращает имя участника серверного сервера, которое WinHTTP было передано в SSPI во время проверки подлинности. Это строковое значение может быть передано в [**сспипромптфоркредентиалс**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) после сбоя проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**\_ \_ имя субъекта-службы для параметра WinHTTP**
</dt> <dd> <dl> <dt>



Включает или удаляет номер порта сервера, если имя участника-службы (SPN) создано для проверки подлинности Kerberos или Negotiate. Этот флаг имеет одно из следующих значений:

| Термин | Описание |
|-|-|
| <span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ отключение \_ \_ порта сервера \_ SPN | Удаляет номер порта сервера. |
| <span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>\_ \_ \_ порт сервера службы WinHTTP Enable SPN \_ | Включает номер порта сервера. |


</dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**\_параметр WinHTTP \_ TCP \_ fast \_ Open**
</dt> <dd> <dl> <dt>



Включает TCP Fast Open для подключения.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**\_параметр WinHTTP \_ \_ KeepAlive TCP**
</dt> <dd> <dl> <dt>



Этот параметр можно задать для обработчика сеанса WinHttp, чтобы включить поведение проверки активности TCP на базовом сокете. Принимает структуру [**TCP \_ KeepAlive**](/windows/win32/winsock/sio-keepalive-vals) .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**\_Запуск параметра WinHTTP \_ TLS \_ false \_**
</dt> <dd> <dl> <dt>



Включает для соединения параметр TLS false.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**\_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Принимает событие, которое будет задано после завершения последнего обратного вызова для определенного сеанса. Этот флаг должен быть использован для обработчика сеанса. Событие не может быть закрыто до тех пор, пока оно не будет установлено WinHTTP.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**\_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Этот параметр зарезервирован для внутреннего использования и не должен вызываться.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**\_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета**
</dt> <dd> <dl> <dt>



Указывает стеку запустить процесс подтверждения соединения WebSocket с [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Этот параметр не принимает параметров.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**\_ \_ URL-адрес параметра WinHTTP**
</dt> <dd> <dl> <dt>



Извлекает строковое значение, содержащее полный URL-адрес скачанного ресурса. Если исходный URL-адрес содержал дополнительные данные, например строки поиска или привязки, или если вызов был перенаправлен, то возвращаемый URL-адрес отличается от исходного. Приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**\_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера**
</dt> <dd> <dl> <dt>



Принимает **логическое** значение и может устанавливать только обработчик сеанса. Она будет распространяться только на дескрипторы, созданные из дескриптора сеанса после установки параметра. Если **значение — true**, этот параметр приводит к тому, что в качестве последнего средства используется учетные данные глобального сервера, которые были отправлены из wininet. Значение по умолчанию для этого параметра — **false**. Для этого параметра требуется раздел реестра **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet параметры Интернета! Шарекредсвисвинхттп**. Этот раздел реестра отсутствует по умолчанию. Когда она задана, WinINet отправит учетные данные на WinHTTP. Всякий раз, когда WinHttp получает запрос проверки подлинности и если для текущего обработчика не заданы учетные данные, он будет использовать учетные данные, предоставляемые WinINet.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**\_ \_ Агент пользователя для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает строку [*агента пользователя*](glossary.md) для дескрипторов, предоставляемых [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) , и используется в последующих функциях [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) , если она не переопределяется заголовком, добавленным [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) или **WinHttpSendRequest**. При извлечении агента пользователя приложение должно передать в буфер размер в байтах, достаточно большой для хранения возвращенного URL-адреса в расширенном символе. При задании агента пользователя размер буфера — это длина строки в символах и знак завершения **null** .


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**\_имя пользователя для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает строку, содержащую имя пользователя.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**\_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает время в миллисекундах, которое [**винхттпвебсоккетклосе**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) должно ожидать завершения подтверждения закрытия. Значение по умолчанию — 10 секунд.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**\_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает интервал (в миллисекундах) отправки пакета проверки активности через соединение. Интервал по умолчанию — 30000 (30 секунд). Минимальный интервал — 15000 (15 секунд). Использование [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) для установки значения ниже 15000 будет возвращать ошибку с **\_ недопустимым \_ параметром**.

> [!Note]
> Значение по умолчанию **для \_ параметра \_ WinHTTP \_ \_ \_ интервал проверки активности веб-сокета** считывается из раздела **HKLM: \\ Software \\ Microsoft \\ WebSocket \\ KeepaliveInterval**. Если значение не задано, будет использоваться значение по умолчанию 30000. Более низкий интервал активности не может превышать 15000 миллисекунд.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**\_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_**
</dt> <dd> <dl> <dt>



Задает или получает значение типа DWORD, указывающее размер буфера приема, используемый для подключений WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**\_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_**
</dt> <dd> <dl> <dt>



Задает или получает значение типа DWORD, указывающее размер буфера отправки, используемый для подключений WebSocket.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**\_ \_ \_ число рабочих потоков \_ параметра WinHTTP**
</dt> <dd> <dl> <dt>



Задает длинное целочисленное значение без знака, указывающее количество рабочих потоков, которые пул потоков должен использовать для асинхронных завершений. Значение этого параметра по умолчанию равно нулю, что указывает, что количество рабочих потоков равно числу процессоров в системе. Этот параметр может быть установлен только для [хинтернетного](hinternet-handles-in-winhttp.md) маркера **до выполнения** асинхронной операции.   Этот параметр можно задать только один раз.

**Windows Server 2008 R2 и Windows 7:** Этот флаг устарел.


</dt> </dl> </dd> <dt>

<span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**\_ \_ \_ Размер буфера записи параметра \_ WinHTTP**
</dt> <dd> <dl> <dt>



Этот параметр является устаревшим; Он не действует.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

В следующей таблице перечислены флаги параметров, указывающие, какие дескрипторы могут действовать, можно ли запрашивать и задавать их, а также использовать тип данных. "X" означает, что флаг параметра является допустимым для использования с функцией или обработчиком, а "-" указывает на недопустимый флаг параметра.

Попытка задать или запросить флаг параметра в версии Windows, где она не поддерживается, приведет к **ошибке \_ \_ "Недопустимый WinHTTP \_ "**.

| Флаг параметра и тип данных | Обработчик сеанса | Маркер запроса | Параметр запросов | Параметр SET | Минимальная версия Windows |
|-|-|-|-|-|-|
| \_параметр WinHTTP \_ — \_ \_ неблокирующие \_ обратные вызовы<br/>**ЛОГИЧЕСКОМ** | X | \- | \- | X | \- |
| \_ \_ политика автоматического входа в службу WinHTTP \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_ \_ обратный вызов параметра WinHTTP<br/>**лпвоид** | X | X | X | X | \- |
| \_ \_ \_ контекст сертификата клиента для параметра WinHTTP \_<br/>[**\_контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | \- | X | Windows Vista |
| \_ \_ \_ \_ список поставщиков сертификатов клиента для параметра WinHTTP \_<br/>[**Секпкгконтекст \_ иссуерлистинфоекс**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | X | X | \- | Windows Vista |
| \_ \_ кодовая страница параметра WinHTTP<br/>**DWORD** | X | \- | \- | X | \- |
| \_параметр WinHTTP \_ Настройка \_ \_ проверки подлинности паспорта<br/>**DWORD** | X | \- | \- | X | \- |
| \_ \_ повторные попытки соединения с ПАРАМЕТРом WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ время ожидания соединения для параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ сведения о соединении параметров WinHTTP \_<br/>[**\_сведения о подключении к WinHTTP \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | X | X | \- | \- |
| \_Параметр WinHTTP \_ Connection \_ stats \_ v0<br/>[**\_V0 сведения о TCP \_**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | X | X | \- | Windows 10, версия 1903 |
| \_Параметр WinHTTP \_ Connection \_ stats \_ v1<br/>[**\_Сведения о TCP \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | X | X | \- | Windows 10, версия 2004 |
| \_ \_ значение контекста WinHTTP для параметра \_<br/>**DWORD \_ ptr** | X | X | X | X | \- |
| \_ \_ распаковка параметров WinHTTP<br/>**DWORD** | X | X | \- | X | Windows 8.1 |
| \_ \_ функция отключения параметров \_ WinHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| \_параметр WinHTTP \_ Отключить \_ откат безопасных \_ протоколов \_<br/>**ЛОГИЧЕСКОМ** | X | \- | \- | X | Windows 10, версия 1903 |
| \_параметр WinHTTP \_ Отключить \_ \_ очередь потока<br/>**ЛОГИЧЕСКОМ** | X | X | \- | X | Windows 10, версия 1809 |
| \_ \_ Включение \_ функции WinHTTP<br/>**DWORD** | \* | \* | \- | X | \- |
| \_параметр WinHTTP \_ Включение \_ \_ протокола HTTP<br/>**DWORD** | X | X | \- | X | Windows 10 версии 1607 |
| \_параметр WinHTTP \_ енаблетраЦинг<br/>**DWORD** | \- | \- | X | X | \- |
| \_ \_ добавочная кодировка параметров WinHTTP \_<br/>**ЛОГИЧЕСКОМ** | X | X | \- | X | Windows 10, версия 1803 |
| \_ \_ срок действия соединения для параметра WinHTTP \_<br/>Н/Д | \- | X | \- | X | Windows 10, версия 1903 |
| \_ \_ Расширенная ошибка при выборе WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| \_ \_ \_ учетные записи глобального прокси-сервера параметров WinHTTP \_<br/>[**учетные учетные \_ службы WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | X | X | \- | X | \- |
| Параметры WINHTTP глобальные учетные значения \_ \_ \_ сервера \_<br/>[**учетные учетные службы WINHTTP, \_ \_ пример**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | X | X | \- | X | \- |
| \_ \_ тип обработчика параметров WinHTTP \_<br/>**DWORD** | X | X | X | \- | \- |
| \_ \_ \_ требуется протокол HTTP для параметра WinHTTP \_<br/>**ЛОГИЧЕСКОМ** | X | X | \- | X | Windows 10, версия 1903 |
| \_ \_ \_ используемый протокол HTTP \_ для параметра WinHTTP<br/>**DWORD** | \- | X | X | \- | Windows 10 версии 1607 |
| \_ \_ Версия HTTP параметра \_ WinHTTP<br/>[**\_ \_ сведения о версии HTTP**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | X | X | X | X | \- |
| \_параметр WinHTTP \_ игнорировать \_ отзыв сертификата в \_ \_ автономном режиме<br/>**ЛОГИЧЕСКОМ** | \- | X | \- | X | Windows 10, версия 2004 |
| \_ \_ \_ Быстрый откат параметров WinHTTP \_ IPv6<br/>**ЛОГИЧЕСКОМ** | X | \- | \- | X | Windows 10, версия 1903 |
| \_параметр WinHTTP \_ — \_ ответ прокси- \_ подключения \_<br/>**ЛОГИЧЕСКОМ** | X | X | X | \- | \- |
| \_Параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ \_ \_ сервер 1 0<br/>**DWORD** | X | \- | X | X | \- |
| \_параметр WinHTTP \_ Максимальное число \_ \_ серверов на \_ сервер<br/>**DWORD** | X | \- | X | X | \- |
| \_параметр WinHTTP \_ Максимальное \_ число \_ автоматических \_ перенаправлений HTTP<br/>**DWORD** | X | X | X | X | \- |
| \_продолжение параметра \_ максимального \_ \_ состояния HTTP \_ для WinHTTP<br/>**DWORD** | X | X | X | X | \- |
| параметр WINHTTP — \_ \_ максимальный \_ \_ Размер очистки ответа \_<br/>**DWORD** | X | X | X | X | \- |
| \_параметр WinHTTP \_ максимальный \_ \_ размер заголовка \_ ответа<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ родительский маркер параметра WinHTTP \_<br/>[хинтернет](hinternet-handles-in-winhttp.md) | X | X | X | \- | \- |
| \_параметр WinHTTP \_ , \_ софирменный текст в паспорте \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ \_ URL-адрес КОфирменной символики для службы WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ \_ \_ URL-адрес возврата паспорта с параметром WinHTTP<br/>**лпвоид** | \- | X | X | \- | \- |
| \_команда WinHTTP \_ выход \_ \_ из паспорта<br/>**лпвоид** | X | \- | \- | X | \- |
| \_пароль для параметра WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_ \_ прокси-сервер параметров WinHTTP<br/>[**\_сведения о прокси-сервере WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | X | X | X | X | \- |
| \_ \_ пароль прокси-сервера для параметра WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_используется параметр WinHTTP \_ прокси- \_ службы \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_параметр WinHTTP \_ \_ имя пользователя-посредника<br/>**LPWSTR** | \- | X | X | X | \- |
| \_ \_ \_ Размер буфера чтения параметра \_ WinHTTP<br/>**DWORD** | \- | X | X | X | \- |
| \_параметр WinHTTP \_ Получение \_ ответа прокси-сервера \_ \_<br/>**ЛОГИЧЕСКОМ** | X | X | \- | X | \- |
| \_ \_ \_ время ожидания ответа для получения параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ время ожидания получения параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ политика перенаправления для параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_параметр WinHTTP \_ отклонять \_ усерпвд \_ в \_ URL-адресе<br/>**ЛОГИЧЕСКОМ** | \- | X | \- | X | \- |
| \_ \_ приоритет запроса параметра \_ WinHTTP<br/>**DWORD** | \- | X | X | X | \- |
| \_ \_ Статистика запросов параметров \_ WinHTTP<br/>[**\_Статистика запросов \_ WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | X | X | \- | Windows 10, версия 1903 |
| \_ \_ время запроса параметра \_ WinHTTP<br/>[**\_время запроса \_ WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | X | X | \- | Windows 10, версия 1903 |
| \_ \_ время ожидания разрешения параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| Параметры WINHTTP для \_ \_ защищенных \_ протоколов<br/>**DWORD** | X | \- | \- | X | \- |
| \_ \_ \_ Структура сертификата безопасности параметра \_ WinHTTP<br/>[**\_сведения о сертификате WinHTTP \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | X | X | \- | \- |
| \_ \_ Флаги безопасности для параметров WinHTTP \_<br/>**DWORD** | \- | X | X | X | \- |
| \_ \_ сведения о безопасности параметров WinHTTP \_<br/>[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | X | X | \- | Windows 10, версия 2004 |
| \_ \_ \_ разрядность ключа безопасности параметра WinHTTP \_<br/>**DWORD** | \- | X | X | \- | \- |
| \_ \_ время ожидания отправки для параметра WinHTTP \_<br/>**DWORD** | X | X | X | X | \- |
| \_ \_ CBT сервера параметров \_ WinHTTP<br/>[**\_Привязки секпкгконтекст**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\* | \- | X | X | \- | \- |
| \_параметр WinHTTP \_ \_ \_ контекст цепочки сертификатов сервера \_<br/>[**CERT_CHAIN_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | X | X | \- | Windows 10, версия 2004 |
| \_ \_ \_ контекст сертификата сервера параметров \_ WinHTTP<br/>[**КОНТЕКСТ СЕРТИФИКАТА**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | X | X | \- | \- |
| \_ \_ \_ используемое имя субъекта-службы сервера параметров WinHTTP \_<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_ \_ имя субъекта-службы для параметра WinHTTP<br/>**DWORD** | \- | X | \- | X | \- |
| \_параметр WinHTTP \_ TCP \_ fast \_ Open<br/>**ЛОГИЧЕСКОМ** | X | \- | \- | X | Windows 10, версия 2004 |
| \_параметр WinHTTP \_ \_ KeepAlive TCP<br/>[**\_KeepAlive TCP**](/windows/win32/winsock/sio-keepalive-vals) | X | \- | \- | X | Windows 10, версия 2004 |
| \_Запуск параметра WinHTTP \_ TLS \_ false \_<br/>**ЛОГИЧЕСКОМ** | X | \- | \- | X | Windows 10, версия 2004 |
| \_ \_ \_ событие уведомления о ВЫгрузке параметра WinHTTP \_<br/>[хинтернет](hinternet-handles-in-winhttp.md) | X | \- | \- | X | \- |
| \_ \_ \_ синтаксический анализ ненадежного заголовка для параметра WinHTTP \_<br/>**DWORD** | \- | X | \- | X | \- |
| \_Обновление параметра \_ WinHTTP \_ до \_ веб- \_ сокета<br/>Н/Д | \- | X | \- | X | \- |
| \_ \_ URL-адрес параметра WinHTTP<br/>**LPWSTR** | \- | X | X | \- | \- |
| \_параметр WinHTTP \_ использовать \_ \_ \_ учетные данные глобального сервера<br/>**ЛОГИЧЕСКОМ** | X | X | \- | X | \- |
| \_ \_ Агент пользователя для параметра WinHTTP \_<br/>**LPWSTR** | X | \- | X | X | \- |
| \_имя пользователя для параметра WinHTTP \_<br/>**LPWSTR** | \- | X | X | X | \- |
| \_ \_ \_ \_ время ожидания закрытия веб-СОКЕТа для параметра WinHTTP \_<br/>**DWORD** | \- | \- | X | X | \- |
| \_интервал проверки \_ активности веб- \_ сокета для \_ параметра WinHTTP \_<br/>**DWORD** | \- | \- | X | X | \- |
| \_параметр WinHTTP \_ \_ \_ \_ Размер буфера получения веб-сокета \_<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_ \_ \_ \_ \_ Размер буфера отправки для веб-сокета параметров WinHTTP \_<br/>**DWORD** | X | X | X | X | Windows 8.1 |
| \_ \_ \_ число рабочих потоков \_ параметра WinHTTP<br/>**DWORD** | \- | \- | \- | X | \- |
| \_ \_ \_ Размер буфера записи параметра \_ WinHTTP<br/>**DWORD** | \- | X | X | X | \- |

> [!Note]
> Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md).

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------------------------|---------------------------------------------------------------------------------|
| Минимальная версия клиента | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]            |
| Минимальная версия сервера | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]         |
| Распространяемые компоненты          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000. |
| Заголовок                   | WinHTTP. h                                                                       |

## <a name="see-also"></a>См. также раздел

[Версии WinHTTP](winhttp-versions.md)
