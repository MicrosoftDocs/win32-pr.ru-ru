---
title: Уведомление о явной перегрузке Winsock (ECN)
description: Некоторые приложения и (или) протоколы, основанные на протоколе UDP (например, QUIC), ищут использование явного уведомления о перегрузке (ECN) кодовыми точками для повышения задержки и колебаний в перегруженных сетях.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110560004"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="82caf-103">Уведомление о явной перегрузке Winsock (ECN)</span><span class="sxs-lookup"><span data-stu-id="82caf-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="82caf-104">Введение</span><span class="sxs-lookup"><span data-stu-id="82caf-104">Introduction</span></span>

<span data-ttu-id="82caf-105">Некоторые приложения и (или) протоколы, основанные на протоколе UDP (например, QUIC), ищут использование явного уведомления о перегрузке (ECN) кодовыми точками для повышения задержки и колебаний в перегруженных сетях.</span><span class="sxs-lookup"><span data-stu-id="82caf-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="82caf-106">API-интерфейсы Winsock ECN расширяют интерфейс **жетсоккопт** / **сетсоккопт** , а &mdash; также [](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / интерфейс управляющих сообщений всасендмсг [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) &mdash; с поддержкой изменения и получения ECN кодовыми точками в заголовках IP.</span><span class="sxs-lookup"><span data-stu-id="82caf-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="82caf-107">Предоставляемые функциональные возможности позволяют получать и устанавливать ECN кодовыми точками для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="82caf-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="82caf-108">Дополнительные сведения о ECN см. [в статье Добавление явного уведомления о перегрузке (ECN) в IP-адрес](https://tools.ietf.org/html/rfc3168).</span><span class="sxs-lookup"><span data-stu-id="82caf-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="82caf-109">Приложению не разрешается указывать обнаруженную перегрузку (CE) кодовую точку при отправке датаграмм.</span><span class="sxs-lookup"><span data-stu-id="82caf-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="82caf-110">Send возвратит ошибку **всаеинвал**.</span><span class="sxs-lookup"><span data-stu-id="82caf-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="82caf-111">Запрос ECN с помощью Всажетреквипекн</span><span class="sxs-lookup"><span data-stu-id="82caf-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="82caf-112">[**Всажетреквипекн**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) — это встроенная функция, определенная в `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="82caf-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="82caf-113">Вызовите **всажетреквипекн** , чтобы запросить текущее разрешение на получение **IP_ECN** (или **IPV6_ECN**) управляющего сообщения с помощью [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span><span class="sxs-lookup"><span data-stu-id="82caf-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="82caf-114">Также см. структуру [**всамсг**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) .</span><span class="sxs-lookup"><span data-stu-id="82caf-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="82caf-115">**Протокол**: IPv4</span><span class="sxs-lookup"><span data-stu-id="82caf-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="82caf-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="82caf-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="82caf-117">**Cmsg_type**: IP_ECN (50 десятичное число)</span><span class="sxs-lookup"><span data-stu-id="82caf-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="82caf-118">**Описание**: указывает/получает ECN codepoint в поле "тип" службы (TOS) IPv4-заголовка.</span><span class="sxs-lookup"><span data-stu-id="82caf-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="82caf-119">**Протокол**: IPv6</span><span class="sxs-lookup"><span data-stu-id="82caf-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="82caf-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="82caf-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="82caf-121">**Cmsg_type**: IPV6_ECN (50 десятичное число)</span><span class="sxs-lookup"><span data-stu-id="82caf-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="82caf-122">**Описание**: указывает/получает ECN codepoint в поле заголовка IPv6 класса трафика.</span><span class="sxs-lookup"><span data-stu-id="82caf-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="82caf-123">Укажите ECN с Всасетреквипекн</span><span class="sxs-lookup"><span data-stu-id="82caf-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="82caf-124">[**Всасетреквипекн**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) — это встроенная функция, определенная в `ws2tcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="82caf-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="82caf-125">Вызовите **всасетреквипекн** , чтобы указать, должен ли стек IP-адресов заполнять буфер управления сообщением, содержащим ECN codepoint типа поля заголовка службы IPv4 (или поля заголовка IPv6 класса трафика) в полученной датаграмме.</span><span class="sxs-lookup"><span data-stu-id="82caf-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="82caf-126">Если задано значение `TRUE` , функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Возвращает дополнительные данные элемента управления, содержащие ECN codepoint полученной датаграммы.</span><span class="sxs-lookup"><span data-stu-id="82caf-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="82caf-127">Возвращаемый тип управляющего сообщения будет **IP_ECN** (или **IPV6_ECN**) с **IPPROTO_IP** уровня (или **IPPROTO_IPV6**).</span><span class="sxs-lookup"><span data-stu-id="82caf-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="82caf-128">Данные управляющих сообщений возвращаются в виде **целого** числа.</span><span class="sxs-lookup"><span data-stu-id="82caf-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="82caf-129">Этот параметр допустим только для сокетов датаграмм (тип сокета должен быть **SOCK_DGRAM**).</span><span class="sxs-lookup"><span data-stu-id="82caf-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="82caf-130">Пример кода 1. &mdash; Поддержка ECN объявлений приложений</span><span class="sxs-lookup"><span data-stu-id="82caf-130">Code example 1&mdash;application advertising ECN support</span></span>

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="82caf-131">Пример кода 2. &mdash; Обнаружение перегрузки приложения</span><span class="sxs-lookup"><span data-stu-id="82caf-131">Code example 2&mdash;application detecting congestion</span></span>

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

## <a name="see-also"></a><span data-ttu-id="82caf-132">См. также</span><span class="sxs-lookup"><span data-stu-id="82caf-132">See also</span></span>

* [<span data-ttu-id="82caf-133">всажетреквипекн</span><span class="sxs-lookup"><span data-stu-id="82caf-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="82caf-134">всасетреквипекн</span><span class="sxs-lookup"><span data-stu-id="82caf-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
