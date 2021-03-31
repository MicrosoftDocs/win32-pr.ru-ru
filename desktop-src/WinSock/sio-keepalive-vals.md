---
description: Управляющий код включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания и интервал проверки активности TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Код элемента управления SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155866"
---
# <a name="sio_keepalive_vals-control-code"></a>Код элемента управления SIO_KEEPALIVE_VALS

## <a name="description"></a>Описание

Управляющий код **\_ \_ Валс** контроля доступа SIO включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания и интервал проверки активности TCP.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Используйте **\_ \_ Валс KeepAlive** для этой операции.

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр должен указывать на структуру **TCP \_ KeepAlive** .

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр должен быть больше или равен размеру структуры **\_ KeepAlive TCP** , указанной параметром *лпвинбуффер* .

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
Этот параметр не используется для этой операции.

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.
Этот параметр должен иметь значение 0.

### <a name="lpcbbytesreturned"></a>лпкббитесретурнед

Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.
Этот возвращаемый параметр указывает на значение **DWORD** , равное нулю, для этой операции, так как выходные данные отсутствуют.

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
|**\_ожидается ввод-вывод WSA \_** | Операция перекрытия успешно инициирована, и ее завершение будет указано позже. |
| **\_Операция WSA \_ прервана** | Операция перекрытия была отменена из-за замыкания сокета или выполнения команды **IOCTL SIO_FLUSH** . |
| **WSAEFAULT** | Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | Функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокирования была прервана. |
| **всаеинвал** | Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. |
| **WSAENETDOWN** | Сбой сетевой подсистемы. |
| **всаенопротупт** | Параметр сокета не поддерживается для указанного протокола. Эта ошибка возвращается для сокета датаграммы. |
| **всаенотсокк** | Дескриптор s не является сокетом. |
| **всаеопнотсупп** | Указанная команда IOCTL не поддерживается. Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ \_ Валс ioctl суперконтроллера** ввода/вывода. |

## <a name="remarks"></a>Комментарии

В Windows 2000 и более поздних версиях операционной системы поддерживается запрос IOCTL **\_ KeepAlive \_ Валс** .

Управляющий код **\_ \_ Валс поддержки SIO** включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания проверки активности TCP и интервал, используемый для пакетов поддержания активности TCP.
Дополнительные сведения о параметре проверки активности см. в разделе 4.2.3.6 (требования для узлов Интернета) — уровни взаимодействия, указанные в RFC 1122, доступны на [веб-сайте IETF](https://www.ietf.org/rfc/rfc1122.txt).
(Этот ресурс может быть доступен только на английском языке.)

Параметр *лпвинбуффер* должен указывать на структуру **TCP \_ KeepAlive** , определенную в файле заголовка *мсткпип. h* .
Эта структура определяется следующим образом:

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

Значение, указанное в элементе **онофф** , определяет, включена или отключена проверка активности TCP.
Если для элемента **онофф** задано ненулевое значение, то поддерживается проверка активности TCP и используются другие элементы структуры.
Элемент **KeepAliveTime** указывает время ожидания (в миллисекундах) без активности, пока не будет отправлен первый пакет проверки активности.
Член **keepAliveInterval** указывает интервал (в миллисекундах) между отправкой последовательных пакетов поддержания активности, если подтверждение не получено.

Параметр [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , который является одним из [**параметров сокета SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), также может использоваться для включения или отключения проверки активности TCP в соединении, а также для запроса текущего состояния этого параметра.
Чтобы запросить, включена ли поддержка TCP-активности на сокете, функцию жетсоккопт можно вызвать с параметром [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Чтобы включить или отключить протокол TCP на активность, функцию **сетсоккопт** можно вызвать с параметром [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Если поддержка проверки активности TCP включена с [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), то параметры TCP, используемые по умолчанию, используются для времени ожидания проверки активности и интервала, если эти значения не были изменены с помощью **SIO \_ KeepAlive \_ Валс**.

Значение времени ожидания проверки активности по умолчанию для всей системы может быть управляемым с помощью параметра реестра [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , который принимает значение в миллисекундах. Если ключ не задан, время ожидания проверки активности по умолчанию составляет 2 часа.
Значение интервала проверки активности по умолчанию может быть управляемым с помощью параметра реестра [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , который принимает значение в миллисекундах. Если ключ не задан, интервал проверки активности по умолчанию равен 1 секунде.

В Windows Vista и более поздних версиях количество проверок активности (повторных передач данных) устанавливается равным 10 и не может быть изменено.

В Windows Server 2003, Windows XP и Windows 2000 параметр по умолчанию для количества проверок активности по сроку поддержания равен 5.
Количество зондов проверки активности может быть управляемым с помощью параметров реестра **TcpMaxDataRetransmissions** и [**пптпткпмаксдатаретрансмиссионс**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .
Число зондов проверки активности устанавливается равным большему из двух значений раздела реестра.
Если это число равно 0, зонды проверки активности не будут отправляться.
Если это число превышает 255, то оно корректируется на 255.

## <a name="see-also"></a>См. также раздел

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**пптпткпмаксдатаретрансмиссионс**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[фиксатор](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**всажетластеррор**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
