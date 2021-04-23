---
description: Установка сеанса PGM похожа на подпрограммы установки соединения, связанные с сеансом TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Отправителей и получателей PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e300a0c9de199e1f836e71407caf6487812cf7b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541519"
---
# <a name="pgm-senders-and-receivers"></a><span data-ttu-id="b10bd-103">Отправителей и получателей PGM</span><span class="sxs-lookup"><span data-stu-id="b10bd-103">PGM Senders and Receivers</span></span>

<span data-ttu-id="b10bd-104">Установка сеанса PGM похожа на подпрограммы установки соединения, связанные с сеансом TCP.</span><span class="sxs-lookup"><span data-stu-id="b10bd-104">Establishing a PGM session is similar to the connection establishment routine associated with a TCP session.</span></span> <span data-ttu-id="b10bd-105">Однако значительная отклонить от сеанса TCP заключается в том, что семантика клиента и сервера отменяется. сервер (отправитель PGM) подключается к группе многоадресной рассылки, а клиент (получатель PGM) ожидает принятия подключения.</span><span class="sxs-lookup"><span data-stu-id="b10bd-105">The significant departure from a TCP session, however, is that the client and server semantics are reversed; the server (the PGM sender) connects to a multicast group, while the client (the PGM receiver) waits to accept a connection.</span></span> <span data-ttu-id="b10bd-106">Следующие абзацы представляют собой сведения о программных действиях, необходимых для создания отправителя PGM и получателя PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-106">The following paragraphs detail programmatic steps necessary for creating a PGM sender and a PGM receiver.</span></span> <span data-ttu-id="b10bd-107">На этой странице также описаны доступные режимы данных для сеансов PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-107">This page also describes the available data modes for PGM sessions.</span></span>

## <a name="pgm-sender"></a><span data-ttu-id="b10bd-108">Отправитель PGM</span><span class="sxs-lookup"><span data-stu-id="b10bd-108">PGM Sender</span></span>

<span data-ttu-id="b10bd-109">**Чтобы создать отправителя PGM, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="b10bd-109">**To create a PGM sender, perform the following steps**</span></span>

1.  <span data-ttu-id="b10bd-110">Создайте сокет PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-110">Create a PGM socket.</span></span>
2.  <span data-ttu-id="b10bd-111">[**привяжите**](/windows/desktop/api/winsock/nf-winsock-bind) сокет к адресу \_ .</span><span class="sxs-lookup"><span data-stu-id="b10bd-111">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to INADDR\_ANY.</span></span>
3.  <span data-ttu-id="b10bd-112">[**подключитесь**](/windows/desktop/api/Winsock2/nf-winsock2-connect) к адресу передачи группы многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="b10bd-112">[**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) to the multicast group transmission address.</span></span>

<span data-ttu-id="b10bd-113">Для клиентов не выполняются подтверждения формальных сеансов.</span><span class="sxs-lookup"><span data-stu-id="b10bd-113">No formal session handshaking is performed with any clients.</span></span> <span data-ttu-id="b10bd-114">Процесс подключения аналогичен протоколу UDP [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), в котором он связывает адрес конечной точки (группу многоадресной рассылки) с сокетом.</span><span class="sxs-lookup"><span data-stu-id="b10bd-114">The connection process is similar to a UDP [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), in that it associates an endpoint address (the multicast group) with the socket.</span></span> <span data-ttu-id="b10bd-115">По завершении данные могут быть отправлены на сокет.</span><span class="sxs-lookup"><span data-stu-id="b10bd-115">Once completed, data may be sent on the socket.</span></span>

<span data-ttu-id="b10bd-116">Когда отправитель создает сокет PGM и подключает его к адресу многоадресной рассылки, создается сеанс PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-116">When a sender creates a PGM socket and connects it to a multicast address, a PGM session is created.</span></span> <span data-ttu-id="b10bd-117">Надежный сеанс многоадресной рассылки определяется сочетанием глобального уникального идентификатора (GUID) и исходного порта.</span><span class="sxs-lookup"><span data-stu-id="b10bd-117">A reliable multicast session is defined by a combination of the globally unique identifier (GUID) and the source port.</span></span> <span data-ttu-id="b10bd-118">Идентификатор GUID создается транспортом.</span><span class="sxs-lookup"><span data-stu-id="b10bd-118">The GUID is generated by the transport.</span></span> <span data-ttu-id="b10bd-119">Порт Ссаурце задается транспортом, и не предоставляется контроль над тем, какой порт источника используется.</span><span class="sxs-lookup"><span data-stu-id="b10bd-119">The sSource port is specified by the transport, and no control is provided over which source port is used.</span></span>

> [!Note]  
> <span data-ttu-id="b10bd-120">Получение данных в сокете отправителя запрещено и приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10bd-120">Receiving data on a sender socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="b10bd-121">В следующем фрагменте кода показано, как настроить отправителя PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-121">The following code snippet illustrates setting up a PGM sender:</span></span>


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a><span data-ttu-id="b10bd-122">Получатель PGM</span><span class="sxs-lookup"><span data-stu-id="b10bd-122">PGM Receiver</span></span>

<span data-ttu-id="b10bd-123">**Чтобы создать приемник PGM, выполните следующие действия.**</span><span class="sxs-lookup"><span data-stu-id="b10bd-123">**To create a PGM receiver, perform the following steps**</span></span>

