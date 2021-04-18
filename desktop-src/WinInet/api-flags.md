---
title: Флаги API (WinInet. h)
description: Многие функции WinINet принимают массив флагов в качестве параметра. Ниже приведено краткое описание определенных флагов.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710511"
---
# <a name="api-flags"></a>Флаги API

Многие функции WinINet принимают массив флагов в качестве параметра. Ниже приведено краткое описание определенных флагов.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**\_Файл cookie Интернета \_ оценивает \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Указывает, что для файла cookie будет связан заголовок платформы для защиты конфиденциальности (P3P).


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**\_сторонние файлы cookie Интернета \_ \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Указывает, что файл cookie стороннего производителя устанавливается или извлекается.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_флаг Интернета \_ Async**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Делает только асинхронные запросы к дескрипторам в порядке убывания из дескриптора, возвращенного этой функцией. Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_кэш флагов Интернета \_ \_ Async**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Разрешает отложенную запись в кэш.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**\_кэш флагов Интернета в \_ \_ случае \_ \_ сбоя NET**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Возвращает ресурс из кэша в случае сбоя сетевого запроса ресурса из-за [ошибки \_ \_ \_ сброса подключения к Интернету](wininet-errors.md) или [ошибки подключения \_ \_ \_ к Интернету](wininet-errors.md) . Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_ \_ кэш не Internet \_ Flag**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Не добавляет возвращенную сущность в кэш. Это эквивалентно предпочтительному значению, [ \_ флагу \_ Интернета \_ нет \_ записи в кэш](/windows).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**Флаг Интернета — \_ \_ существующее \_ подключение**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Пытается использовать существующий объект [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , если он существует с теми же атрибутами, которые требуются для выполнения запроса. Это полезно только при использовании FTP-операций, так как FTP является единственным протоколом, который обычно выполняет несколько операций во время одного сеанса. WinINet кэширует один обработчик соединения для каждого [**хинтернетного**](appendix-a-hinternet-handles.md) маркера, созданного [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и **интернетконнект** используют этот флаг для соединений HTTP и FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_Отправка форм флагов Интернета \_ \_**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Указывает, что это отправка форм.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_флаг Интернета \_ из \_ кэша**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Не выполняет сетевые запросы. Все сущности возвращаются из кэша. Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден. Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_флаг Интернета \_ ФВД \_ назад**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Указывает, что функция должна использовать копию ресурса, который в данный момент находится в кэше Интернета. Дата окончания срока действия и другие сведения о ресурсе не проверяются. Если запрошенный элемент не найден в кэше Интернета, система пытается найти ресурс в сети. Это значение было представлено в Microsoft Internet Explorer 5 и связано с операциями « **вперед** » и « **назад** » обозревателя Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_Гиперссылка для Internet Flag \_**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Принудительная перезагрузка при отсутствии истечения срока действия и отсутствии времени LastModified, возвращенного сервером при определении необходимости перезагрузки элемента из сети. Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**\_флаг Интернета \_ игнорирует \_ \_ недопустимое общее имя сертификата \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Отключает проверку сертификатов на основе SSL/PCT, возвращаемых с сервера по имени узла, заданному в запросе. WinINet использует простую проверку сертификатов, сравнивая их с именами узлов и простыми правилами с подстановочными знаками. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**Флаг Интернета не \_ \_ учитывать \_ \_ дату сертификата \_**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Отключает проверку сертификатов на основе SSL/PCT для правильных дат действия. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_флаг Интернета \_ пропустить \_ Перенаправление \_ на \_ http**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Отключает обнаружение этого специального типа перенаправления. При использовании этого флага WinINet прозрачно разрешает перенаправление с URL-адресов HTTPS на HTTP. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_флаг Интернета \_ пропустить \_ Перенаправление \_ на \_ HTTPS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Отключает обнаружение этого специального типа перенаправления. При использовании этого флага WinINet явным образом разрешает перенаправление с URL-адресов HTTP на HTTPS. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_Подключение флага Интернета \_ \_**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Использует для соединения семантику проверки активности, если она доступна. Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов). Этот флаг является обязательным для Microsoft Network (MSN), NTLM и других типов проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_флаг Интернета \_ сделать \_ постоянным**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Больше не поддерживается.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**\_флаг Интернета \_ должен \_ кэшировать \_ запрос**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Аналогично предпочтительному значению, для **\_ флага Интернета \_ требуется \_ файл**. Вызывает создание временного файла, если файл не может быть кэширован. Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**для \_ флага Интернета \_ требуется \_ файл**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Вызывает создание временного файла, если файл не может быть кэширован. Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET \_ Flag \_ без \_ проверки подлинности**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Не пытается автоматически пройти проверку подлинности. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_флаг Интернета \_ без \_ автоматического \_ перенаправления**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Не обрабатывает перенаправление в [**хттпсендрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)автоматически. Этот флаг также может использоваться [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) для HTTP-запросов.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_флаг Интернета \_ без \_ записи в кэш \_**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Не добавляет возвращенную сущность в кэш. Этот флаг используется, [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_флаг Интернета \_ нет \_ файлов cookie**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Не добавляет к запросам заголовки файлов cookie автоматически и не добавляет возвращенные файлы cookie в базу данных cookie. Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (для HTTP-запросов).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_флаг Интернета \_ нет \_ пользовательского интерфейса**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Отключает диалоговое окно "файл cookie". Этот флаг может использоваться [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только HTTP-запросы).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_отключить флаг \_ Интернета**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Аналогично **\_ флагу Интернета \_ из \_ кэша**. Не выполняет сетевые запросы. Все сущности возвращаются из кэша. Если запрошенный элемент отсутствует в кэше, возвращается подходящая ошибка, например \_ файл ошибок \_ не \_ найден. Этот флаг используется только в функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_ \_ пассивный флаг Интернета**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Использует пассивную семантику FTP. Этот флаг используется только для [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . [**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует этот флаг для FTP-запросов, а [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) использует этот флаг для FTP-файлов и каталогов.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**параметр INTERNET \_ Flag \_ pragma \ \_ Cache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Вызывает принудительное разрешение запроса сервером-источником, даже если кэшированная копия существует на прокси-сервере. Функция [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для запросов HTTP и HTTPS) и функция [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) используют этот флаг.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ необработанные \_ данные Internet Flag**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Возвращает данные в виде структуры [**Win32 \_ Find \_**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) при получении данных из каталога FTP. Если этот флаг не указан или вызов осуществляется через прокси-сервер CERN, [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Возвращает HTML-версию каталога. Этот флаг используется только в функции [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также возвращает структуру [**\_ \_ данных Gopher Find**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) при получении сведений о каталоге Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**Предвыборка для чтения с \_ флагом Интернета \_ \_**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Этот флаг сейчас отключен.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_Перезагрузка флага Интернета \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Принудительно загружает запрошенный файл, объект или каталог с сервера-источника, а не из кэша. Функции [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) используют этот флаг.

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_зона Internet Flag \_ ограниченной \_ зоны**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Указывает, что заданный куки-файл связан с недоверенным сайтом.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**\_ \_ Повторная синхронизация ФЛАГа Интернета**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Перезагружает ресурсы HTTP, если ресурс был изменен с момента последней загрузки. Все ресурсы FTP перегружаются. Этот флаг может использоваться [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также используется в [**гоферфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) и [**гоферопенфиле**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), и ресурсы Gopher перегружаются.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_безопасный флаг \_ Интернета**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Использует безопасную семантику транзакций. Это означает использование технологии SSL/частной связи (SSL/PCT) и имеет смысл только в HTTP-запросах. Этот флаг используется [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) и [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), но он является избыточным, если HTTPS://отображается в URL-адресе. Функция [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует этот флаг для HTTP-соединений; Этот флаг будет унаследован всеми дескрипторами запросов, созданными при этом соединении.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**код \_ \_ ASCII для перевода с ФЛАГом Интернета \_**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Передает файл как ASCII (только FTP). Этот флаг может использоваться [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)и [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_ \_ двоичный файл передаваемых ФЛАГов Интернета \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Передает файл как двоичный (только FTP). Этот флаг может использоваться [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)и [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**\_ \_ обратный вызов через Интернет**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Указывает, что для этого API не нужно создавать обратные вызовы. Используется для параметра *дксконтекст* функций, которые позволяют выполнять асинхронные операции.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_параметр Интернета \_ подавлять \_ проверку \_ подлинности сервера**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Задает объект HTTP-запроса таким, что он не будет выполнять вход на серверы-источники, но будет автоматически входить на прокси-серверы HTTP. Этот параметр отличается от флага запроса INTERNET \_ Flag \_ без \_ проверки подлинности, что предотвращает аутентификацию как на прокси-серверах, так и на исходных серверах. Установка этого режима подавляет использование любого материала учетных данных (ранее предоставленные имя пользователя, пароль или SSL-сертификат клиента) при взаимодействии с сервером-источником. Однако если запрос должен пройти через прокси-сервер с проверкой подлинности, WinINet будет по-прежнему выполнять автоматическую проверку подлинности прокси-сервера HTTP согласно параметрам зоны интрасети для пользователя. Параметр зоны интрасети по умолчанию позволяет автоматически входить в систему, используя учетные данные пользователя по умолчанию. Чтобы предотвратить подавление всех идентифицирующих сведений, вызывающий объект должен сочетать \_ параметр \_ Internet \_ \_ AUTH Authentication с \_ флагом Internet flags \_ No \_ cookies Request. Этот параметр может быть установлен только для объектов запроса перед отправкой. Попытки установить этот параметр после отправки запроса будут возвращать сообщение об ошибке "ошибка в \_ Интернете неверный режим работы" \_ \_ \_ . Для этого параметра не требуется буфер. Он используется Интернетсетоптион для дескрипторов, возвращаемых только Хттпопенрекуест. Версия: требуется Internet Explorer 8,0 или более поздней версии.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_флаг API \_ WinInet \_ Async**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Принудительно выполняет асинхронные операции.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_ \_ Синхронизация флагов API WinInet \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Принудительно выполняет синхронные операции.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_ \_ контекст использования флага API WinInet \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Заставляет API использовать значение контекста, даже если оно равно нулю.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

