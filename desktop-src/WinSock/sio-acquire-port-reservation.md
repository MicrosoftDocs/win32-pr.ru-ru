---
description: Управляющий код получает резервирование во время выполнения для блока портов TCP или UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Код элемента управления SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719476"
---
# <a name="sio_acquire_port_reservation-control-code"></a>Код элемента управления SIO_ACQUIRE_PORT_RESERVATION

## <a name="description"></a>Описание

Контрольный код для **\_ \_ \_ резервирования порта SIO** получает резервирование во время выполнения для блока портов TCP или UDP.

Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
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
Для этой операции используйте для **\_ получения \_ порта SIO \_ резервирование портов**  .

### <a name="lpvinbuffer"></a>лпвинбуффер

Указатель на входной буфер.
Этот параметр содержит указатель на структуру [**\_ \_ диапазона портов inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) , которая указывает номер начальной точки и число портов для резервирования.

### <a name="cbinbuffer"></a>кбинбуффер

Размер входного буфера в байтах.
Этот параметр должен быть размером структуры [**\_ \_ диапазона портов inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .

### <a name="lpvoutbuffer"></a>лпваутбуффер

Указатель на выходной буфер.
При успешном выходе этот параметр содержит указатель на структуру [**\_ \_ \_ экземпляра резервирования порта inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

### <a name="cboutbuffer"></a>кбаутбуффер

Размер выходного буфера в байтах.
Этот параметр должен быть не меньше размера структуры [**\_ \_ \_ экземпляра резервирования порта inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .

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

Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове **впукуеуеапк**.
Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция **впукуеуеапк** не вернет значение.

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
| **всаеопнотсупп** | Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка. Эта ошибка возвращается, если указанная команда IOCTL не поддерживается. Эта ошибка также возвращается, если поставщик транспорта не поддерживает **\_ запрос на получение \_ \_ резервирования порта SIO** . Эта ошибка также возвращается, если попытка использовать запрос на **\_ \_ \_ зарезервированный порт суперконтроллера** ввода/вывода выполняется на сокете, отличном от UDP или TCP. |

## <a name="remarks"></a>Комментарии

**Запрос на \_ \_ \_ зарезервированный порт SIO** поддерживается в Windows Vista и более поздних версиях операционной системы.

Приложения и службы, которым необходимо резервировать порты, делятся на две категории.
Первая категория включает компоненты, которым требуется определенный порт в рамках своей работы.
Такие компоненты, как правило, предпочитают указывать требуемый порт во время установки (например, в манифесте приложения).
Вторая категория включает компоненты, которым требуется любой доступный порт или блок портов во время выполнения.
Эти две категории соответствуют конкретным и запросам резервирования портов с подстановочными знаками.
Определенные запросы на резервирование могут быть постоянными или средой выполнения, тогда как запросы резервирования портов с подстановочными знаками поддерживаются только во время выполнения.

Запрос на получение данных о **\_ \_ \_ резервировании порта SIO**  используется для запроса резервирования среды выполнения для блока портов TCP или UDP.
Для резервирования портов во время выполнения пул портов требует, чтобы резервирования использовались в процессе, для которого было предоставлено резервирование.
Количество резервирований портов среды выполнения было последним только в течение времени существования сокета, на котором был вызван **\_ запрос IOCTL \_ \_ резервирования порта**  .
Напротив, постоянные резервирования портов, созданные с помощью функции [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) , могут быть использованы любым процессом с возможностью получения постоянных резервирований.

После получения резервирования порта времени выполнения TCP или UDP приложение может запрашивать назначения портов из резервирования портов, открыв сокет TCP или UDP, а затем вызывая функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) , указывающую на подключение SIO, и передав маркер резервирования перед вызовом функции Bind на сокете. [**\_ \_ \_**](sio-associate-port-reservation.md)

Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны **null**, сокет в этой функции будет рассматриваться как сокет без перекрытия.
Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.
Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.

Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.

Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.
Если приложение не допускает блокировку в вызове функции Всаиоктл или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.

Запрос IOCTL на **\_ Получение \_ порта \_ SIO**  может завершиться ошибкой, если операция **всаеинтр** или **WSA \_ \_ прервана** в следующих случаях:

* Запрос отменяется диспетчером ввода-вывода.
* Сокет закрыт.

## <a name="examples"></a>Примеры

В следующем примере запрашивается резервирование портов среды выполнения, затем создается сокет и выделяется порт из резервирования порта среды выполнения для сокета, а затем закрывается сокет и освобождается резервирование портов среды выполнения.

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a>См. также раздел

[**гласит**](/windows/desktop/api/winsock2/nf-winsock2-accept)

[**выполняется**](/windows/desktop/api/winsock/nf-winsock-bind)

[**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**делетеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**делетеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**\_диапазон портов \_ inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[**\_ \_ экземпляр резервирования порта \_ inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[**лукупперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**лукупперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**\_ \_ резервирование порта для сопоставления SIO \_**](sio-associate-port-reservation.md)

[**\_ \_ резервирование портов освобождения SIO \_**](sio-release-port-reservation.md)

[**фиксатор**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**всажетоверлаппедресулт**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**всасоккета**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**всасоккетв**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