1.  <span data-ttu-id="b10bd-124">Создайте сокет PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-124">Create a PGM socket.</span></span>
2.  <span data-ttu-id="b10bd-125">[**привяжите**](/windows/desktop/api/winsock/nf-winsock-bind) сокет к адресу группы многоадресной рассылки, на которую отправляется отправитель.</span><span class="sxs-lookup"><span data-stu-id="b10bd-125">[**bind**](/windows/desktop/api/winsock/nf-winsock-bind) the socket to the multicast group address on which the sender is transmitting.</span></span>
3.  <span data-ttu-id="b10bd-126">Вызовите функцию [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) на сокете, чтобы перевести сокет в режим прослушивания.</span><span class="sxs-lookup"><span data-stu-id="b10bd-126">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function on the socket to put the socket in listening mode.</span></span> <span data-ttu-id="b10bd-127">Функция Listen Возвращает время обнаружения сеанса PGM по указанному адресу и порту группы многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="b10bd-127">The listen function returns when a PGM session is detected on the specified multicast group address and port.</span></span>
4.  <span data-ttu-id="b10bd-128">Вызовите функцию [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , чтобы получить новый маркер сокета, соответствующий сеансу.</span><span class="sxs-lookup"><span data-stu-id="b10bd-128">Call the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function to obtain a new socket handle corresponding to the session.</span></span>

<span data-ttu-id="b10bd-129">Принятие нового сеанса инициируется только исходными данными PGM (ODATA).</span><span class="sxs-lookup"><span data-stu-id="b10bd-129">Only original PGM data (ODATA) triggers the acceptance of a new session.</span></span> <span data-ttu-id="b10bd-130">Таким образом, транспорт может получить другой трафик PGM (например, пакеты SPM или RDATA), но не приводит к возврату функции [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="b10bd-130">As such, other PGM traffic (such as SPM or RDATA packets) may be received by the transport, but do not result in the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function returning.</span></span>

<span data-ttu-id="b10bd-131">После принятия сеанса для получения данных используется возвращенный маркер сокета.</span><span class="sxs-lookup"><span data-stu-id="b10bd-131">Once a session is accepted, the returned socket handle is used for receiving data.</span></span>

> [!Note]  
> <span data-ttu-id="b10bd-132">Отправка данных через сокет приема запрещена и приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="b10bd-132">Sending data on a receive socket is not allowed, and results in an error.</span></span>

 

<span data-ttu-id="b10bd-133">В следующем фрагменте кода показано, как настроить приемник PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-133">The following code snippet illustrates setting up a PGM receiver:</span></span>


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a><span data-ttu-id="b10bd-134">Режимы данных</span><span class="sxs-lookup"><span data-stu-id="b10bd-134">Data Modes</span></span>

<span data-ttu-id="b10bd-135">Сеансы PGM имеют два варианта режима данных: режим сообщения и режим потока.</span><span class="sxs-lookup"><span data-stu-id="b10bd-135">PGM sessions have two options for data modes: message mode and stream mode.</span></span>

<span data-ttu-id="b10bd-136">Режим сообщения подходит для приложений, которые должны отсылать дискретные сообщения и задается типом сокета Сокк \_ RDM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-136">Message mode is appropriate for applications that need to send discrete messages, and is specified by a socket type of SOCK\_RDM.</span></span> <span data-ttu-id="b10bd-137">Режим потока подходит для приложений, которым требуется передавать потоковые данные получателям, таким как приложения видео или голоса, и задается типом сокета \_ потока Сокк.</span><span class="sxs-lookup"><span data-stu-id="b10bd-137">Stream mode is appropriate for applications that need to send streaming data to receivers, such as video or voice applications, and is specified by a socket type of SOCK\_STREAM.</span></span> <span data-ttu-id="b10bd-138">Режим выбора влияет на то, как Winsock обрабатывает данные.</span><span class="sxs-lookup"><span data-stu-id="b10bd-138">The choice of mode effects how Winsock processes data.</span></span>

<span data-ttu-id="b10bd-139">Рассмотрим следующий пример: в режиме сообщения отправитель PGM выполняет три вызова функции [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , каждая с буфером 100 байт.</span><span class="sxs-lookup"><span data-stu-id="b10bd-139">Consider the following example: A message mode PGM sender makes three calls to the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) function, each with a 100-byte buffer.</span></span> <span data-ttu-id="b10bd-140">Эта операция отображается в сети как три отдельных пакета PGM.</span><span class="sxs-lookup"><span data-stu-id="b10bd-140">This operation appears on the wire as three discrete PGM packets.</span></span> <span data-ttu-id="b10bd-141">На стороне получателя каждый вызов функции [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) возвращает только 100 байт, даже если предоставлен больший буфер получения.</span><span class="sxs-lookup"><span data-stu-id="b10bd-141">On the receiver side, each call to the [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) function returns only 100 bytes, even if a larger receive buffer is provided.</span></span> <span data-ttu-id="b10bd-142">В отличие от этого, при использовании отправителя PGM в режиме потока эти 3 100 байт могут сообщаться менее чем с тремя физическими пакетами по сети (или объединены в один большой двоичный объект данных на стороне получателя).</span><span class="sxs-lookup"><span data-stu-id="b10bd-142">In contrast, with a stream mode PGM sender those three 100 byte transmissions could be coalesced into less than three physical packets on the wire (or coalesced into one blob of data on the receiver side).</span></span> <span data-ttu-id="b10bd-143">Таким образом, когда получатель вызывает одну из функций получения сокетов Windows, любой объем данных, полученных транспортом PGM, может быть возвращен в приложение без учета того, как данные были физически переданы или получены.</span><span class="sxs-lookup"><span data-stu-id="b10bd-143">As such, when the receiver calls one of the Windows Sockets receive functions, any amount of data that has been received by the PGM transport may be returned to the application without regard to how the data was physically transmitted or received.</span></span>

 

 



