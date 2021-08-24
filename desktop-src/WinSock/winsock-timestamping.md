---
title: Отметка времени Winsock
description: Метки времени пакетов являются важной функцией для многих приложений синхронизации часов &mdash; , например для протокола времени точности. Чем ближе создается метка времени, когда пакет получает или отправляется аппаратным обеспечением сетевого адаптера, тем более точным может быть приложение синхронизации.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: 329c13d76fc0c4ce0d87550623e7419af14bfdd268bf359a8f50729e0b0596e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568994"
---
# <a name="winsock-timestamping"></a>Отметка времени Winsock

## <a name="introduction"></a>Введение

Метки времени пакетов являются важной функцией для многих приложений синхронизации часов &mdash; , например для протокола времени точности. Чем ближе создается метка времени, когда пакет получает или отправляется аппаратным обеспечением сетевого адаптера, тем более точным может быть приложение синхронизации.

Поэтому API-интерфейсы меток времени, описанные в этом разделе, предоставляют приложению механизм для создания отчетов о отметках времени, созданных под уровнем приложения. В частности, отметка времени программного обеспечения в интерфейсе между мини-портом и NDIS и аппаратной меткой времени на сетевом адаптере. API меток времени может значительно повысить точность синхронизации часов. В настоящее время поддержка ограничена протоколами UDP.

## <a name="receive-timestamps"></a>Получение отметок времени

Вы настраиваете получение метки времени с помощью [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Используйте этот запрос IOCTL, чтобы включить получение метки времени. При получении датаграммы с помощью функции [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) ее метка времени (если она доступна) содержится в сообщении об элементе управления **SO_TIMESTAMP** .

**SO_TIMESTAMP** (0x300A) определяется в `mstcpip.h` . Данные управляющих сообщений возвращаются в виде **UINT64**.

## <a name="transmit-timestamps"></a>Отметка времени передачи

Передача метки времени также настраивается с помощью [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Используйте этот запрос IOCTL, чтобы включить прием отметок времени и указать число отметок времени, которые система будет использовать в буфере. По мере создания отметок времени передачи они добавляются в буфер. Если буфер полон, новые отметки времени передачи отбрасываются.

При отправке датаграммы свяжите датаграмму с управляющим сообщением **SO_TIMESTAMP_ID** . Он должен содержать уникальный идентификатор. Отправьте датаграмму вместе с сообщением управления **SO_TIMESTAMP_ID** , используя [**всасендмсг**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg). Отметка времени передачи может быть недоступна сразу после возврата **всасендмсг** . По мере того как отметка времени передачи становится доступной, они помещаются в буфер каждого сокета. Используйте [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL для опроса отметки времени по ее идентификатору. Если метка времени доступна, она удаляется из буфера и возвращается. Если метка времени недоступна, [всажетластеррор](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) возвращает **всаеваулдблокк**. Если при заполнении буфера создается отметка времени передачи, Новая отметка времени отбрасывается.

**SO_TIMESTAMP_ID** (0x300B) определяется в `mstcpip.h` . Данные управляющего сообщения должны быть предоставлены как **UINT32**.

Метки времени представлены в виде значения счетчика с 64-битным значением. Частота счетчика зависит от источника метки времени. Для программных отметок времени счетчик является значением [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC), и его периодичность можно определить с помощью [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency). Для аппаратных меток времени частота счетчика зависит от аппаратного адаптера, и вы можете определить ее с помощью дополнительной информации, предоставляемой [**каптуреинтерфацехардварекросстиместамп**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp). Чтобы определить источник меток времени, используйте функции [**жетинтерфацеактиветиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) и [**жетинтерфацесуппортедтиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .

Помимо настройки на уровне сокета с помощью параметра [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) Socket для включения приема меток времени для сокета также требуется Системная конфигурация.

## <a name="estimating-latency-of-socket-send-path"></a>Оценка задержки пути отправки сокета

В этом разделе мы будем использовать метки времени передачи для оценки задержки пути отправки сокета. Если у вас есть приложение, использующее метки времени ввода-вывода на уровне приложения, &mdash; где отметка времени должна быть максимально близкой к фактической точке передачи, &mdash; Этот пример предоставляет количественное описание, сколько API-интерфейсов по отметке времени Winsock может улучшить точность приложения.

В примере предполагается, что в системе только одна сетевая карта (NIC) и что *интерфацелуид* является LUID этого адаптера.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

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
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a>Оценка задержки пути получения сокета

Ниже приведен похожий пример для пути получения. В примере предполагается, что в системе только одна сетевая карта (NIC) и что *интерфацелуид* является LUID этого адаптера.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a>Ограничение

Одно из ограничений API-интерфейсов отметок времени Winsock заключается в том, что вызов [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) всегда является неблокирующей операцией. Даже вызов IOCTL в перекрытом виде приводит к немедленному возврату **всаеваулдблокк** , если в настоящее время нет доступных отметок времени передачи. Так как отметка времени передачи может быть недоступна сразу после возврата [**всасендмсг**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) , приложение должно опросить ioctl до тех пор, пока не будет доступна отметка времени. Отметка времени передачи гарантированно будет доступна после успешного вызова **всасендмсг** , учитывая, что буфер отметок времени передачи не полон.
