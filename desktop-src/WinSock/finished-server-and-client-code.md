---
description: Выполнение примера кода для клиентского и серверного приложения TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Выполнение примера кода клиента и сервера Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991116"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="19a32-103">Выполнение примера кода клиента и сервера Winsock</span><span class="sxs-lookup"><span data-stu-id="19a32-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="19a32-104">В этом разделе содержится полный исходный код для клиентских и серверных приложений TCP/IP:</span><span class="sxs-lookup"><span data-stu-id="19a32-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="19a32-105">Завершение кода клиента Winsock</span><span class="sxs-lookup"><span data-stu-id="19a32-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="19a32-106">Завершение кода сервера Winsock</span><span class="sxs-lookup"><span data-stu-id="19a32-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="19a32-107">Серверное приложение должно быть запущено до запуска клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="19a32-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="19a32-108">Чтобы выполнить сервер, скомпилируйте полный исходный код сервера и запустите исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="19a32-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="19a32-109">Серверное приложение прослушивает TCP-порт 27015 для подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="19a32-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="19a32-110">После подключения клиента сервер получает данные от клиента и выводит (отправляет) данные, полученные обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="19a32-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="19a32-111">Когда клиент завершает подключение, сервер завершает работу сокета клиента, закрывает сокет и завершает работу.</span><span class="sxs-lookup"><span data-stu-id="19a32-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="19a32-112">Чтобы выполнить клиент, скомпилируйте полный исходный код клиента и запустите исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="19a32-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="19a32-113">Клиентское приложение требует, чтобы имя компьютера или IP-адреса компьютера, на котором выполняется серверное приложение, передавалось как параметр командной строки при выполнении клиента.</span><span class="sxs-lookup"><span data-stu-id="19a32-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="19a32-114">Если клиент и сервер выполняются на образце компьютера, клиент можно запустить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19a32-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="19a32-115">**localhost клиента**</span><span class="sxs-lookup"><span data-stu-id="19a32-115">**client localhost**</span></span>

<span data-ttu-id="19a32-116">Клиент пытается подключиться к серверу через TCP-порт 27015.</span><span class="sxs-lookup"><span data-stu-id="19a32-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="19a32-117">После подключения клиента Клиент отправляет данные на сервер и получает от сервера любые данные, отправляемые обратно.</span><span class="sxs-lookup"><span data-stu-id="19a32-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="19a32-118">Затем клиент закрывает сокет и завершает работу.</span><span class="sxs-lookup"><span data-stu-id="19a32-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19a32-119">См. также</span><span class="sxs-lookup"><span data-stu-id="19a32-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a32-120">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="19a32-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



