---
description: Управляющий код, который настраивает начальные параметры времени ожидания повторной передачи (RTO) на сокете.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Код элемента управления SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "104488472"
---
# <a name="sio_tcp_initial_rto-control-code"></a>Код элемента управления SIO_TCP_INITIAL_RTO

## <a name="description"></a>Описание

Код элемента управления **SIO_TCP_INITIAL_RTO** настраивает начальные параметры времени ожидания повторной передачи (RTO) на сокете.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
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
Для этой операции используйте **SIO_TCP_INITIAL_RTO** .

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр содержит указатель на [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) , связанный с сокетом.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
Этот параметр не используется для этой операции.

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.
Этот параметр должен иметь значение 0.

### <a name="lpcbbytesreturned"></a>лпкббитесретурнед

Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.

Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.

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

Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.

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
| **\_ожидается ввод-вывод WSA \_** | Выполняется перекрывающаяся операция ввода-вывода. Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Операция ввода-вывода прервана из-за завершения потока или запроса приложения. Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода. |
| **всаеакцес** | Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ. Эта ошибка возникает при нескольких условиях, которые включают следующее: у пользователя отсутствуют необходимые права администратора на локальном компьютере, или приложение не работает в расширенной оболочке как встроенное администратор ( `RunAs administrator` ). |
| **WSAEFAULT** | Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове. Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | В данный момент выполняется блокирующая операция. Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокировки была прервана вызовом *всаканцелблоккингкалл*. Эта ошибка возвращается в случае прерывания блокирующей операции. |
| **всаеинвал** | Указан недопустимый аргумент. Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. |
| **WSAENETDOWN** | Операция на сокете обнаружила отключение сети. Эта ошибка возвращается в случае сбоя сетевой подсистемы. |
| **всаенотсокк** | Предпринята попытка выполнить операцию для объекта, который не является сокетом. Эта ошибка возвращается, если дескриптор s не является сокетом. |
| **всаеопнотсупп** | Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка. Эта ошибка возвращается, если указанная команда IOCTL не поддерживается. Эта ошибка также возвращается, если **SIO_TCP_INITIAL_RTO** ioctl не поддерживается поставщиком транспорта. |

## <a name="remarks"></a>Комментарии

Приложение может использовать **SIO_TCP_INITIAL_RTO** IOCTL для управления начальными характеристиками повторной передачи (SYN/SYN + ACK) СОКЕТа TCP, если это необходимо.
Приложение при использовании этого параметра должно предоставлять подходящие значения перед началом попытки подключения TCP к сокету.

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) ioctl позволяет приложению настроить начальное время ожидания повторной отправки (SYN), используемое сокетом.

Указатель на структуру [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) , переданную в параметре *лпвинбуффер* , позволяет приложению настроить начальное время кругового пути (RTT), используемое для расчета времени ожидания повторной передачи.
Кроме того, приложение может настроить число повторных передач, которые будут выполняться до сбоя попытки подключения.

## <a name="see-also"></a>См. также раздел

[фиксатор](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[**всажетластеррор**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
