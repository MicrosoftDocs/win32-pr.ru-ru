---
title: Отметка времени Winsock
description: Метки времени пакетов являются важной функцией для многих приложений синхронизации часов &mdash; , например для протокола времени точности. Чем ближе создается метка времени, когда пакет получает или отправляется аппаратным обеспечением сетевого адаптера, тем более точным может быть приложение синхронизации.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559989"
---
# <a name="winsock-timestamping"></a><span data-ttu-id="ba533-104">Отметка времени Winsock</span><span class="sxs-lookup"><span data-stu-id="ba533-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="ba533-105">Введение</span><span class="sxs-lookup"><span data-stu-id="ba533-105">Introduction</span></span>

<span data-ttu-id="ba533-106">Метки времени пакетов являются важной функцией для многих приложений синхронизации часов &mdash; , например для протокола времени точности.</span><span class="sxs-lookup"><span data-stu-id="ba533-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="ba533-107">Чем ближе создается метка времени, когда пакет получает или отправляется аппаратным обеспечением сетевого адаптера, тем более точным может быть приложение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ba533-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="ba533-108">Поэтому API-интерфейсы меток времени, описанные в этом разделе, предоставляют приложению механизм для создания отчетов о отметках времени, созданных под уровнем приложения.</span><span class="sxs-lookup"><span data-stu-id="ba533-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="ba533-109">В частности, отметка времени программного обеспечения в интерфейсе между мини-портом и NDIS и аппаратной меткой времени на сетевом адаптере.</span><span class="sxs-lookup"><span data-stu-id="ba533-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="ba533-110">API меток времени может значительно повысить точность синхронизации часов.</span><span class="sxs-lookup"><span data-stu-id="ba533-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="ba533-111">В настоящее время поддержка ограничена протоколами UDP.</span><span class="sxs-lookup"><span data-stu-id="ba533-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="ba533-112">Получение отметок времени</span><span class="sxs-lookup"><span data-stu-id="ba533-112">Receive timestamps</span></span>

