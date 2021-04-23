---
description: Отправка и получение данных PGM аналогична отправке или приему данных на любом сокете. Существуют некоторые рекомендации по протоколу PGM, приведенные в следующих параграфах.
ms.assetid: 51b447ad-b6da-424b-91df-e5be9ce225a5
title: Отправка и получение данных PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab73999c33c97c6ba528552af6d746d54fb605df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156014"
---
# <a name="sending-and-receiving-pgm-data"></a><span data-ttu-id="139d1-104">Отправка и получение данных PGM</span><span class="sxs-lookup"><span data-stu-id="139d1-104">Sending and Receiving PGM Data</span></span>

<span data-ttu-id="139d1-105">Отправка и получение данных PGM аналогична отправке или приему данных на любом сокете.</span><span class="sxs-lookup"><span data-stu-id="139d1-105">Sending and receiving PGM data is similar to sending or receiving data on any socket.</span></span> <span data-ttu-id="139d1-106">Существуют некоторые рекомендации по протоколу PGM, приведенные в следующих параграфах.</span><span class="sxs-lookup"><span data-stu-id="139d1-106">There are considerations specific to PGM, outlined in the following paragraphs.</span></span>

## <a name="sending-pgm-data"></a><span data-ttu-id="139d1-107">Отправка данных PGM</span><span class="sxs-lookup"><span data-stu-id="139d1-107">Sending PGM Data</span></span>

