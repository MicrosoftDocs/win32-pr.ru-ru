---
description: Управляющий код освобождает резервирование времени выполнения для блока портов TCP или UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Код элемента управления SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8d949e325292210ec7126da5ddf65c6ff30c5aa151cfaf85331fb7ebf3e5b346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097495"
---
# <a name="sio_release_port_reservation-control-code"></a>Код элемента управления SIO_RELEASE_PORT_RESERVATION

## <a name="description"></a>Описание

Код **управления \_ \_ \_ резервирования порта SIO** освобождает резервирование времени выполнения для блока портов TCP или UDP.
Зарезервированное время выполнения должно быть получено из процесса выдачи с помощью [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
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
Используйте для этой операции **\_ \_ \_ резервирование портов освобождения SIO** .

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр содержит указатель на структуру [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) с маркером резервирования порта TCP или UDP для освобождения.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр должен быть не меньше размера структуры [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

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
| **\_Операция WSA \_ прервана** | Операция ввода-вывода прервана из-за завершения потока или запроса приложения. Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды **SIO_FLUSH** IOCTL. |
| **WSAEFAULT** | Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове. Эта ошибка возвращается параметром *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя. |
| **всаеинпрогресс** | В данный момент выполняется блокирующая операция. Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова. |
| **всаеинтр** | Операция блокировки была прервана вызовом **всаканцелблоккингкалл**. Эта ошибка возвращается в случае прерывания блокирующей операции. |
| **всаеинвал** | Указан недопустимый аргумент. Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета. |
| **WSAENETDOWN** | Операция на сокете обнаружила отключение сети. Эта ошибка возвращается в случае сбоя сетевой подсистемы. |
| **всаенотсокк** | Предпринята попытка выполнить операцию для объекта, который не является сокетом. Эта ошибка возвращается, если дескриптор *s* не является сокетом. |
| **всаеопнотсупп** | Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка. Эта ошибка возвращается, если указанная команда IOCTL не поддерживается. Эта ошибка также возвращается, если поставщик транспорта не поддерживает запрос на **\_ \_ \_ зарезервированный номер порта освобождения SIO** . Эта ошибка также возвращается, если попытка использования ioctl **\_ \_ порта \_ выпуска SIO** выполняется на сокете, отличном от UDP или TCP. |

## <a name="remarks"></a>Remarks

в Windows Vista и более поздних версиях операционной системы поддерживается запрос на **\_ \_ \_ зарезервированный номер порта версии SIO** .

Приложения и службы, которым необходимо резервировать порты, делятся на две категории.
Первая категория включает компоненты, которым требуется определенный порт в рамках своей работы.
Такие компоненты, как правило, предпочитают указывать требуемый порт во время установки (например, в манифесте приложения).
Вторая категория включает компоненты, которым требуется любой доступный порт или блок портов во время выполнения.
Эти две категории соответствуют конкретным и запросам резервирования портов с подстановочными знаками.
Определенные запросы на резервирование могут быть постоянными или средой выполнения, тогда как запросы резервирования портов с подстановочными знаками поддерживаются только во время выполнения.

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl используется для запроса резервирования среды выполнения для блока портов TCP или UDP.
Для резервирования портов во время выполнения пул портов требует, чтобы резервирования использовались в процессе, для которого было предоставлено резервирование.
Количество резервирований портов среды выполнения последний раз, пока время существования сокета, на котором вызывался [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.
Напротив, постоянные резервирования портов, созданные с помощью функции [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) , могут быть использованы любым процессом с возможностью получения постоянных резервирований.

**\_ \_ \_ Зарезервированный номер порта освобождения SIO** используется для освобождения резервирования времени выполнения для блока портов TCP или UDP.

Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны **null**, сокет в этой функции будет рассматриваться как сокет без перекрытия.
Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.
Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.

Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.

Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.
Если приложение не допускает блокировку в вызове функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.

В следующих случаях операция IOCTL с **\_ \_ \_ зарезервированным портом SIO** может завершиться ошибкой, так как операции **всаеинтр** или **WSA \_ \_ прерываются** .

* Запрос отменяется диспетчером ввода-вывода.
* Сокет закрыт.

## <a name="examples"></a>Примеры

В следующем примере запрашивается резервирование портов среды выполнения, а затем освобождается резервирование портов среды выполнения.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>См. также

[**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**делетеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**делетеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**лукупперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**лукупперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_ASSOCIATE_PORT_RESERVATION**](sio-associate-port-reservation.md)

[фиксатор](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**всажетластеррор**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