<span data-ttu-id="ba533-113">Вы настраиваете получение метки времени с помощью [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="ba533-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="ba533-114">Используйте этот запрос IOCTL, чтобы включить получение метки времени.</span><span class="sxs-lookup"><span data-stu-id="ba533-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="ba533-115">При получении датаграммы с помощью функции [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) ее метка времени (если она доступна) содержится в сообщении об элементе управления **SO_TIMESTAMP** .</span><span class="sxs-lookup"><span data-stu-id="ba533-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="ba533-116">**SO_TIMESTAMP** (0x300A) определяется в `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="ba533-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="ba533-117">Данные управляющих сообщений возвращаются в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="ba533-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="ba533-118">Отметка времени передачи</span><span class="sxs-lookup"><span data-stu-id="ba533-118">Transmit timestamps</span></span>

<span data-ttu-id="ba533-119">Передача метки времени также настраивается с помощью [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="ba533-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="ba533-120">Используйте этот запрос IOCTL, чтобы включить прием отметок времени и указать число отметок времени, которые система будет использовать в буфере.</span><span class="sxs-lookup"><span data-stu-id="ba533-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="ba533-121">По мере создания отметок времени передачи они добавляются в буфер.</span><span class="sxs-lookup"><span data-stu-id="ba533-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="ba533-122">Если буфер полон, новые отметки времени передачи отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="ba533-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="ba533-123">При отправке датаграммы свяжите датаграмму с управляющим сообщением **SO_TIMESTAMP_ID** .</span><span class="sxs-lookup"><span data-stu-id="ba533-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="ba533-124">Он должен содержать уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ba533-124">This should contain a unique identifier.</span></span> <span data-ttu-id="ba533-125">Отправьте датаграмму вместе с сообщением управления **SO_TIMESTAMP_ID** , используя [**всасендмсг**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span><span class="sxs-lookup"><span data-stu-id="ba533-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="ba533-126">Отметка времени передачи может быть недоступна сразу после возврата **всасендмсг** .</span><span class="sxs-lookup"><span data-stu-id="ba533-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="ba533-127">По мере того как отметка времени передачи становится доступной, они помещаются в буфер каждого сокета.</span><span class="sxs-lookup"><span data-stu-id="ba533-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="ba533-128">Используйте [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL для опроса отметки времени по ее идентификатору.</span><span class="sxs-lookup"><span data-stu-id="ba533-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="ba533-129">Если метка времени доступна, она удаляется из буфера и возвращается.</span><span class="sxs-lookup"><span data-stu-id="ba533-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="ba533-130">Если метка времени недоступна, [всажетластеррор](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) возвращает **всаеваулдблокк**.</span><span class="sxs-lookup"><span data-stu-id="ba533-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="ba533-131">Если при заполнении буфера создается отметка времени передачи, Новая отметка времени отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="ba533-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="ba533-132">**SO_TIMESTAMP_ID** (0x300B) определяется в `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="ba533-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="ba533-133">Данные управляющего сообщения должны быть предоставлены как **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="ba533-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="ba533-134">Метки времени представлены в виде значения счетчика с 64-битным значением.</span><span class="sxs-lookup"><span data-stu-id="ba533-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="ba533-135">Частота счетчика зависит от источника метки времени.</span><span class="sxs-lookup"><span data-stu-id="ba533-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="ba533-136">Для программных отметок времени счетчик является значением [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC), и его периодичность можно определить с помощью [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span><span class="sxs-lookup"><span data-stu-id="ba533-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="ba533-137">Для аппаратных меток времени частота счетчика зависит от аппаратного адаптера, и вы можете определить ее с помощью дополнительной информации, предоставляемой [**каптуреинтерфацехардварекросстиместамп**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span><span class="sxs-lookup"><span data-stu-id="ba533-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="ba533-138">Чтобы определить источник меток времени, используйте функции [**жетинтерфацеактиветиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) и [**жетинтерфацесуппортедтиместампкапабилитиес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="ba533-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="ba533-139">Помимо настройки на уровне сокета с помощью параметра [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) Socket для включения приема меток времени для сокета также требуется Системная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ba533-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="ba533-140">Оценка задержки пути отправки сокета</span><span class="sxs-lookup"><span data-stu-id="ba533-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="ba533-141">В этом разделе мы будем использовать метки времени передачи для оценки задержки пути отправки сокета.</span><span class="sxs-lookup"><span data-stu-id="ba533-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="ba533-142">Если у вас есть приложение, использующее метки времени ввода-вывода на уровне приложения, &mdash; где отметка времени должна быть максимально близкой к фактической точке передачи, &mdash; Этот пример предоставляет количественное описание, сколько API-интерфейсов по отметке времени Winsock может улучшить точность приложения.</span><span class="sxs-lookup"><span data-stu-id="ba533-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="ba533-143">В примере предполагается, что в системе только одна сетевая карта (NIC) и что *интерфацелуид* является LUID этого адаптера.</span><span class="sxs-lookup"><span data-stu-id="ba533-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="ba533-144">Оценка задержки пути получения сокета</span><span class="sxs-lookup"><span data-stu-id="ba533-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="ba533-145">Ниже приведен похожий пример для пути получения.</span><span class="sxs-lookup"><span data-stu-id="ba533-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="ba533-146">В примере предполагается, что в системе только одна сетевая карта (NIC) и что *интерфацелуид* является LUID этого адаптера.</span><span class="sxs-lookup"><span data-stu-id="ba533-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="a-limitation"></a><span data-ttu-id="ba533-147">Ограничение</span><span class="sxs-lookup"><span data-stu-id="ba533-147">A limitation</span></span>

<span data-ttu-id="ba533-148">Одно из ограничений API-интерфейсов отметок времени Winsock заключается в том, что вызов [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) всегда является неблокирующей операцией.</span><span class="sxs-lookup"><span data-stu-id="ba533-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="ba533-149">Даже вызов IOCTL в перекрытом виде приводит к немедленному возврату **всаеваулдблокк** , если в настоящее время нет доступных отметок времени передачи.</span><span class="sxs-lookup"><span data-stu-id="ba533-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="ba533-150">Так как отметка времени передачи может быть недоступна сразу после возврата [**всасендмсг**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) , приложение должно опросить ioctl до тех пор, пока не будет доступна отметка времени.</span><span class="sxs-lookup"><span data-stu-id="ba533-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="ba533-151">Отметка времени передачи гарантированно будет доступна после успешного вызова **всасендмсг** , учитывая, что буфер отметок времени передачи не полон.</span><span class="sxs-lookup"><span data-stu-id="ba533-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