<span data-ttu-id="139d1-108">После создания сеанса отправителя PGM данные отправляются с помощью различных функций отправки сокетов Windows: [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)и [**всасендто**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span><span class="sxs-lookup"><span data-stu-id="139d1-108">Once a PGM sender session is created, data is sent using the various Windows Sockets send functions: [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto).</span></span> <span data-ttu-id="139d1-109">Так как дескрипторы сокетов Windows являются дескрипторами файловой системы, другие функции, такие как функции [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) и CRT, также могут передавать данные.</span><span class="sxs-lookup"><span data-stu-id="139d1-109">Since Windows Sockets handles are file system handles, other functions such as [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile) and CRT functions can also transmit data.</span></span> <span data-ttu-id="139d1-110">В следующем фрагменте кода показана операция отправителя PGM:</span><span class="sxs-lookup"><span data-stu-id="139d1-110">The following code snippet illustrates a PGM sender operation:</span></span>


```C++
LONG        error;
    //:
error = send (s, pSendBuffer, SendLength, 0);
if (error == SOCKET_ERROR)
{
    fprintf (stderr, "send() failed: Error = %d\n",
             WSAGetLastError());
}
```



<span data-ttu-id="139d1-111">При использовании режима сообщений (Сокк \_ RDM) каждый вызов функции Send приводит к появлению дискретного сообщения, которое иногда нежелательно; приложение может захотеть отправить сообщение 2 МБ с несколькими вызовами для [**отправки**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span><span class="sxs-lookup"><span data-stu-id="139d1-111">When using message mode (SOCK\_RDM), each call to a send function results in a discrete message, which sometimes isn't desirable; an application may want to send a 2 megabyte message with multiple calls to [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send).</span></span> <span data-ttu-id="139d1-112">В таких обстоятельствах отправитель может установить параметр сокета [ \_ \_ \_ границ сообщения RM](socket-options.md) , чтобы указать размер сообщения, следующего за ним.</span><span class="sxs-lookup"><span data-stu-id="139d1-112">In such circumstances, the sender can set the [RM\_SET\_MESSAGE\_BOUNDARY](socket-options.md) socket option to indicate the size of the message that followings.</span></span>

<span data-ttu-id="139d1-113">Если окно отправки заполнено, Новая отправка из приложения не принимается, пока окно не будет расширено.</span><span class="sxs-lookup"><span data-stu-id="139d1-113">If the send window is full, a new send from the application is not accepted until window has been advanced.</span></span> <span data-ttu-id="139d1-114">Попытка отправки на неблокирующий сокет завершается сбоем с ВСАЕВАУЛДБЛОКК; Блокирующий сокет просто блокируется до тех пор, пока окно не перейдет к точке, в которой запрошенные данные могут быть помещены в буфер и отправлены.</span><span class="sxs-lookup"><span data-stu-id="139d1-114">Attempting to send on a non-blocking socket fails with WSAEWOULDBLOCK; a blocking socket simply blocks until the window advances to the point where the requested data can be buffered and sent.</span></span> <span data-ttu-id="139d1-115">В перекрытом вводе-выводе операция не завершается до тех пор, пока окно не будет достаточно для размещения новых данных.</span><span class="sxs-lookup"><span data-stu-id="139d1-115">In overlapped I/O, the operation does not complete until the window advances enough to accommodate the new data.</span></span>

## <a name="receiving-pgm-data"></a><span data-ttu-id="139d1-116">Получение данных PGM</span><span class="sxs-lookup"><span data-stu-id="139d1-116">Receiving PGM Data</span></span>

<span data-ttu-id="139d1-117">После создания сеанса приемника PGM данные получаются с помощью различных функций получения сокетов Windows: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)и [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span><span class="sxs-lookup"><span data-stu-id="139d1-117">Once a PGM receiver session is created, data is received using the various Windows Sockets receive functions: [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom).</span></span> <span data-ttu-id="139d1-118">Так как дескрипторы сокетов Windows также являются дескрипторами файлов, функции [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) и CRT можно также использовать для получения данных сеанса PGM.</span><span class="sxs-lookup"><span data-stu-id="139d1-118">Since Windows Sockets handles are also file handles, the [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) and CRT functions can also be used to receive PGM session data.</span></span> <span data-ttu-id="139d1-119">Транспорт пересылает данные получателю по мере поступления, если данные находятся в последовательности.</span><span class="sxs-lookup"><span data-stu-id="139d1-119">The transport forwards data up to the receiver as it arrives as long as the data is in sequence.</span></span> <span data-ttu-id="139d1-120">Транспорт гарантирует, что возвращаемые данные являются непрерывными и освобождаются от дубликатов.</span><span class="sxs-lookup"><span data-stu-id="139d1-120">The transport guarantees that the data returned is contiguous and free of duplicates.</span></span> <span data-ttu-id="139d1-121">В следующем фрагменте кода показана операция получения PGM:</span><span class="sxs-lookup"><span data-stu-id="139d1-121">The following code snippet illustrates a PGM receive operation:</span></span>


```C++
LONG        BytesRead;
    //:
BytesRead = recv (sockR, pTestBuffer, MaxBufferSize, 0);
if (BytesRead == 0)
{
    fprintf(stdout, "Session was terminated\n");
}
else if (BytesRead == SOCKET_ERROR)
{
    fprintf(stderr, "recv() failed: Error = %d\n",
            WSAGetLastError());
}
```



<span data-ttu-id="139d1-122">При использовании режима сообщений (Сокк \_ RDM) транспорт указывает, когда получено частичное сообщение либо с ошибкой всаемсгсизе, либо путем установки \_ флага «MSG partial» при возврате из функций [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) и [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="139d1-122">When using message mode (SOCK\_RDM), the transport indicates when a partial message is received, either with the WSAEMSGSIZE error, or by setting the MSG\_PARTIAL flag upon return from the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) and [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) functions.</span></span> <span data-ttu-id="139d1-123">Когда клиенту возвращается последний фрагмент полного сообщения, ошибка или флаг не указываются.</span><span class="sxs-lookup"><span data-stu-id="139d1-123">When the last fragment of the full message is returned to the client, the error or flag is not indicated.</span></span>

<span data-ttu-id="139d1-124">При корректном завершении сеанса операция получения завершается с ВСАЕДИСКОН.</span><span class="sxs-lookup"><span data-stu-id="139d1-124">When the session is terminated gracefully, the receive operation fails with WSAEDISCON.</span></span> <span data-ttu-id="139d1-125">Когда происходит потеря данных в транспорте, протокол PGM временно помещает в буфер непоследовательные пакеты и пытается восстановить потерянные данные.</span><span class="sxs-lookup"><span data-stu-id="139d1-125">When data loss occurs in the transport, PGM temporarily buffers the out-of-sequence packets and attempts to recover the lost data.</span></span> <span data-ttu-id="139d1-126">Если потери данных невозможно восстановить, операция получения завершается с ВСАЕКОННРЕСЕТ, а сеанс завершается.</span><span class="sxs-lookup"><span data-stu-id="139d1-126">If the data-loss is unrecoverable, the receive operation fail with WSAECONNRESET, and the session is terminated.</span></span> <span data-ttu-id="139d1-127">Сеанс можно сбросить из-за ряда условий, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="139d1-127">The session can be reset due to a variety of conditions, including the following:</span></span>

-   <span data-ttu-id="139d1-128">Скорость входящего и исступающего подключения слишком мала для сохранения скорости передачи данных.</span><span class="sxs-lookup"><span data-stu-id="139d1-128">The receiver or the incoming connection rate is too slow to keep pace with the incoming data rate.</span></span>
-   <span data-ttu-id="139d1-129">Чрезмерная потери данных, возможно, из-за временных условий сети, таких как проблемы маршрутизации, нестабильность сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="139d1-129">Excessive data loss occurs, possibly due to transient network conditions, such as routing problems, network instability, and so forth.</span></span>
-   <span data-ttu-id="139d1-130">В отправителю возникает неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="139d1-130">An unrecoverable error occurs on the sender.</span></span>
-   <span data-ttu-id="139d1-131">Чрезмерное использование ресурсов происходит на локальном компьютере, например при превышении максимально допустимого внутреннего хранилища буфера или при обнаружении нехватки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="139d1-131">Excessive resource utilization occurs on the local computer, such as exceeding the maximum allowed internal buffer storage, or encountering an out-of-resources condition.</span></span>
-   <span data-ttu-id="139d1-132">Возникает ошибка проверки согласованности данных.</span><span class="sxs-lookup"><span data-stu-id="139d1-132">A data consistency check error occurs.</span></span>
-   <span data-ttu-id="139d1-133">Сбой в компоненте PGM зависит от, например TCP/IP или сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="139d1-133">Failure in a component PGM depends on, such as TCP/IP or Windows Sockets.</span></span>

<span data-ttu-id="139d1-134">Как первый, так и второй элементы в приведенном выше списке могут привести к чрезмерной буферизации приемника до истечения ресурсов или в конечном итоге за пределами окна отправителя.</span><span class="sxs-lookup"><span data-stu-id="139d1-134">Both the first and second items in the above list could result in the receiver performing excessive buffering before running out of resources, or before ultimately moving beyond the sender's window.</span></span>

## <a name="terminating-a-pgm-session"></a><span data-ttu-id="139d1-135">Завершение сеанса PGM</span><span class="sxs-lookup"><span data-stu-id="139d1-135">Terminating A PGM Session</span></span>

<span data-ttu-id="139d1-136">Отправитель или получатель PGM может перемешать отправку или получение данных, вызвав [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span><span class="sxs-lookup"><span data-stu-id="139d1-136">The PGM sender or receiver can stop sending or receiving data by calling [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket).</span></span> <span data-ttu-id="139d1-137">Получатель должен вызвать **функции closesocket** как для прослушивания, так и для приема сокетов, чтобы предотвратить утечки в обработке.</span><span class="sxs-lookup"><span data-stu-id="139d1-137">The receiver must call **closesocket** on both the listening and receiving sockets to prevent handle leaks.</span></span> <span data-ttu-id="139d1-138">Вызов метода [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) на отправителю перед вызовом **функции closesocket** гарантирует, что все данные будут отправлены, и данные об исправлении сохраняются до тех пор, пока окно отправки не перейдет за последнюю последовательность данных, даже если само приложение завершается.</span><span class="sxs-lookup"><span data-stu-id="139d1-138">Calling [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) on the sender before calling **closesocket** ensures all data gets sent, and ensures repair data is maintained until the send window advances past the last data sequence, even if the application itself terminates.</span></span>

 

 
