---
description: Управляющий код запрашивает связь между сокетом и ядром процессора RSS и узлом NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Код элемента управления SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 6c0f690555beb19f7d5d79a81e2cc900194f731c3acacb075ae12dc304debffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740386"
---
# <a name="sio_query_rss_processor_info-control-code"></a>Код элемента управления SIO_QUERY_RSS_PROCESSOR_INFO

## <a name="description"></a>Описание

Код **управления \_ \_ \_ \_ сведениями о обработчике SIO для запросов к RSS-каналу** запрашивает связь между сокетом и ядром процессора RSS и узлом NUMA.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
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
Для этой операции используйте **\_ \_ \_ \_ сведения о обработчике запросов SIO** в формате RSS.

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр не используется для этой операции.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр не используется для этой операции.

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
Этот параметр должен указывать на структуру [**\_ \_ сходства процессоров сокетов**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) , если параметры *Лповерлаппед* и *лпкомплетионраутине* имеют **значение NULL**.

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.
Этот параметр должен быть не меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .

### <a name="lpcbbytesreturned"></a>лпкббитесретурнед

Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.

Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение *DWORD* , равное нулю.

Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.

Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.
Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.
Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.

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
| **Ошибка \_ недостаточного \_ буфера** | Область данных, переданная в системный вызов, слишком мала. Эта ошибка возвращается, если буфер, на который указывает параметр *лпваутбуффер* с размером буфера, переданным в параметре *кбаутбуффер* , слишком мал. Требуемый размер буфера будет возвращен в параметре *лпкббитесретурнед* . Эта ошибка возвращается, если параметр *кбаутбуффер* меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) . |
| **\_ожидается ввод-вывод WSA \_** | Операция перекрытия успешно инициирована, и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода. |
| **WSAEFAULT** | Параметр *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | Функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокирования была прервана. |
| **всаеинвал** | Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. Эта ошибка возвращается, если параметр *кбаутбуффер* меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .
| **WSAENETDOWN** | Сбой сетевой подсистемы. |
| **всаенопротупт** | Параметр сокета не поддерживается для указанного протокола. |
| **WSAENOTCONN** | *Сокеты не* подключены. |
| **всаенотсокк** | Дескриптор *s* не является сокетом. |
| **всаеопнотсупп** | Указанная команда IOCTL не поддерживается. Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ запрос на \_ \_ \_ сведения о процессоре SIO** в формате RSS. |

## <a name="remarks"></a>Remarks

в Windows 8 и Windows Server 2012 и более поздних версиях операционной системы поддерживается **\_ запрос на \_ \_ \_ сведения о процессоре SIO** .

**\_ \_ \_ \_ Сведения о обработчике запросов SIO** в формате RSS используются для определения связи между сокетом и ядром процессора RSS и узлом NUMA.
Этот запрос IOCTL возвращает [**структуру \_ \_ соответствия процессоров сокетов**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) , которая содержит [**\_ номер процессора**](/windows/desktop/api/winnt/ns-winnt-processor_number) и идентификатор узла NUMA.
Возвращенная [**Структура \_ номеров процессоров**](/windows/desktop/api/winnt/ns-winnt-processor_number) содержит номер группы и относительный номер процессора в группе.

Если сокет является UDP-сокетом, сокет должен быть подключен для правильной работы **\_ запроса на \_ \_ \_ сведения о процессоре SIO с запросом** IOCTL.

## <a name="see-also"></a>См. также раздел

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**фиксатор**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
