---
description: Код элемента управления получает список локальных транспортных адресов семейства протоколов сокета, к которому может быть привязано приложение.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Код элемента управления SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097534"
---
# <a name="sio_address_list_query-control-code"></a>Код элемента управления SIO_ADDRESS_LIST_QUERY

## <a name="description"></a>Описание

Код элемента управления **\_ \_ \_ запросом списка адресов SIO** получает список локальных транспортных адресов семейства протоколов сокетов, к которым может быть привязано приложение.
Список адресов зависит от семейства адресов, а некоторые адреса исключаются из списка.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Параметры

### <a name="s"></a>s

Дескриптор, идентифицирующий сокет.

### <a name="dwiocontrolcode"></a>двиоконтролкоде

Управляющий код для операции.
Используйте **\_ \_ \_ запрос списка адресов SIO** для этой операции.

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр не используется для этой операции.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр не используется для этой операции.

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.

### <a name="lpcbbytesreturned"></a>лпкббитесретурнед

Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.

### <a name="lpvoverlapped"></a>лпвоверлаппед

Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.

Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.
В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.
В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.

### <a name="lpcompletionroutine"></a>лпкомплетионраутине

Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).

### <a name="lpthreadid"></a>лпсреадид

Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.

**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .

### <a name="lperrno"></a>лперрно

Указатель на код ошибки.

**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .

## <a name="return-value"></a>Возвращаемое значение

Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.

Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.
Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Код ошибки | Значение |
|------------|---------|
| **\_ожидается ввод-вывод WSA \_** | Операция перекрытия успешно инициирована, и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода. |
| **WSAEFAULT** | Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | Функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокирования была прервана. |
| **всаеинвал** | Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. Эта ошибка возвращается, если параметр *кбинбуффер* не имеет значение **null**. |
| **WSAENETDOWN** | Сбой сетевой подсистемы. |
| **WSAENOBUFS** | Нет доступного места в буфере. |
| **всаенопротупт** | Параметр сокета не поддерживается для указанного протокола. |
| **всаенотсокк** | Дескриптор *s* не является сокетом. |
| **всаеопнотсупп** | Указанная команда IOCTL не поддерживается. Эта ошибка возвращается, если поставщик транспорта не поддерживает **\_ \_ \_ запрос списка адресов SIO** . |

## <a name="remarks"></a>Remarks

**запрос IOCTL \_ \_ списка адресов \_ SIO** поддерживается в Windows 2000 и более поздних версиях операционной системы.

Код элемента управления **\_ \_ \_ запросом списка адресов SIO** получает список локальных транспортных адресов семейства протоколов сокетов, к которым может быть привязано приложение.
Список адресов зависит от семейства адресов.

Для \_ семейства адресов AF INET6 все адреса возвращаются, за исключением следующих:

* Любой IP-адрес, в котором состояние обнаружения повторяющихся адресов (отец) не Ипдадстатепреферред.
* Любой IP-адрес с уровнем области ниже Скопелевелсубнет в интерфейсе, где тип интерфейса — это **\_ тип \_ \_ замыкания на себя программного обеспечения**.
Это означает, что локальные ссылки (FE80: *) и замыкание (:: 1) используются в интерфейсах, **Если тип \_ \_ \_ замыкания на себя** не исключается, но не в том случае, если эти адреса находятся в интерфейсе с другим типом.

Для семейства адресов **AF \_ inet** все адреса возвращаются, за исключением следующих:

* Любой IP-адрес, в котором состояние обнаружения повторяющихся адресов (отец) не Ипдадстатепреферред.
* Любой IP-адрес в интерфейсе с типом интерфейса, **Если \_ тип \_ " \_ замыкание на себя** " и "ссылка" является локальным.
Это означает, что локальные адреса (169,254.*) и замыкание на себя (127.*) используются в интерфейсах, **Если тип \_ \_ \_ замыкания на себя** не исключается, но не в том случае, если эти адреса находятся в интерфейсе с другим типом.

Дополнительные сведения о состоянии "отец" см. в документации вспомогательной функции IP в разделе Перечисление [**\_ \_ состояния IP**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) -адресов и [**\_ \_ \_ адрес одноадресной рассылки IP-адаптера**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) и в документации MIB по структуре [**\_ \_ строк MIB уникастипаддресс**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .
Дополнительные сведения о типе интерфейса см. в документации вспомогательной функции IP на странице Структура [**\_ \_ адресов IP-адаптеров**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) , а также в разделе [**жетадаптерсаддрессес**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) и документации MIB по структуре [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) .
Дополнительные сведения об уровне области см. в документации вспомогательной функции IP на [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) структуре и перечислении [**\_ уровня области**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .

Список, возвращенный в выходном буфере, на который указывает параметр *лпваутбуффер* , представлен в виде [**структуры \_ \_ списка адресов сокета**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .

Если выходной буфер, указанный в параметре *лпваутбуффер* , недостаточно велик для хранения списка адресов, то в результате выполнения этого ioctl возвращается **\_ Ошибка сокета** , а [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [всаефаулт](windows-sockets-error-codes-2.md).
Необходимый размер (в байтах) выходного буфера возвращается в параметре *лпкббитесретурнед* в этом случае.
Примечание. код ошибки [всаефаулт](windows-sockets-error-codes-2.md) также возвращается, если параметр *лпвинбуффер*, *лпваутбуффер* или *лпкббитесретурнед* не полностью содержится в допустимой части адресного пространства пользователя.

**\_ \_ \_ Запрос списка адресов SIO** обычно вызывается синхронно с параметром *лпвоверлаппед* , имеющим значение **null**, так как список адресов возвращается немедленно.

**Примечание** .  в Windows средах Plug-n-Play адреса можно добавлять и удалять динамически.
Поэтому приложения не могут полагаться на сведения, возвращаемые **\_ \_ \_ запросом списка адресов SIO** , как постоянные.
Приложения могут регистрироваться для получения уведомлений об изменении адреса через **\_ список адресов SIO \_ \_ изменение** ioctl, который обеспечивает уведомление с помощью перекрывающихся операций ввода-вывода или события **\_ \_ \_ изменения списка адресов** .
Чтобы гарантировать, что приложение всегда имеет текущие сведения о списке адресов, можно использовать следующую последовательность действий.

* Выдача IOCTL с **\_ \_ \_ изменением списка адресов SIO**
* Выдача **\_ запроса IOCTL \_ списка \_ адресов SIO**
* Всякий раз, когда вызов IOCTL на **\_ \_ \_ изменение списка адресов SIO** уведомляет приложение об изменении списка адресов (через перекрывающиеся операции ввода-вывода или с помощью сигнализации о событии **\_ \_ \_ изменения списка адресов** ), должна повторяться вся последовательность действий.

в пакете Microsoft Windows Software Development Kit (SDK), выпущенном для Windows Vista и более поздних версий, была изменена организация файлов заголовков, а код контроля **\_ \_ \_ запросов в списке адресов SIO** определен в файле заголовка *Ws2def. h* .
Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.

## <a name="see-also"></a>См. также

[**жетадаптерсаддрессес**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**фиксатор**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
