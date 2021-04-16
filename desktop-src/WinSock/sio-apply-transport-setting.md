---
description: Управляющий код применяет один или несколько параметров транспорта к сокету.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Код элемента управления SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719460"
---
# <a name="sio_apply_transport_setting-control-code"></a>Код элемента управления SIO_APPLY_TRANSPORT_SETTING

## <a name="description"></a>Описание

Контрольный код для **\_ применения \_ \_ параметров транспорта** применяет один или несколько параметров транспорта к сокету.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
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
Используйте для этой операции **\_ \_ \_ параметр транспорта, применяемый SIO** .

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр содержит указатель на структуру, в которой первый элемент структуры является [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) структурой, определяющей, какой параметр транспорта применяется.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр зависит от применяемого параметра транспорта.

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
Этот параметр зависит от применяемого параметра транспорта.

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
|**\_ожидается ввод-вывод WSA \_** | Выполняется перекрывающаяся операция ввода-вывода. Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Операция ввода-вывода прервана из-за завершения потока или запроса приложения. Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода. |
| **WSAEFAULT** | Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове. Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | В данный момент выполняется блокирующая операция. Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокировки была прервана вызовом [**всаканцелблоккингкалл**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Эта ошибка возвращается в случае прерывания блокирующей операции. |
| **всаеинвал** | Указан недопустимый аргумент. Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. |
| **WSAENETDOWN** | Операция на сокете обнаружила отключение сети. Эта ошибка возвращается в случае сбоя сетевой подсистемы. |
| **всаенотсокк** | Предпринята попытка выполнить операцию для объекта, который не является сокетом. Эта ошибка возвращается, если дескриптор *s* не является сокетом. |
| **всаеопнотсупп** | Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка. Эта ошибка возвращается, если указанная команда IOCTL не поддерживается. Эта ошибка также возвращается в том случае, если **\_ \_ \_ Параметры транспорта, применяемые SIO** , не поддерживаются поставщиком транспорта. Эта ошибка также возвращается, если попытка использовать **\_ \_ \_ параметр транспорта, применяемого через SIO** , выполняется на сокете, отличном от UDP или TCP. |

## <a name="remarks"></a>Комментарии

**\_ \_ \_ Параметры транспорта, применяемые SIO** , поддерживаются в windows 8, Windows Server 2012 и более поздних версиях операционной системы.

**\_ \_ \_ Параметры транспорта, применяемые SIO** , — это универсальный запрос IOCTL, используемый для применения параметра транспорта к сокету.
Применяемый параметр транспорта основан на [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* .

Начиная с Windows 8 и Windows Server 2012, система определяет **REAL_TIME_NOTIFICATION_CAPABILITYную** возможность на сокете TCP.
Начиная с Windows 10 и Windows Server 2016, также определяется **\_ \_ контекст связывания намерес** .
Дополнительные сведения см. в разделе [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).

Если в [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре лпвинбуффер, для элемента GUID задана **\_ \_ \_ возможность уведомления в режиме реального времени**, это запрос на применение параметров уведомлений в режиме реального времени для сокета TCP, используемого вместе с [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) для получения уведомлений в фоновом режиме в приложении Магазина Windows.
Параметр *лпвинбуффер* должен указывать на структуру **REAL_TIME_NOTIFICATION_SETTING_INPUT** .
Параметр *лпваутбуффер* не используется для этой операции.
Этот параметр транспорта применяется только к сокетам TCP.
Этот параметр транспорта позволяет WinInet или подобным сетевым службам пометить заданный сокет TCP как включенный [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .
Windows пометит соответствующий сокет TCP и настроит соответствующие параметры оборудования и программного обеспечения при вызове этого параметра.
Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.

## <a name="see-also"></a>См. также раздел

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[фиксатор](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SIO_QUERY_TRANSPORT_SETTING**](sio-query-transport-setting.md)

[**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
