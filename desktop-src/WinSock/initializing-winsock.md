---
description: Все процессы (приложения или библиотеки DLL), вызывающие функции Winsock, должны инициализировать использование библиотеки DLL Windows Sockets перед выполнением других вызовов функций Winsock. Это также обеспечивает поддержку Winsock в системе.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Инициализация Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541570"
---
# <a name="initializing-winsock"></a><span data-ttu-id="26b43-104">Инициализация Winsock</span><span class="sxs-lookup"><span data-stu-id="26b43-104">Initializing Winsock</span></span>

<span data-ttu-id="26b43-105">Все процессы (приложения или библиотеки DLL), вызывающие функции Winsock, должны инициализировать использование библиотеки DLL Windows Sockets перед выполнением других вызовов функций Winsock.</span><span class="sxs-lookup"><span data-stu-id="26b43-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="26b43-106">Это также обеспечивает поддержку Winsock в системе.</span><span class="sxs-lookup"><span data-stu-id="26b43-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="26b43-107">**Инициализация Winsock**</span><span class="sxs-lookup"><span data-stu-id="26b43-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="26b43-108">Создайте объект [**всадата**](/windows/desktop/api/winsock/ns-winsock-wsadata) с именем всадата.</span><span class="sxs-lookup"><span data-stu-id="26b43-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="26b43-109">Вызовите [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) и верните его значение в виде целого числа и проверьте наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="26b43-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="26b43-110">Функция [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) вызывается для инициации использования WS2 \_32.dll.</span><span class="sxs-lookup"><span data-stu-id="26b43-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="26b43-111">Структура [**всадата**](/windows/desktop/api/winsock/ns-winsock-wsadata) содержит сведения о реализации сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="26b43-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="26b43-112">Параметр МАКЕВОРД (2, 2) [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) отправляет запрос на использование Winsock версии 2,2 в системе и задает переданную версию в качестве наивысшей версии поддержки сокетов Windows, которую может использовать вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="26b43-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="26b43-113">Следующий шаг для клиента: [создание сокета для клиента](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="26b43-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="26b43-114">Следующий шаг для сервера: [создание сокета для сервера](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="26b43-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="26b43-115">См. также</span><span class="sxs-lookup"><span data-stu-id="26b43-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26b43-116">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="26b43-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="26b43-117">Создание базового приложения Winsock</span><span class="sxs-lookup"><span data-stu-id="26b43-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



