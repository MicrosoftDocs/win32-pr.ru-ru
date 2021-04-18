---
description: После того как сокет прослушивает соединение, программа должна выполнять запросы на подключение к этому сокету.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Принятие подключения (сокеты Windows 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650536"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="2b0bd-103">Принятие подключения (сокеты Windows 2)</span><span class="sxs-lookup"><span data-stu-id="2b0bd-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="2b0bd-104">После того как сокет прослушивает соединение, программа должна выполнять запросы на подключение к этому сокету.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="2b0bd-105">**Принятие подключения на сокете**</span><span class="sxs-lookup"><span data-stu-id="2b0bd-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="2b0bd-106">Создайте временный объект **Socket** с именем клиентсоккет для приема соединений от клиентов.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="2b0bd-107">Обычно серверное приложение предназначено для прослушивания подключений от нескольких клиентов.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="2b0bd-108">Для высокопроизводительных серверов несколько потоков обычно используются для управления несколькими клиентскими подключениями.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="2b0bd-109">Существует несколько различных методов программирования, использующих Winsock, которые можно использовать для прослушивания нескольких клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="2b0bd-110">Одним из методов программирования является создание непрерывного цикла, который проверяет наличие запросов на подключение с помощью функции [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (см. раздел [прослушивание на сокете](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="2b0bd-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="2b0bd-111">Если происходит запрос на соединение, приложение вызывает функцию [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)или [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) и передает работу другому потоку для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="2b0bd-112">Возможно несколько других приемов программирования.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="2b0bd-113">Обратите внимание, что этот простой пример очень прост и не использует несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="2b0bd-114">Пример также просто прослушивает и принимает только одно соединение.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="2b0bd-115">Когда клиентское соединение принято, серверное приложение обычно передает принятый клиентский сокет (переменную Клиентсоккет в приведенном выше примере кода) в рабочий поток или порт завершения ввода-вывода и продолжает принимать дополнительные соединения.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="2b0bd-116">В этом базовом примере сервер переходит к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="2b0bd-117">Существует ряд других методов программирования, которые можно использовать для прослушивания и принятия нескольких подключений.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="2b0bd-118">Они включают использование функций [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="2b0bd-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="2b0bd-119">Примеры некоторых из этих методов программирования показаны в [расширенных примерах Winsock](getting-started-with-winsock.md) , входящих в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="2b0bd-120">В системах Unix общий метод программирования для серверов был для того, чтобы приложение было прослушивать подключения.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="2b0bd-121">Когда соединение было принято, родительский процесс вызовет функцию **ветвления** для создания нового дочернего процесса для обработки клиентского соединения, наследуя сокет от родительского.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="2b0bd-122">Этот метод программирования не поддерживается в Windows, так как функция **ветвления** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="2b0bd-123">Эта методика обычно не подходит для высокопроизводительных серверов, так как ресурсы, необходимые для создания нового процесса, гораздо больше, чем те, которые необходимы для потока.</span><span class="sxs-lookup"><span data-stu-id="2b0bd-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="2b0bd-124">Следующий шаг: [Получение и отправка данных на сервере](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="2b0bd-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b0bd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2b0bd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b0bd-126">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="2b0bd-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="2b0bd-127">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="2b0bd-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="2b0bd-128">Прослушивание на сокете</span><span class="sxs-lookup"><span data-stu-id="2b0bd-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
