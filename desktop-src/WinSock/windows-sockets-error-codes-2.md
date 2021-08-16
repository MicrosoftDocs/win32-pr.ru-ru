---
description: Windows Коды ошибок сокетов (Winsock), возвращаемые функцией Всажетластеррор.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Windows Коды ошибок сокетов (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece53093e7aca31d9d883680005f92ca8b30a76120209affb4dba42d6826d0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322007"
---
# <a name="windows-sockets-error-codes"></a>Windows Коды ошибок сокетов

большинство функций сокетов Windows 2 не возвращают конкретную причину ошибки, когда функция возвращает значение. Дополнительные сведения см. в разделе [Обработка ошибок Winsock](handling-winsock-errors.md) .

Функция [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает последнюю ошибку, возникшую для вызывающего потока. если определенная функция Windows sockets указывает на возникновение ошибки, эту функцию следует вызывать немедленно, чтобы получить расширенный код ошибки для вызова функции, вызвавшей сбой. Эти коды ошибок и краткое текстовое описание, связанное с кодом ошибки, определены в файле заголовка *Winerror. h* . Функцию [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) можно использовать для получения строки сообщения для возвращенной ошибки.

Сведения о том, как выполнять обработку кодов ошибок при переносе приложений сокетов в Winsock, см. в разделе [коды ошибок — ошибки, з \_ и всажетластеррор](error-codes-errno-h-errno-and-wsagetlasterror-2.md).

В следующем списке описаны возможные коды ошибок, возвращаемые функцией [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Ошибки перечислены в числовом порядке с именем макроса ошибки. Некоторые коды ошибок, определенные в файле заголовка *Winsock2. h* , не возвращаются ни одной из функций.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Возвращаемый код и значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>Указан недопустимый обработчик объекта события.</dt> <dd> Приложение пытается использовать объект события, но указанный маркер является недопустимым.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Недостаточно доступной памяти.</dt> <dd> приложение использует функцию сокетов Windows, которая напрямую сопоставляется с Windowsной функцией. функция Windows указывает на отсутствие требуемых ресурсов памяти.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Один или несколько параметров недопустимы.</dt> <dd> приложение использует функцию сокетов Windows, которая напрямую сопоставляется с Windowsной функцией. функция Windows указывает на проблему с одним или несколькими параметрами.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Операция перекрытия прервана.</dt> <dd> Перекрывающаяся операция была отменена из-за замыкания сокета или выполнения команды SIO_FLUSH в <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>всаиоктл</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>Перекрытый объект события ввода-вывода, не являющийся сигнальным состоянием.</dt> <dd> Приложение попыталось определить состояние операции перекрытия, которая еще не завершена. Приложения, использующие <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>всажетоверлаппедресулт</strong></a> (с флагом <em>фваит</em> , имеющим значение <strong>false</strong>) в режиме опроса, чтобы определить, когда была выполнена операция перекрытия, получите этот код ошибки до завершения операции.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Перекрывающиеся операции будут выполнены позже. <br/> <dl> <dt><span></span></dt> <dd> Приложение инициировало перекрывающуюся операцию, которая не может быть закончена немедленно. Индикатор завершения будет указан позже после завершения операции.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>Всаеинтр</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Прерванный вызов функции.</dt> <dd> Операция блокировки была прервана вызовом <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">всаканцелблоккингкалл</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>Всаебадф</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>Недопустимый файловый маркер.</dt> <dd> Указан недопустимый файловый обработчик. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>Всаеакцес</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Отказано в разрешении.</dt> <dd> Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ. В качестве примера используется широковещательный адрес для функции <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> без широковещательного разрешения, установленного с помощью <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a>(SO_BROADCAST). <br/> другая возможная причина ошибки всаеакцес заключается в том, что при вызове функции <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>bind</strong></a> (в Windows NT 4,0 с пакетом обновления 4 (SP4) или более поздней версии) другой драйвер приложения, службы или режима ядра привязан к тому же адресу с эксклюзивным доступом. такой эксклюзивный доступ является новой функцией Windows NT 4,0 с пакетом обновления 4 (SP4) и более поздних версий и реализуется с помощью параметра <a href="/windows/desktop/winsock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>Всаефаулт</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Неправильный адрес.</dt> <dd> Система обнаружила недопустимый адрес указателя при попытке использования аргумента указателя вызова. Эта ошибка возникает, если приложение передает недопустимое значение указателя или длина буфера слишком мала. Например, если длина аргумента, который является структурой <a href="/windows/desktop/winsock/sockaddr-2"><strong>SOCKADDR</strong></a> , меньше, чем sizeof (SOCKADDR).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>Всаеинвал</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Недопустимый аргумент.</dt> <dd> Указан недопустимый аргумент (например, указан недопустимый уровень для функции <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> ). В некоторых случаях он также ссылается на текущее состояние сокета — например, вызов метода <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>Accept</strong></a> на сокете, который не прослушивается.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>Всаемфиле</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Слишком много открытых файлов.</dt> <dd> Слишком много открытых сокетов. Каждая реализация может иметь максимальное количество доступных дескрипторов сокетов: глобально, на один процесс или на поток.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>Всаеваулдблокк</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>Ресурс временно недоступен.</dt> <dd> Эта ошибка возвращается из операций на неблокирующих сокетах, которые не могут быть завершены немедленно, <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>например, если данные</strong></a> не помещаются в очередь для чтения из сокета. Это некритическая ошибка, и операция должна быть повторена позже. ВСАЕВАУЛДБЛОКК будет считаться результатом вызова <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> на неблокирующем сокете SOCK_STREAM, так как некоторое время должно пройти для установления соединения.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>Всаеинпрогресс</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Операция сейчас выполняется.</dt> <dd> В данный момент выполняется блокирующая операция. Windows Сокеты допускают только одну операцию блокировки (по задаче или потоку), и если какой-либо другой вызов функции выполняется (независимо от того, ссылается ли он или на какой-либо другой сокет), функция завершается с ошибкой ВСАЕИНПРОГРЕСС.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>Всаеалреади</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>Операция уже выполняется.</dt> <dd> Предпринята попытка выполнить операцию на неблокирующем сокете с уже выполняемой операцией, т. е. вызов <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>соединения</strong></a> второй раз на неблокирующем сокете, который уже подключается, или отмена асинхронного запроса (<strong>всаасинкжетксбии</strong>), который уже был отменен или завершен.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>Всаенотсокк</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Операция сокета не на сокете.</dt> <dd> Предпринята попытка выполнить операцию для объекта, который не является сокетом. Либо параметр обработчика сокета не <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>ссылается на</strong></a>допустимый сокет, либо член <strong>FD_SET</strong> является недопустимым.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>Всаедестаддррек</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Требуется адрес назначения.</dt> <dd> В операции на сокете пропущен требуемый адрес. Например, эта ошибка возвращается, если метод <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> вызывается с удаленным адресом ADDR_ANY.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>Всаемсгсизе</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Слишком длинное сообщение.</dt> <dd> Сообщение, отправленное на сокете датаграмм, было больше, чем внутренний буфер сообщений или какое-либо другое ограничение сети, либо буфер, используемый для получения датаграммы, меньше, чем сама датаграмма.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>Всаепрототипе</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Неправильный тип протокола для сокета.</dt> <dd> В вызове функции <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>сокета</strong></a> указан протокол, не поддерживающий семантику запрошенного типа сокета. Например, протокол ARPA Интернет UDP не может быть указан с типом сокета SOCK_STREAM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>Всаенопротупт</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Неверный параметр протокола.</dt> <dd> В вызове <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>жетсоккопт</strong></a> или <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> был указан неизвестный, недопустимый или неподдерживаемый параметр или уровень.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>Всаепротоносуппорт</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Протокол не поддерживается.</dt> <dd> Запрошенный протокол не был настроен в системе или для него не существует реализации. Например, вызов <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>сокета</strong></a> запрашивает сокет SOCK_DGRAM, но указывает протокол потока.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>Всаесокктносуппорт</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Тип сокета не поддерживается.</dt> <dd> Указанный тип сокета не поддерживается в данном семействе адресов. Например, необязательный тип SOCK_RAW можно выбрать в вызове <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>сокета</strong></a> , и реализация не поддерживает сокеты SOCK_RAW.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>Всаеопнотсупп</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Операция не поддерживается.</dt> <dd> Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка. Обычно это происходит, когда дескриптор сокета для сокета, который не поддерживает эту операцию, пытается принять соединение на сокете датаграммы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>Всаепфносуппорт</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Семейство протоколов не поддерживается.</dt> <dd> Семейство протоколов не было настроено в системе или не существует реализации для него. Это сообщение имеет немного отличающееся значение от ВСАЕАФНОСУППОРТ. однако в большинстве случаев он является взаимозаменяемым, и все функции Windows sockets, возвращающие одно из этих сообщений, также указывают всаеафносуппорт.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>Всаеафносуппорт</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Семейство адресов не поддерживается семейством протоколов.</dt> <dd> Использован адрес, несовместимый с запрошенным протоколом. Все сокеты создаются со связанным семейством адресов (то есть AF_INET для протоколов Интернета) и общим типом протокола (SOCK_STREAM). Эта ошибка возвращается, если неверно запрашивается неправильный протокол в вызове <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>сокета</strong></a> или если для сокета используется адрес неправильного семейства, например в функции <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>Всаеаддринусе</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>Адрес уже используется.</dt> <dd> Обычно допускается только одно использование каждого адреса сокета (протокол/IP-адрес/порт). Эта ошибка возникает, если приложение пытается <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>привязать</strong></a> сокет к IP-адресу или порту, который уже использовался для существующего сокета, или к сокету, который не был закрыт должным образом, или к одному, который еще находится в процессе закрытия. Для серверных приложений, которым необходимо <strong>привязать</strong> несколько сокетов к одному и тому же номеру порта, рассмотрите возможность использования <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> (SO_REUSEADDR). Как правило, клиентским приложениям не требуется вызывать <strong>привязку</strong> —<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Подключение</strong></a> выбирает неиспользуемый порт автоматически. Когда <strong>BIND</strong> вызывается с подстановочным адресом (включающим ADDR_ANY), ошибка всаеаддринусе может быть отложена до тех пор, пока не зафиксирован указанный адрес. Это может произойти при вызове другой функции позже, включая <strong>Connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>Listen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>всаконнект</strong></a>или <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>всажоинлеаф</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>Всаеаддрнотаваил</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>Не удается назначить запрошенный адрес.</dt> <dd> Запрошенный адрес недопустим в своем контексте. Это обычно приводит к попытке <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>привязки</strong></a> к адресу, который не является допустимым для локального компьютера. Это также может быть вызвано <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>подключением</strong></a>, <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>всаконнект</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>всажоинлеаф</strong></a>или <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>всасендто</strong></a> , если удаленный адрес или порт недействителен для удаленного компьютера (например, адреса или порта 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>Всаенетдовн</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>Сеть не работает.</dt> <dd> Операция на сокете обнаружила отключение сети. Это может указывать на серьезные сбои в системе сети (стеке протоколов, на основе которого работает библиотека DLL Windows Sockets), интерфейсе сети или в самой локальной сети.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>Всаенетунреач</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>Сеть недоступна.</dt> <dd> Операция сокета была предпринята к недостижимой сети. Обычно это означает, что локальное программное обеспечение не имеет маршрута, чтобы связаться с удаленным узлом.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>Всаенетресет</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>Сетевое подключение разорвано при сбросе.</dt> <dd> Соединение разорвано из-за того, что операция проверки активности обнаруживает сбой во время выполнения операции. Его также можно вернуть с помощью <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> , если предпринимается попытка установить <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> для соединения, которое уже завершилось сбоем.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>Всаеконнабортед</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>Программное обеспечение привело к прерыванию подключения.</dt> <dd> Установленное подключение прервано программным обеспечением на главном компьютере, возможно, из-за истечения времени ожидания передачи данных или ошибки протокола.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>Всаеконнресет</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Сброс соединения по одноранговому узлу.</dt> <dd> существующее соединение было принудительно завершено удаленным узлом. Это обычно происходит, если однорангическое приложение на удаленном узле внезапно остановлено, узел перезагружается, узел или удаленный сетевой интерфейс отключены, или удаленный узел использует жесткое закрытие (см. <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> для получения дополнительных сведений о параметре SO_LINGER на удаленном сокете). Эта ошибка также может возникнуть, если подключение разорвано из-за активности проверки активности, когда выполняется одна или несколько операций. Выполняемые операции завершились ошибкой с ВСАЕНЕТРЕСЕТ. Последующие операции завершаются сбоем с ВСАЕКОННРЕСЕТ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>Всаенобуфс</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>Нет доступного места в буфере.</dt> <dd> Не удалось выполнить операцию с сокетом, так как в системе недостаточно места в буфере или из-за переполнения очереди.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>Всаеисконн</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>Сокет уже подключен.</dt> <dd> Запрос на подключение был сделан на уже подключенном сокете. Некоторые реализации также возвращают эту ошибку, если метод <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> вызывается для подключенного SOCK_DGRAM сокета (для SOCK_STREAM сокетах параметр <em>to</em> в <strong>SendTo</strong> не учитывается), хотя другие реализации считают это допустимым.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>Всаенотконн</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>Сокет не подключен.</dt> <dd> Запрос на отправку или получение данных запрещен, так как сокет не подключен и (при отправке через сокет датаграмм с помощью <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>) адрес не указан. Любой другой тип операции также может возвратить эту ошибку, например <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>сетсоккопт</strong></a> , если соединение было сброшено.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>Всаешутдовн</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>Не удается отправить после завершения работы сокета.</dt> <dd> Запрос на отправку или получение данных запрещен, так как работа сокета уже была завершена в этом направлении с предыдущим вызовом <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>завершения работы</strong></a> . Вызывая <strong>Завершение работы</strong> , вы запрашиваете частичное замыкание сокета, которое является сигналом, который отправляет или получает или что больше не поддерживается.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>Всаетуманирефс</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Слишком много ссылок.</dt> <dd> Слишком много ссылок на некоторый объект ядра.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>Всаетимедаут</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Истекло время ожидания подключения.</dt> <dd> Попытка подключения не удалась, так как подключенная сторона не ответила должным образом по истечении определенного периода времени или не удалось установить соединение, так как подключенный узел не ответил.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>Всаеконнрефусед</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Подключение отклонено.</dt> <dd> Не удалось установить подключение, так как конечный компьютер отказался от него. Это обычно происходит при попытке подключиться к службе, которая неактивна на внешнем узле, то есть в том случае, если серверное приложение не работает.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>Всаелуп</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>Не удается преобразовать имя.</dt> <dd> Не удается преобразовать имя.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>Всаенаметулонг</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Слишком длинное имя.</dt> <dd> Имя компонента или имени слишком длинное.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>Всаехостдовн</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>Узел не работает.</dt> <dd> Сбой операции сокета, так как целевой узел не работает. Операция сокета обнаружила неработающий узел. Не запущена сетевая активность на локальном узле. Эти условия скорее всего помечаются ошибкой ВСАЕТИМЕДАУТ.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>Всаехостунреач</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>Нет маршрута к узлу.</dt> <dd> Сделана попытка выполнить операцию на сокете для недоступного хоста. См. ВСАЕНЕТУНРЕАЧ.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>Всаенотемпти</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>Каталог не пуст.</dt> <dd> Невозможно удалить каталог, который не является пустым.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>Всаепроклим</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Слишком много процессов.</dt> <dd> реализация Windowsных сокетов может иметь ограничение на количество приложений, которые могут использовать его одновременно. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>Сбой WSAStartup</strong></a> может завершиться с этой ошибкой, если достигнут предел.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>Всаеусерс</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>Превышена квота пользователя.</dt> <dd> Исчерпана квота пользователя. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>Всаедкуот</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Превышена квота диска.</dt> <dd> Дисковая квота исчерпана. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>Всаестале</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Ссылка на устаревший файловый обработчик.</dt> <dd> Ссылка на обработчик файлов больше недоступна. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>Всаеремоте</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>Элемент является удаленным.</dt> <dd> Элемент недоступен локально. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>Всасиснотреади</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>Сетевая подсистема недоступна.</dt> <dd> эта ошибка возвращается функцией <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>сбой wsastartup</strong></a> , если в настоящее время не удается выполнить реализацию сокетов Windows, так как базовая система, используемая для предоставления сетевых служб, в данный момент недоступна. Пользователи должны проверить следующее:<br/> </dd> </dl>
<ul>
<li>, что соответствующий DLL-файл Windows sockets находится в текущем пути.</li>
<li>что они не пытаются одновременно использовать более одной реализации Windows сокетов. Если в системе имеется несколько DLL-библиотек Winsock, убедитесь, что первая из них подходит для сетевой подсистемы, загруженной в данный момент.</li>
<li>документация по реализации сокетов Windows, чтобы убедиться в том, что все необходимые компоненты установлены и правильно настроены.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>Всавернотсуппортед</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span> ВерсияWinsock.dll вне допустимого диапазона.</dt> <dd> текущая реализация Windowsных сокетов не поддерживает версию спецификации Windowsных сокетов, запрошенную приложением. Убедитесь, что программа не обращается к старым версиям файлов DLL Windows Sockets.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>Всанотинитиалисед</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>Успешное выполнение сбой WSAStartup еще не выполнено.</dt> <dd> Приложение не вызвало <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>сбой WSAStartup</strong></a> или <strong>сбой WSAStartup</strong> . Приложение может получить доступ к сокету, владельцем которого является текущая активная задача (то есть при попытке совместного использования сокета между задачами), или <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>всаклеануп</strong></a> был вызван слишком много раз.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>Всаедискон</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Выполняется корректное завершение работы.</dt> <dd> Возвращается <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>всарекв</strong></a> и <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>всареквфром</strong></a> , чтобы указать, что удаленная сторона запустила последовательность корректного завершения работы.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>Всаеноморе</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Больше нет результатов.</dt> <dd> Функция <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>всалукупсервиценекст</strong></a> не может вернуть дополнительные результаты.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>Всаеканцеллед</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>Вызов отменен.</dt> <dd> Вызов функции <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>всалукупсервицеенд</strong></a> был выполнен, пока этот вызов все еще обрабатывается. Вызов отменен.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>Всаеинвалидпроктабле</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>Недопустимая таблица вызовов процедур.</dt> <dd> Недопустимая таблица вызова процедуры поставщика услуг. Поставщик услуг вернул фиктивную таблицу процедур для Ws2_32.dll. Обычно это вызвано тем, что один или несколько указателей функций <strong>имеют значение NULL</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>Всаеинвалидпровидер</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>Недопустимый поставщик услуг.</dt> <dd> Запрошенный поставщик услуг недопустим. Эта ошибка возвращается функциями <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>вскжетпровидеринфо</strong></a> и <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> , если не удалось найти указанную запись протокола. Эта ошибка также возвращается, если поставщик услуг возвратил номер версии, отличный от 2,0.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>Всаепровидерфаилединит</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>Не удалось инициализировать поставщик услуг.</dt> <dd> Не удалось загрузить или инициализировать запрошенного поставщика услуг. Эта ошибка возвращается, если не удалось загрузить библиотеку DLL поставщика услуг (сбой<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> ) или не удалось выполнить <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>Вспстартуп</strong></a> или функцию <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>нспстартуп</strong></a> поставщика.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>Всасискаллфаилуре</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Сбой системного вызова.</dt> <dd> Неудачный вызов системного вызова, который не должен быть успешным. Это универсальный код ошибки, возвращаемый при различных условиях. <br/> Возвращается, когда системный вызов, который не должен завершаться ошибкой, завершается ошибкой. Например, если вызов <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>ваитформултипливентс</strong></a> завершается ошибкой или одна из функций реестра не может работать с каталогами протокола или пространства имен.<br/> Возвращается, когда поставщик не возвращает результат и не предоставляет расширенный код ошибки. Может указывать на ошибку реализации поставщика услуг.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>Служба не найдена.</dt> <dd> Такая служба неизвестна. Не удается найти службу в указанном пространстве имен.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>Тип класса не найден.</dt> <dd> Указанный класс не найден.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Больше нет результатов.</dt> <dd> Функция <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>всалукупсервиценекст</strong></a> не может вернуть дополнительные результаты.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>Вызов отменен.</dt> <dd> Вызов функции <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>всалукупсервицеенд</strong></a> был выполнен, пока этот вызов все еще обрабатывается. Вызов отменен.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>Всаерефусед</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>Запрос к базе данных отклонен.</dt> <dd> Запрос к базе данных не выполнен из-за того, что он был активно отклонен.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>Узел не найден.</dt> <dd> Такой узел не существует. Имя не является официальным именем узла или псевдонимом или не может быть найдено в запрашиваемых базах данных. Эта ошибка также может возвращаться для запросов протокола и службы и означает, что указанное имя не найдено в соответствующей базе данных.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>Неполномочный узел не найден.</dt> <dd> Обычно это временная ошибка во время разрешения имени узла и означает, что локальный сервер не получил ответ от полномочного сервера. Возможно, повторная попытка через некоторое время будет успешной.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Это неустранимая ошибка.</dt> <dd> Это означает, что во время уточняющего запроса базы данных произошла неустранимая ошибка. Это может быть вызвано тем, что не удалось найти файлы базы данных (например, файлы узлов, службы или ПРОТОКОЛы, совместимые с BSD), или запрос DNS был возвращен сервером с серьезной ошибкой.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Допустимое имя, нет записи данных запрошенного типа.</dt> <dd> Запрошенное имя является допустимым и найдено в базе данных, но для него не разрешены соответствующие данные. Обычным примером для этого является попытка преобразования имени узла в адрес (с помощью <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> или <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>всаасинкжесостбинаме</strong></a>), которая использует DNS (сервер доменных имен). Возвращается запись MX, но отсутствует запись, указывающая, что сам узел существует, но недоступен напрямую.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>Получатели QoS.</dt> <dd> Получен по крайней мере один резерв качества обслуживания.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>Отправители QoS.</dt> <dd> Получен по крайней мере один путь отправки QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Нет отправителя QoS.</dt> <dd> Отправители QoS отсутствуют.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>Служба QoS не имеет получателей.</dt> <dd> Нет получателей QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>Запрос на качество обслуживания подтвержден.</dt> <dd> Запрос на резервирование QoS подтвержден.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>Ошибка при допуске QoS.</dt> <dd> Произошла ошибка QoS из-за нехватки ресурсов.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>Сбой политики качества обслуживания.</dt> <dd> Запрос QoS был отклонен, так как система политики не смогла выделить запрошенный ресурс в существующей политике. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Неправильный стиль качества обслуживания.</dt> <dd> Обнаружен неизвестный или конфликтующий стиль QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Недопустимый объект QoS.</dt> <dd> Обнаружена проблема в некоторых частях филтерспек или в общем буфере конкретного поставщика.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>Ошибка управления трафиком QoS.</dt> <dd> Ошибка в API базового управления трафиком (TC), так как универсальный запрос QoS был преобразован для локального применения с помощью API TC. Это может быть вызвано ошибкой нехватки памяти или внутренней ошибкой поставщика QoS. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Общая ошибка QoS.</dt> <dd> Общая ошибка QoS.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>Ошибка типа службы QoS.</dt> <dd> В фловспек QoS обнаружен недопустимый или Нераспознанный тип службы.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>Ошибка QoS фловспек.</dt> <dd> В структуре <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QoS</strong></a> обнаружена недопустимая или нераспознанная фловспек.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Недопустимый буфер поставщика качества обслуживания.</dt> <dd> Недопустимый буфер, зависящий от поставщика QoS.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Недопустимый стиль фильтра качества обслуживания.</dt> <dd> Использован недопустимый стиль фильтра качества обслуживания.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Недопустимый тип фильтра качества обслуживания.</dt> <dd> Использован недопустимый тип фильтра качества обслуживания.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Неверное количество фильтров QoS.</dt> <dd> В ФЛОВДЕСКРИПТОР указано неверное число Филтерспекс качества обслуживания.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Недопустимая длина объекта качества обслуживания.</dt> <dd> В буфере, зависящем от поставщика QoS, был указан объект с недопустимым полем Обжектленгс.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Неверное количество потоков качества обслуживания.</dt> <dd> В структуре QoS задано неверное число дескрипторов потока.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Нераспознанный объект QoS.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружен нераспознанный объект.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Недопустимый объект политики качества обслуживания.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружен недопустимый объект политики.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Недопустимый дескриптор потока качества обслуживания.</dt> <dd> В списке дескрипторов потока обнаружен недопустимый дескриптор потока качества обслуживания.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>Недопустимый фловспек, зависящий от поставщика QoS.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружено недопустимое или непротиворечивое фловспек.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>Недопустимый филтерспек, зависящий от поставщика QoS.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружен недопустимый ФИЛТЕРСПЕК.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Недопустимый объект режима отклонения фигуры качества обслуживания.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружен недопустимый объект режима удаления фигуры.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Недопустимый объект частоты формирования качества обслуживания.</dt> <dd> В буфере, зависящем от поставщика QoS, обнаружен недопустимый объект частоты формирования.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>Зарезервированный тип элемента QoS политики.</dt> <dd> Зарезервированный элемент политики обнаружен в буфере, зависящем от поставщика QoS.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Winsock2. h; </dt> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды ошибок — код возврата, h \_ и всажетластеррор](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Обработка ошибок Winsock](handling-winsock-errors.md)
</dt> <dt>

[**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
