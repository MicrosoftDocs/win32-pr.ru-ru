---
title: Уведомление о явной перегрузке Winsock (ECN)
description: Некоторые приложения и (или) протоколы, основанные на протоколе UDP (например, QUIC), ищут использование явного уведомления о перегрузке (ECN) кодовыми точками для повышения задержки и колебаний в перегруженных сетях.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 79b38611cd0301d0b5d301592eec02b68c02353246c67a6c94528417623834f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322027"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a>Уведомление о явной перегрузке Winsock (ECN)

## <a name="introduction"></a>Введение

Некоторые приложения и (или) протоколы, основанные на протоколе UDP (например, QUIC), ищут использование явного уведомления о перегрузке (ECN) кодовыми точками для повышения задержки и колебаний в перегруженных сетях.

API-интерфейсы Winsock ECN расширяют интерфейс **жетсоккопт** / **сетсоккопт** , а &mdash; также [](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / интерфейс управляющих сообщений всасендмсг [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) &mdash; с поддержкой изменения и получения ECN кодовыми точками в заголовках IP. Предоставляемые функциональные возможности позволяют получать и устанавливать ECN кодовыми точками для каждого пакета.

Дополнительные сведения о ECN см. [в статье Добавление явного уведомления о перегрузке (ECN) в IP-адрес](https://tools.ietf.org/html/rfc3168).

Приложению не разрешается указывать обнаруженную перегрузку (CE) кодовую точку при отправке датаграмм. Send возвратит ошибку **всаеинвал**.

## <a name="query-ecn-with-wsagetrecvipecn"></a>Запрос ECN с помощью Всажетреквипекн

[**Всажетреквипекн**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) — это встроенная функция, определенная в `ws2tcpip.h` .

Вызовите **всажетреквипекн** , чтобы запросить текущее разрешение на получение **IP_ECN** (или **IPV6_ECN**) управляющего сообщения с помощью [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).

Также см. структуру [**всамсг**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) .

- **Протокол**: IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type**: IP_ECN (50 десятичное число)
- **Описание**: указывает/получает ECN codepoint в поле "тип" службы (TOS) IPv4-заголовка.

- **Протокол**: IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type**: IPV6_ECN (50 десятичное число)
- **Описание**: указывает/получает ECN codepoint в поле заголовка IPv6 класса трафика.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Укажите ECN с Всасетреквипекн

[**Всасетреквипекн**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) — это встроенная функция, определенная в `ws2tcpip.h` .

Вызовите **всасетреквипекн** , чтобы указать, должен ли стек IP-адресов заполнять буфер управления сообщением, содержащим ECN codepoint типа поля заголовка службы IPv4 (или поля заголовка IPv6 класса трафика) в полученной датаграмме. Если задано значение `TRUE` , функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Возвращает дополнительные данные элемента управления, содержащие ECN codepoint полученной датаграммы. Возвращаемый тип управляющего сообщения будет **IP_ECN** (или **IPV6_ECN**) с **IPPROTO_IP** уровня (или **IPPROTO_IPV6**). Данные управляющих сообщений возвращаются в виде **целого** числа. Этот параметр допустим только для сокетов датаграмм (тип сокета должен быть **SOCK_DGRAM**).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Пример кода 1. &mdash; Поддержка ECN объявлений приложений

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Пример кода 2. &mdash; Обнаружение перегрузки приложения

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a>См. также

* [всажетреквипекн](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [всасетреквипекн](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
