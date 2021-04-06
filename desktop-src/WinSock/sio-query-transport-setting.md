---
description: Управляющий код запрашивает параметры транспорта на сокете.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: Код элемента управления SIO_QUERY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898573"
---
# <a name="sio_query_transport_setting-control-code"></a>Код элемента управления SIO_QUERY_TRANSPORT_SETTING

## <a name="description"></a>Описание

Управляющий код **\_ \_ \_ параметров транспорта запросов SIO** запрашивает параметры транспорта на сокете.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
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
Используйте **\_ \_ \_ параметр транспорта запросов SIO** для этой операции.

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр содержит указатель на структуру, в которой первый элемент структуры является [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) структурой, определяющей, какой параметр транспорта запрашивается.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр зависит от параметра транспорта, к которому выполняется запрос.

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
Этот параметр зависит от параметра транспорта, который запрашивается, если параметры *лповерлаппед* и *Лпкомплетионраутине* имеют **значение NULL**.

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.

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
| **Ошибка \_ недостаточного \_ буфера** | Область данных, переданная в системный вызов, слишком мала. Эта ошибка возвращается, если буфер, на который указывает параметр *лпваутбуффер* с размером буфера, переданным в параметре *кбаутбуффер* , слишком мал. Требуемый размер буфера будет возвращен в параметре *лпкббитесретурнед* . |
| **\_ожидается ввод-вывод WSA \_** | Операция перекрытия успешно инициирована, и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода. |
| **WSAEFAULT** | Параметр *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* полностью не содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | Функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокирования была прервана. |
| **всаеинвал** | Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. |
| **WSAENETDOWN** | Сбой сетевой подсистемы. |
| **всаенопротупт** | Параметр сокета не поддерживается для указанного протокола. |
| **WSAENOTCONN** | Сокеты не подключены. |
| **всаенотсокк** | Дескриптор s не является сокетом. |
| **всаеопнотсупп** | Указанная команда IOCTL не поддерживается. Эта ошибка возвращается, если **\_ \_ \_ параметр транспорта запросов SIO** не поддерживается поставщиком транспорта. |

## <a name="remarks"></a>Комментарии

**\_ \_ \_ Параметр транспорта запросов SIO** поддерживается в windows 8, Windows Server 2012 и более поздних версиях операционной системы.

**\_ \_ \_ Параметр передачи запросов SIO** — это универсальный запрос IOCTL, используемый для запроса параметров транспорта на сокете.
Запрашиваемый параметр транспорта основан на [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* .

Единственным параметром транспорта, который сейчас определяет, является возможность получения **\_ \_ уведомлений \_ в режиме реального времени** на сокете TCP.

Если в [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* , для элемента GUID задана **\_ \_ \_ возможность уведомления в режиме реального времени**, это запрос на запрос параметров уведомлений в режиме реального времени для сокета TCP, используемого с [**Контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) , для получения фоновых сетевых уведомлений в приложении Магазина Windows.
Параметр *лпвинбуффер* должен указывать на структуру [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .
Параметр *лпваутбуффер* должен указывать на **\_ \_ \_ \_ выходную структуру параметра уведомления в режиме реального времени** .
Этот параметр транспорта применяется только к сокетам TCP.
Этот параметр транспорта предоставляет WinInet или подобным сетевым службам запрос на заданный TCP-сокет для определения состояния [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .
Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.
При успешном вызове [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **ВСПИОКТЛ** этот запрос IOCTL возвращает **\_ \_ \_ \_ выходную структуру параметра уведомления в режиме реального времени** с текущим состоянием.

**\_ \_ \_ Параметр передачи запросов SIO** позволяет службе WinInet или подобным сетевым службам запрашивать состояние параметра транспорта для данного TCP-сокета, чтобы определить, включен ли [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) на сокете.
Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.

Этот запрос IOCTL применяется только к сокетам TCP.

## <a name="see-also"></a>См. также раздел

[**CONTROL_CHANNEL_TRIGGER_STATUS**](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[**SIO_APPLY_TRANSPORT_SETTING**](sio-apply-transport-setting.md)

[фиксатор](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**всажетластеррор**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
