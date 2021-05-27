---
title: Уведомления о состоянии сокета WinSock
description: Интерфейсы API уведомлений о состоянии сокетов предоставляют масштабируемый и эффективный способ получения уведомлений об изменениях состояния сокета. Сюда входят такие уведомления, как неблокирующие чтение, неблокирующие записи, условия ошибок и другие сведения.
ms.topic: article
ms.date: 11/18/2020
ms.openlocfilehash: 9ad7f7afcb3dda223b4d54af293bc9a4dd019758
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559992"
---
# <a name="winsock-socket-state-notifications"></a><span data-ttu-id="d3d72-104">Уведомления о состоянии сокета WinSock</span><span class="sxs-lookup"><span data-stu-id="d3d72-104">Winsock socket state notifications</span></span>

## <a name="introduction"></a><span data-ttu-id="d3d72-105">Введение</span><span class="sxs-lookup"><span data-stu-id="d3d72-105">Introduction</span></span>

<span data-ttu-id="d3d72-106">Интерфейсы API уведомлений о состоянии сокетов, приведенные в таблице ниже, предоставляют масштабируемый и эффективный способ получения уведомлений об изменениях состояния сокета (эффективно с точки зрения ЦП и памяти).</span><span class="sxs-lookup"><span data-stu-id="d3d72-106">The socket state notifications APIs in the table below provide you with a scalable and efficient way to obtain notifications about socket state changes (efficient in terms of both CPU and memory).</span></span> <span data-ttu-id="d3d72-107">Сюда входят такие уведомления, как неблокирующие чтение, неблокирующие записи, условия ошибок и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="d3d72-107">This includes notifications about things such as non-blocking read, non-blocking write, error conditions, and other info.</span></span>

|<span data-ttu-id="d3d72-108">API</span><span class="sxs-lookup"><span data-stu-id="d3d72-108">API</span></span>|<span data-ttu-id="d3d72-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d3d72-109">Description</span></span>|
|-|-|
|<span data-ttu-id="d3d72-110">Функция [**процесссоккетнотификатионс**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications)</span><span class="sxs-lookup"><span data-stu-id="d3d72-110">[**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) function</span></span>|<span data-ttu-id="d3d72-111">Связывает набор сокетов с портом завершения и получает все уведомления, которые уже ожидают на этом порту.</span><span class="sxs-lookup"><span data-stu-id="d3d72-111">Associates a set of sockets with a completion port, and retrieves any notifications that are already pending on that port.</span></span> <span data-ttu-id="d3d72-112">После связывания порт завершения получает указанные уведомления о состоянии сокета.</span><span class="sxs-lookup"><span data-stu-id="d3d72-112">Once associated, the completion port receives the socket state notifications that were specified.</span></span>|
|<span data-ttu-id="d3d72-113">Структура [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)</span><span class="sxs-lookup"><span data-stu-id="d3d72-113">[**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration) structure</span></span>|<span data-ttu-id="d3d72-114">Представляет сведения, предоставляемые функции **процесссоккетнотификатионс** .</span><span class="sxs-lookup"><span data-stu-id="d3d72-114">Represents info supplied to the **ProcessSocketNotifications** function.</span></span>|
|<span data-ttu-id="d3d72-115">Функция [**соккетнотификатионретриевивентс**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents)</span><span class="sxs-lookup"><span data-stu-id="d3d72-115">[**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) function</span></span>|<span data-ttu-id="d3d72-116">Эта встроенная вспомогательная функция предоставляется в качестве удобства для получения маски событий из [**OVERLAPPED_ENTRY**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).</span><span class="sxs-lookup"><span data-stu-id="d3d72-116">This inline helper function is provided as a convenience to retrieve the events mask from an [**OVERLAPPED_ENTRY**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped_entry).</span></span>|

<span data-ttu-id="d3d72-117">Рабочий процесс начинается с связывания сокетов с портом завершения ввода-вывода ([**процесссоккетнотификатионс**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) и [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)).</span><span class="sxs-lookup"><span data-stu-id="d3d72-117">The workflow begins with you associating sockets with an I/O completion port ([**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) and [**SOCK_NOTIFY_REGISTRATION**](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)).</span></span> <span data-ttu-id="d3d72-118">После этого порт будет дополнять сведения об изменениях состояния сокетов с помощью обычных методов запроса порта завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="d3d72-118">After that, the port delivers info about socket state changes using the usual I/O completion port query methods.</span></span>

<span data-ttu-id="d3d72-119">Эти интерфейсы API позволяют легко создавать абстракции, независимые от платформы.</span><span class="sxs-lookup"><span data-stu-id="d3d72-119">These APIs allow easy construction of platform-agnostic abstractions.</span></span> <span data-ttu-id="d3d72-120">Таким образом поддерживаются постоянные и одноразовые флаги, а также флажки, активируемые на уровне и на границе.</span><span class="sxs-lookup"><span data-stu-id="d3d72-120">As such, persistent and one-shot, and level- and edge-triggered flags are supported.</span></span> <span data-ttu-id="d3d72-121">Например, для многопоточных серверов рекомендуется использовать одноразовые регистрации, активируемые на уровне одного снимка.</span><span class="sxs-lookup"><span data-stu-id="d3d72-121">For example, one-shot level-triggered registrations are the recommended pattern for multi-threaded servers.</span></span>

## <a name="recommendations"></a><span data-ttu-id="d3d72-122">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="d3d72-122">Recommendations</span></span>

<span data-ttu-id="d3d72-123">Эти API предоставляют масштабируемую альтернативу интерфейсам API [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) и [**SELECT**](/windows/win32/api/winsock2/nf-winsock2-select) .</span><span class="sxs-lookup"><span data-stu-id="d3d72-123">These APIs provide a scalable alternative to the [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/win32/api/winsock2/nf-winsock2-select) APIs.</span></span>

<span data-ttu-id="d3d72-124">Они являются альтернативой [перекрывающейся операции ввода-вывода сокета](/windows/win32/api/winsock2/nf-winsock2-wsasend#overlapped-socket-i-o) , используемой с [портами завершения ввода-вывода](/windows/win32/fileio/i-o-completion-ports), и позволяют избежать необходимости постоянного использования буферов ввода-вывода для каждого сокета.</span><span class="sxs-lookup"><span data-stu-id="d3d72-124">They're an alternative to [overlapped socket I/O](/windows/win32/api/winsock2/nf-winsock2-wsasend#overlapped-socket-i-o) used with [I/O completion ports](/windows/win32/fileio/i-o-completion-ports), and they avoid the need for permanent per-socket I/O buffers.</span></span> <span data-ttu-id="d3d72-125">Но в ситуации, когда буферы ввода-вывода для каждого сокета не являются важным фактором (число сокетов относительно мало или постоянно используются), перекрывающиеся операции ввода-вывода сокетов могут иметь меньше ресурсов, так как это меньшее количество переходов ядра, а также более простая модель.</span><span class="sxs-lookup"><span data-stu-id="d3d72-125">But in a scenario where per-socket I/O buffers aren't an important consideration (the number of sockets is relatively low, or they're constantly used), overlapped socket I/O might have less overhead due to a smaller number of kernel transitions, as well as a simpler model.</span></span>

<span data-ttu-id="d3d72-126">Сокет может быть связан только с одним портом завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="d3d72-126">A socket may be associated with only a single I/O completion port.</span></span> <span data-ttu-id="d3d72-127">Сокет может быть зарегистрирован с портом завершения ввода-вывода только один раз.</span><span class="sxs-lookup"><span data-stu-id="d3d72-127">A socket may be registered with an I/O completion port only once.</span></span> <span data-ttu-id="d3d72-128">Чтобы изменить ключи завершения, отмените регистрацию уведомления, дождитесь **SOCK_NOTIFY_EVENT_REMOVE** сообщения (см. разделы [**процесссоккетнотификатионс**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) и [**соккетнотификатионретриевивентс**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) ), а затем повторно зарегистрируйте сокет.</span><span class="sxs-lookup"><span data-stu-id="d3d72-128">To change completion keys, deregister the notification, wait for the **SOCK_NOTIFY_EVENT_REMOVE** message (see the [**ProcessSocketNotifications**](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications) and [**SocketNotificationRetrieveEvents**](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents) topics), and then re-register the socket.</span></span>

<span data-ttu-id="d3d72-129">Чтобы избежать освобождения памяти, которая еще используется, необходимо освободить структуры данных, связанные с регистрацией, только после получения уведомления **SOCK_NOTIFY_EVENT_REMOVE** для регистрации.</span><span class="sxs-lookup"><span data-stu-id="d3d72-129">To avoid freeing memory that's still in use, you should free a registration's associated data structures only after receiving the **SOCK_NOTIFY_EVENT_REMOVE** notification for the registration.</span></span> <span data-ttu-id="d3d72-130">Когда дескриптор сокета, используемый для регистрации уведомлений, закрывается с помощью функции [функции closesocket](/windows/win32/api/winsock/nf-winsock-closesocket) , его уведомления автоматически отменяются.</span><span class="sxs-lookup"><span data-stu-id="d3d72-130">When the socket descriptor used to register for notifications is closed using the [closesocket](/windows/win32/api/winsock/nf-winsock-closesocket) function, its notifications are automatically deregistered.</span></span> <span data-ttu-id="d3d72-131">Однако уведомления, уже поставленные в очередь, могут по-прежнему доставляться.</span><span class="sxs-lookup"><span data-stu-id="d3d72-131">However, already-queued notifications might still be delivered.</span></span> <span data-ttu-id="d3d72-132">Автоматическая отмена регистрации через **функции closesocket** не приведет к созданию уведомления **SOCK_NOTIFY_EVENT_REMOVE** .</span><span class="sxs-lookup"><span data-stu-id="d3d72-132">An automatic deregistration via **closesocket** won't generate a **SOCK_NOTIFY_EVENT_REMOVE** notification.</span></span>

<span data-ttu-id="d3d72-133">Если требуется Многопотоковая обработка, следует использовать один порт завершения ввода-вывода с несколькими потоками обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d3d72-133">If you want multi-threaded processing, then you should use a single I/O completion port with multiple threads processing notifications.</span></span> <span data-ttu-id="d3d72-134">Это позволяет порту завершения ввода-вывода масштабировать работу по нескольким потокам по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="d3d72-134">This allows the I/O completion port to scale out the work across multiple threads, as necessary.</span></span> <span data-ttu-id="d3d72-135">Избегайте наличия нескольких портов завершения ввода-вывода (например, по одному на поток), так как эта схема уязвима для неограниченного использования в одном потоке, а другие — в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="d3d72-135">Avoid having multiple I/O completion ports (for example, one per thread), because that design is vulnerable to bottle-necking on a single thread while others are idle.</span></span>

<span data-ttu-id="d3d72-136">Если несколько потоков отправляют пакеты уведомлений с уведомлениями, активируемыми на уровне, то **SOCK_NOTIFY_TRIGGER_ONESHOT** должны быть указаны, чтобы избежать нескольких потоков, принимающих уведомления об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="d3d72-136">If multiple threads are dequeuing notification packets with level-triggered notifications, then **SOCK_NOTIFY_TRIGGER_ONESHOT** should be supplied to avoid multiple threads receiving notifications for a state change.</span></span> <span data-ttu-id="d3d72-137">После обработки уведомления сокета необходимо повторно зарегистрировать уведомление.</span><span class="sxs-lookup"><span data-stu-id="d3d72-137">Once the socket notification has been processed, the notification should be re-registered.</span></span>

<span data-ttu-id="d3d72-138">Если несколько потоков отправляют пакеты уведомлений в потоковой среде, где отдельные сообщения должны обрабатываться в одном потоке, рассмотрите возможность использования однозначных уведомлений, активируемых на уровне.</span><span class="sxs-lookup"><span data-stu-id="d3d72-138">If multiple threads are dequeuing notification packets on a stream-oriented connection where individual messages need to be processed on a single thread, then consider using level-triggered one-shot notifications.</span></span> <span data-ttu-id="d3d72-139">Это снижает вероятность того, что несколько потоков получат фрагменты сообщений, которые должны быть повторно собраны между потоками.</span><span class="sxs-lookup"><span data-stu-id="d3d72-139">That reduces the likelihood that multiple threads will receive message fragments that need to be re-assembled cross-thread.</span></span> 

<span data-ttu-id="d3d72-140">Если вы используете уведомления, активируемые с помощью пограничных уведомлений, мы не советуем использовать уведомления одного снимка, так как после включения регистрации сокет необходимо снять.</span><span class="sxs-lookup"><span data-stu-id="d3d72-140">If you're using edge-triggered notifications, then we don't recommend one-shot notifications because the socket needs to be drained after enabling registrations.</span></span> <span data-ttu-id="d3d72-141">Это более сложный шаблон для реализации и является более затратным, поскольку ему всегда требуется вызов, возвращающий **всаеваулдблокк**.</span><span class="sxs-lookup"><span data-stu-id="d3d72-141">This is a more complicated pattern to implement, and is more expensive because it always requires a call that returns **WSAEWOULDBLOCK**.</span></span>

<span data-ttu-id="d3d72-142">Если требуется горизонтальное масштабирование соединения на одном сокете прослушивания, серверы должны использовать функцию [акцептекс](/windows/win32/api/mswsock/nf-mswsock-acceptex) вместо подписки на уведомления для запросов на подключение.</span><span class="sxs-lookup"><span data-stu-id="d3d72-142">If you want connection acceptance scale-out on a single listening socket, then servers should use the [AcceptEx](/windows/win32/api/mswsock/nf-mswsock-acceptex) function instead of subscribing to notifications for connection requests.</span></span> <span data-ttu-id="d3d72-143">Принятие подключений в ответ на уведомления неявно регулирует скорость приема соединения относительно обработки запросов на существующие соединения.</span><span class="sxs-lookup"><span data-stu-id="d3d72-143">Accepting connections in response to notifications implicitly throttles the rate of connection acceptance relative to processing requests for existing connections.</span></span>

<span data-ttu-id="d3d72-144">Ниже приведены примеры кода, иллюстрирующие некоторые сценарии уведомлений о состоянии сокетов.</span><span class="sxs-lookup"><span data-stu-id="d3d72-144">Below are code examples illustrating some socket state notification scenarios.</span></span> <span data-ttu-id="d3d72-145">Часть кода содержит элементы для *выполнения* собственных приложений.</span><span class="sxs-lookup"><span data-stu-id="d3d72-145">Some of the code contains *to do* items for your own applications.</span></span>

## <a name="common-code"></a><span data-ttu-id="d3d72-146">Общий код</span><span class="sxs-lookup"><span data-stu-id="d3d72-146">Common code</span></span>

<span data-ttu-id="d3d72-147">Во-первых, Вот листинг кода, содержащий некоторые общие определения и функции, которые используются в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="d3d72-147">First, here's a code listing that contains some common definitions and functions that are used by the scenarios that follow.</span></span>

```cpp
#include "pch.h"
#include <winsock2.h>
#pragma comment(lib, "Ws2_32")

#define SERVER_ADDRESS          0x0100007f  // localhost
#define SERVER_PORT             0xffff      // TODO: select an actual valid port
#define MAX_TIMEOUT             1000
#define CLIENT_LOOP_COUNT       10

typedef struct SERVER_CONTEXT {
    HANDLE ioCompletionPort;
    SOCKET listenerSocket;
} SERVER_CONTEXT;

typedef struct CLIENT_CONTEXT {
    UINT32 transmitCount;
} CLIENT_CONTEXT;

SRWLOCK g_printLock = SRWLOCK_INIT;

VOID DestroyServerContext(_Inout_ _Post_invalid_ SERVER_CONTEXT* serverContext) {
    if (serverContext->listenerSocket != INVALID_SOCKET) {
        closesocket(serverContext->listenerSocket);
    }

    if (serverContext->ioCompletionPort != NULL) {
        CloseHandle(serverContext->ioCompletionPort);
    }

    free(serverContext);
}

DWORD CreateServerContext(_Outptr_ SERVER_CONTEXT** serverContext) {
    DWORD errorCode;
    SERVER_CONTEXT* localContext = NULL;
    sockaddr_in serverAddress = { };

    localContext = (SERVER_CONTEXT*)malloc(sizeof(*localContext));
    if (localContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(localContext, sizeof(*localContext));
    localContext->listenerSocket = INVALID_SOCKET;


    localContext->ioCompletionPort = CreateIoCompletionPort(INVALID_HANDLE_VALUE, NULL, 0, 0);
    if (localContext->ioCompletionPort == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    localContext->listenerSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (localContext->listenerSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (bind(localContext->listenerSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    if (listen(localContext->listenerSocket, 0) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    *serverContext = localContext;
    localContext = NULL;
    errorCode = ERROR_SUCCESS;

Exit:
    if (localContext != NULL) {
        DestroyServerContext(localContext);
    }

    return errorCode;
}

// Create a socket, connect to the server, send transmitCount copies of the
// payload, then disconnect.
DWORD
WINAPI
ClientThreadRoutine(_In_ PVOID clientContextPointer) {
    const UINT32 payload = 0xdeadbeef;
    CLIENT_CONTEXT* clientContext = (CLIENT_CONTEXT*)clientContextPointer;

    sockaddr_in serverAddress = {};
    SOCKET clientSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (clientSocket == INVALID_SOCKET) {
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (connect(clientSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        goto Exit;
    }

    for (UINT32 Index = 0; Index < clientContext->transmitCount; Index += 1) {
        if (send(clientSocket, (const char*)&payload, sizeof(payload), 0) < 0) {
            goto Exit;
        }
    }

    if (shutdown(clientSocket, SD_BOTH) != 0) {
        goto Exit;
    }

Exit:
    if (clientSocket != INVALID_SOCKET) {
        closesocket(INVALID_SOCKET);
    }

    free(clientContext);

    return 0;
}

DWORD CreateClientThread(_In_ UINT32 transmitCount) {
    DWORD errorCode = ERROR_SUCCESS;
    CLIENT_CONTEXT* clientContext = NULL;
    HANDLE clientThread = NULL;

    clientContext = (CLIENT_CONTEXT*)malloc(sizeof(*clientContext));
    if (clientContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(clientContext, sizeof(*clientContext));
    clientContext->transmitCount = transmitCount;

    clientThread = CreateThread(NULL, 0, ClientThreadRoutine, clientContext, 0, NULL);
    if (clientThread == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    clientContext = NULL;

Exit:
    if (clientContext != NULL) {
        free(clientContext);
    }

    if (clientThread != NULL) {
        CloseHandle(clientThread);
    }

    return errorCode;
}

VOID PrintError(DWORD errorCode) {
    AcquireSRWLockExclusive(&g_printLock);

    wprintf_s(L"Server thread %d encountered an error %d.", GetCurrentThreadId(), errorCode);
    WCHAR errorString[512];
    if (FormatMessageW(FORMAT_MESSAGE_FROM_SYSTEM,
        NULL,
        errorCode,
        0,
        errorString,
        RTL_NUMBER_OF(errorString),
        NULL) != 0)
    {
        wprintf_s(L"%s", errorString);
    }

    ReleaseSRWLockExclusive(&g_printLock);
}

// This routine must be used only if a single socket is registered. 
DWORD DeregisterAndWait(_In_ HANDLE ioCompletionPort, _In_ SOCKET socket) {
    DWORD errorCode;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    UINT32 notificationCount;

    // Keep looping until the registration is removed, or a timeout is hit.
    while (TRUE) {

        registration.operation = SOCK_NOTIFY_OP_REMOVE;
        registration.socket = socket;
        errorCode = ProcessSocketNotifications(ioCompletionPort,
            1,
            &registration,
            MAX_TIMEOUT,
            1,
            &notification,
            &notificationCount);

        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }

        if (registration.registrationResult != ERROR_SUCCESS) {
            errorCode = registration.registrationResult;
            goto Exit;
        }

        // Drops all non-removal notifications. Must be used only
        // if a single socket is registered.
        if (SocketNotificationRetrieveEvents(&notification) & SOCK_NOTIFY_EVENT_REMOVE) {
            break;
        }
    }

Exit:
    return errorCode;
}
```

## <a name="simple-replacement-for-polling"></a><span data-ttu-id="d3d72-148">Простая замена для опроса</span><span class="sxs-lookup"><span data-stu-id="d3d72-148">Simple replacement for polling</span></span>

<span data-ttu-id="d3d72-149">Этот сценарий демонстрирует замену для приложений, использующих опрос ([**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)) или аналогичных API.</span><span class="sxs-lookup"><span data-stu-id="d3d72-149">This scenario demonstrates a drop-in replacement for applications using poll ([**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)) or similar APIs.</span></span> <span data-ttu-id="d3d72-150">Он является однопотоковым и использует постоянные (не одноразовые) регистрации.</span><span class="sxs-lookup"><span data-stu-id="d3d72-150">It's single-threaded, and makes use of persistent (not one-shot) registrations.</span></span> <span data-ttu-id="d3d72-151">Так как регистрация не требует повторной регистрации, она использует [**жеткуеуедкомплетионстатусекс**](/windows/win32/fileio/getqueuedcompletionstatusex-func) для вывода уведомлений из очереди.</span><span class="sxs-lookup"><span data-stu-id="d3d72-151">Because the registration doesn't need to be re-registered, it uses [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) to dequeue notifications.</span></span>

```cpp
VOID SimplePollReplacement() {
    DWORD errorCode;
    WSADATA wsaData;
    SERVER_CONTEXT* serverContext = NULL;
    SOCKET tcpAcceptSocket = INVALID_SOCKET;
    u_long nonBlocking = 1;
    SOCKET currentSocket;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    ULONG notificationCount;
    UINT32 events;
    CHAR dataBuffer[512];

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    errorCode = CreateServerContext(&serverContext);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    tcpAcceptSocket = accept(serverContext->listenerSocket, NULL, NULL);
    if (tcpAcceptSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    if (ioctlsocket(tcpAcceptSocket, FIONBIO, &nonBlocking) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Register the accepted connection.
    registration.completionKey = (PVOID)tcpAcceptSocket;
    registration.eventFilter = SOCK_NOTIFY_REGISTER_EVENT_IN | SOCK_NOTIFY_REGISTER_EVENT_HANGUP;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_LEVEL;
    registration.socket = tcpAcceptSocket;
    errorCode = ProcessSocketNotifications(serverContext->ioCompletionPort,
        1,
        &registration,
        0,
        0,
        NULL,
        NULL);

    // Make sure all registrations were processed.
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Make sure each registration was successful.
    if (registration.registrationResult != ERROR_SUCCESS) {
        errorCode = registration.registrationResult;
        goto Exit;
    }

    // Keep receiving data until the client disconnects.
    while (TRUE) {

        wprintf_s(L"Waiting for client action...\r\n");

        if (!GetQueuedCompletionStatusEx(serverContext->ioCompletionPort,
            &notification,
            1,
            &notificationCount,
            MAX_TIMEOUT,
            FALSE))
        {
            errorCode = GetLastError();
            goto Exit;
        }

        // The completion key is the socket we supplied above.
        //
        // This is true only because the registration supplied the socket as the completion
        // key. A more typical pattern is to supply a context pointer. This example supplies
        // the socket directly, for simplicity.
        //
        // The events are stored in the number-of-bytes-received field.
        events = SocketNotificationRetrieveEvents(&notification);

        currentSocket = (SOCKET)notification.lpCompletionKey;
        if (events & SOCK_NOTIFY_EVENT_IN) {

            // We don't check for a 0-size receive because we subscribed to hang-up notifications.
            if (recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0) < 0) {
                errorCode = GetLastError();
                goto Exit;
            }

            wprintf_s(L"Received client data.\r\n");
        }

        if (events & SOCK_NOTIFY_EVENT_HANGUP) {
            wprintf_s(L"Client hung up. Exiting. \r\n");
            break;
        }

        if (events & SOCK_NOTIFY_EVENT_ERR) {
            wprintf_s(L"The socket was ungracefully reset or another error occurred. Exiting.\r\n");
            // Obtain a more detailed error code by issuing a non-blocking receive.
            recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            errorCode = GetLastError();
            goto Exit;
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
    }

    if (serverContext != NULL) {
        if (tcpAcceptSocket != INVALID_SOCKET) {
            DeregisterAndWait(serverContext->ioCompletionPort, tcpAcceptSocket);
        }

        DestroyServerContext(serverContext);
    }

    if (tcpAcceptSocket != INVALID_SOCKET) {
        closesocket(tcpAcceptSocket);
    }

    WSACleanup();
}
```

## <a name="edge-triggered-udp-server"></a><span data-ttu-id="d3d72-152">Сервер UDP, активируемый с пограничным сервером</span><span class="sxs-lookup"><span data-stu-id="d3d72-152">Edge-triggered UDP server</span></span>

<span data-ttu-id="d3d72-153">Это простая иллюстрация использования API-интерфейсов с помощью пограничных триггеров.</span><span class="sxs-lookup"><span data-stu-id="d3d72-153">This is a simple illustration of how to use the APIs with edge-triggering.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3d72-154">Сервер должен получать получение, пока он не получит **всаеваулдблокк**.</span><span class="sxs-lookup"><span data-stu-id="d3d72-154">The server must keep receiving until it receives a **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="d3d72-155">В противном случае невозможно гарантировать, что будет наблюдаться повышенная граница.</span><span class="sxs-lookup"><span data-stu-id="d3d72-155">Otherwise, it can't be sure that a rising edge will be observed.</span></span> <span data-ttu-id="d3d72-156">Таким образом, сокет сервера также должен быть не заблокирован.</span><span class="sxs-lookup"><span data-stu-id="d3d72-156">As such, the server's socket must also be non-blocking.</span></span>

<span data-ttu-id="d3d72-157">В этом примере используется протокол UDP для демонстрации отсутствия уведомления о **разрыве соединения** .</span><span class="sxs-lookup"><span data-stu-id="d3d72-157">This example uses UDP to demonstrate the lack of a **HANGUP** notification.</span></span> <span data-ttu-id="d3d72-158">Он принимает некоторые вольностей, предполагая, что общие вспомогательные методы создают сокеты UDP при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d3d72-158">It takes some liberties with assuming the common helpers create UDP sockets if needed.</span></span>

```cpp
// This example assumes that substantially similar helpers are available for UDP sockets.
VOID SimpleEdgeTriggeredSample() {
    DWORD errorCode;
    WSADATA wsaData;
    SOCKET serverSocket = INVALID_SOCKET;
    SOCKET currentSocket;
    HANDLE ioCompletionPort = NULL;
    sockaddr_in serverAddress = { };
    u_long nonBlocking = 1;
    SOCK_NOTIFY_REGISTRATION registration = {};
    OVERLAPPED_ENTRY notification;
    ULONG notificationCount;
    UINT32 events;
    CHAR dataBuffer[512];
    UINT32 datagramCount;
    int receiveResult;

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    ioCompletionPort = CreateIoCompletionPort(INVALID_HANDLE_VALUE, NULL, 0, 0);
    if (ioCompletionPort == NULL) {
        errorCode = GetLastError();
        goto Exit;
    }

    serverSocket = socket(AF_INET, SOCK_DGRAM, IPPROTO_UDP);
    if (serverSocket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Register the server UDP socket before binding to a port to ensure data doesn't become
    // present before the registration. Otherwise, the server could miss the notification and
    // hang.
    //
    // Edge-triggered is not recommended with one-shot due to the difficulty in re-registering.
    registration.completionKey = (PVOID)serverSocket;
    registration.eventFilter = SOCK_NOTIFY_EVENT_IN;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_EDGE;
    registration.socket = serverSocket;
    errorCode = ProcessSocketNotifications(ioCompletionPort, 1, &registration, 0, 0, NULL, NULL);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    if (registration.registrationResult != ERROR_SUCCESS) {
        errorCode = registration.registrationResult;
        goto Exit;
    }

    // Use non-blocking sockets with edge-triggered notifications, since the data must be
    // drained before a rising edge can be observed again.
    errorCode = ioctlsocket(serverSocket, FIONBIO, &nonBlocking);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    serverAddress.sin_family = AF_INET;
    serverAddress.sin_addr.s_addr = SERVER_ADDRESS;
    serverAddress.sin_port = SERVER_PORT;
    if (bind(serverSocket, (sockaddr*)&serverAddress, sizeof(serverAddress)) != 0) {
        errorCode = GetLastError();
        goto Exit;
    }

    // Create the client.
    // While CreateClientThread connects to a TCP socket and sends data over it, for this example
    // assume that CreateClientThread creates a UDP socket instead, and sends data over it.
    errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Receive the packets.
    datagramCount = 0;
    while (datagramCount < CLIENT_LOOP_COUNT) {

        wprintf_s(L"Waiting for client action...\r\n");

        if (!GetQueuedCompletionStatusEx(ioCompletionPort,
            &notification,
            1,
            &notificationCount,
            MAX_TIMEOUT,
            FALSE))
        {
            errorCode = GetLastError();
            goto Exit;
        }

        // The completion key is the socket we supplied above.
        //
        // This is true only because the registration supplied the socket as the completion
        // key. A more typical pattern is to supply a context pointer. This example supplies
        // the socket directly, for simplicity.
        //
        // The events are the integer value of the overlapped pointer.
        events = SocketNotificationRetrieveEvents(&notification);

        currentSocket = (SOCKET)notification.lpCompletionKey;
        if (events & SOCK_NOTIFY_EVENT_ERR) {
            // Obtain a more detailed error code by issuing a non-blocking receive.
            recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            errorCode = GetLastError();
            goto Exit;
        }

        if ((events & SOCK_NOTIFY_EVENT_IN) == 0) {
            continue;
        }

        // Keep looping receiving data until the read would block, otherwise the edge may not
        // have been reset.
        while (TRUE) {
            receiveResult = recv(currentSocket, dataBuffer, sizeof(dataBuffer), 0);
            if (receiveResult < 0) {
                errorCode = GetLastError();
                if (errorCode != WSAEWOULDBLOCK) {
                    goto Exit;
                }

                break;
            }

            datagramCount += 1;
            wprintf_s(L"Received client data.\r\n");
        }
    }

    wprintf_s(L"Received all data. Exiting... \r\n");
    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
    }

    if (serverSocket != INVALID_SOCKET) {
        if (ioCompletionPort != NULL) {
            DeregisterAndWait(ioCompletionPort, serverSocket);
        }

        closesocket(serverSocket);
    }

    if (ioCompletionPort != NULL) {
        CloseHandle(ioCompletionPort);
    }

    WSACleanup();
}
```

## <a name="multi-threaded-server"></a><span data-ttu-id="d3d72-159">Многопоточный сервер</span><span class="sxs-lookup"><span data-stu-id="d3d72-159">Multi-threaded server</span></span>

<span data-ttu-id="d3d72-160">В этом примере показан более реалистичный многопотоковый шаблон использования, использующий возможности горизонтального масштабирования порта завершения ввода-вывода для распределения работы между несколькими потоками сервера.</span><span class="sxs-lookup"><span data-stu-id="d3d72-160">This example demonstrates a more realistic multi-threaded use pattern that uses the I/O completion port's scale-out capabilities to distribute work across multiple server threads.</span></span> <span data-ttu-id="d3d72-161">Сервер использует триггеры на уровне однократного выполнения, чтобы избежать отправки несколькими потоками уведомлений для одного и того же сокета, а также для того, чтобы каждый поток запускал полученные данные по одному блоку за раз.</span><span class="sxs-lookup"><span data-stu-id="d3d72-161">The server uses one-shot level-triggering to avoid multiple threads picking up notifications for the same socket, and to allow each thread to drain received data one chunk at a time.</span></span>

<span data-ttu-id="d3d72-162">В нем также демонстрируются некоторые распространенные шаблоны, используемые с портом завершения.</span><span class="sxs-lookup"><span data-stu-id="d3d72-162">It also demonstrates some common patterns used with the completion port.</span></span> <span data-ttu-id="d3d72-163">Ключ завершения используется для предоставления указателя контекста для каждого сокета.</span><span class="sxs-lookup"><span data-stu-id="d3d72-163">The completion key is used to supply a per-socket context pointer.</span></span> <span data-ttu-id="d3d72-164">Указатель контекста имеет заголовок, описывающий используемый тип сокета, поэтому для одного порта завершения можно использовать несколько типов сокетов.</span><span class="sxs-lookup"><span data-stu-id="d3d72-164">The context pointer has a header that describes the type of socket being used, so that multiple sockets types can be used on a single completion port.</span></span> <span data-ttu-id="d3d72-165">Комментарии в примере выделяют, что произвольные завершения могут быть выведены из очереди (как и в случае функции [**жеткуеуедкомплетионстатусекс**](/windows/win32/fileio/getqueuedcompletionstatusex-func) ), а не только с уведомлениями сокета.</span><span class="sxs-lookup"><span data-stu-id="d3d72-165">Comments in the example highlight that arbitrary completions can be dequeued (just as with the [**GetQueuedCompletionStatusEx**](/windows/win32/fileio/getqueuedcompletionstatusex-func) function), not only socket notifications.</span></span> <span data-ttu-id="d3d72-166">API [**PostQueuedCompletionStatus**](/windows/win32/fileio/postqueuedcompletionstatus) используется для отправки сообщений в потоки и их пробуждения без ожидания получения уведомления сокета.</span><span class="sxs-lookup"><span data-stu-id="d3d72-166">The [**PostQueuedCompletionStatus**](/windows/win32/fileio/postqueuedcompletionstatus) API is used to post messages to threads, and wake them without having to wait for the arrival of a socket notification.</span></span>

<span data-ttu-id="d3d72-167">Наконец, в примере демонстрируются некоторые сложности правильной отмены регистрации и очистки контекстов сокетов в потоковой нагрузке.</span><span class="sxs-lookup"><span data-stu-id="d3d72-167">Finally, the example demonstrates some of the intricacies of correctly deregistering and cleaning up socket contexts in a threaded workload.</span></span> <span data-ttu-id="d3d72-168">В этом примере контекст сокета неявно принадлежит потоку, который получает уведомление.</span><span class="sxs-lookup"><span data-stu-id="d3d72-168">In this example, socket context is implicitly owned by the thread that receives the notification.</span></span> <span data-ttu-id="d3d72-169">Поток сохраняет владение, если не удается зарегистрировать уведомление.</span><span class="sxs-lookup"><span data-stu-id="d3d72-169">The thread maintains ownership if it fails to register the notification.</span></span>

```cpp
#define CLIENT_THREAD_COUNT         100
// The I/O completion port infrastructure ensures that the system isn't over-subscribed by
// ensuring server-side threads block if they exceed the number of logical processors. If the
// machine has more than 16 logical processors, then this can be observed by increasing this number.
#define SERVER_THREAD_COUNT         16
#define SERVER_DEQUEUE_COUNT        3
#define SERVER_EXIT_KEY             ((ULONG_PTR)-1)

typedef struct SERVER_THREAD_CONTEXT {
    SERVER_CONTEXT* commonContext;
    SRWLOCK stateLock;
    _Guarded_by_(stateLock) UINT32 deregisterCount;
    _Guarded_by_(stateLock) BOOLEAN shouldExit;
} SERVER_THREAD_CONTEXT;

typedef enum SOCKET_TYPE {
    SOCKET_TYPE_LISTENER,
    SOCKET_TYPE_ACCEPT
} SOCKET_TYPE;

typedef struct SOCKET_CONTEXT {
    SOCKET_TYPE socketType;
    SOCKET socket;
} SOCKET_CONTEXT;

VOID CancelServerThreadsAsync(_Inout_ SERVER_THREAD_CONTEXT* serverThreadContext) {
    AcquireSRWLockExclusive(&serverThreadContext->stateLock);
    serverThreadContext->shouldExit = TRUE;
    ReleaseSRWLockExclusive(&serverThreadContext->stateLock);
}

VOID IndicateServerThreadExit(_In_ HANDLE ioCompletionPort) {
    // Notify a server thread that it needs to exit. It can then notify the other threads when it
    // exits.
    //
    // If this fails, then server threads may hang, and this program will never terminate. That
    // is an unrecoverable error.
    if (!PostQueuedCompletionStatus(ioCompletionPort, 0, SERVER_EXIT_KEY, NULL)) {
        RaiseFailFastException(NULL, NULL, 0);
    }
}

VOID DestroySocketContext(_Inout_ _Post_invalid_ SOCKET_CONTEXT* socketContext) {
    if (socketContext->socket != INVALID_SOCKET) {
        closesocket(socketContext->socket);
    }

    free(socketContext);
}

DWORD AcceptConnection(_In_ SOCKET listenSocket, _Outptr_ SOCKET_CONTEXT** socketContextOut) {
    DWORD errorCode;
    SOCKET_CONTEXT* socketContext = NULL;

    socketContext = (SOCKET_CONTEXT*)malloc(sizeof(*socketContext));
    if (socketContext == NULL) {
        errorCode = ERROR_NOT_ENOUGH_MEMORY;
        goto Exit;
    }

    ZeroMemory(socketContext, sizeof(*socketContext));
    socketContext->socketType = SOCKET_TYPE_ACCEPT;
    socketContext->socket = accept(listenSocket, NULL, NULL);
    if (socketContext->socket == INVALID_SOCKET) {
        errorCode = GetLastError();
        goto Exit;
    }

    *socketContextOut = socketContext;
    socketContext = NULL;

Exit:
    if (socketContext != NULL) {
        _ASSERT(errorCode != ERROR_SUCCESS);
        DestroySocketContext(socketContext);
    }

    return errorCode;
}

DWORD
WINAPI
ServerThreadRoutine(_In_ PVOID serverThreadContextPointer) {
    DWORD errorCode;
    SERVER_THREAD_CONTEXT* serverThreadContext;
    HANDLE ioCompletionPort;
    // Accepting a connection requires two registrations: one to re-enable the listening socket
    // notification, and one to register the newly-accepted connection.
    SOCK_NOTIFY_REGISTRATION registrationBuffer[SERVER_DEQUEUE_COUNT * 2];
    UINT32 registrationCount;
    SOCK_NOTIFY_REGISTRATION* registration;
    OVERLAPPED_ENTRY notifications[SERVER_DEQUEUE_COUNT];
    UINT32 notificationCount;
    UINT32 events;
    SOCKET_CONTEXT* socketContext;
    SOCKET_CONTEXT* acceptedContext;
    BOOLEAN shouldExit;
    CHAR dataBuffer[512];

    serverThreadContext = (SERVER_THREAD_CONTEXT*)serverThreadContextPointer;
    ioCompletionPort = serverThreadContext->commonContext->ioCompletionPort;

    // Boot-strap the loop process.
    registrationCount = 0;

    // Keep looping, processing notifications until exit has been requested.
    while (TRUE) {

        AcquireSRWLockExclusive(&serverThreadContext->stateLock);
        shouldExit = serverThreadContext->shouldExit;
        ReleaseSRWLockExclusive(&serverThreadContext->stateLock);
        if (shouldExit) {
            goto Exit;
        }

        AcquireSRWLockExclusive(&g_printLock);
        wprintf_s(L"Server thread %d waiting for client action...\r\n", GetCurrentThreadId());
        ReleaseSRWLockExclusive(&g_printLock);

        // Process notifications and re-register one-shot notifications that were processed on a
        // previous iteration.
        errorCode = ProcessSocketNotifications(ioCompletionPort,
            registrationCount,
            (registrationCount == 0) ? NULL : registrationBuffer,
            MAX_TIMEOUT,
            RTL_NUMBER_OF(notifications),
            notifications,
            &notificationCount);

        // TODO: Production code should handle failure better. This can fail due to transient memory conditions, or due to
        // invalid input such as a bad handle. Retrying in case the memory conditions abate is
        // a reasonable strategy.
        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }

        // Check whether any registrations failed, and attempt to clean up if they did.
        errorCode = ERROR_SUCCESS;
        for (UINT32 i = 0; i < registrationCount; i += 1) {
            registration = &registrationBuffer[i];
            if (registration->registrationResult == ERROR_SUCCESS) {
                continue;
            }

            // Preserve the first failure code.
            if (errorCode == ERROR_SUCCESS) {
                errorCode = registration->registrationResult;
            }

            // All the registrations are oneshot, so if the registration failed, then only this thread
            // has access to the context. Attempt to clean up fully:
            // - The listening socket is owned by the main thread, so ignore that.
            // - If the socket hasn't been registered, just free its memory.
            // - Otherwise, attempt to deregister it.

            socketContext = (SOCKET_CONTEXT*)registration->completionKey;
            if (socketContext->socketType == SOCKET_TYPE_LISTENER) {
                continue;
            }

            // Best-effort de-registration. In case of failure, simply get rid of the socket and
            // context. This is safe to do because the notification for the socket can't be enabled.
            // Either it was never registered in the first place, or re-registration failed, and it
            // was previously disabled by nature of being a one-shot registration.
            registration->operation = SOCK_NOTIFY_OP_REMOVE;
            errorCode = ProcessSocketNotifications(ioCompletionPort,
                1,
                registration,
                0,
                0,
                NULL,
                NULL);

            if ((errorCode != ERROR_SUCCESS) ||
                (registration->registrationResult != ERROR_SUCCESS)) {
                DestroySocketContext(socketContext);
            }
        }

        // Process the notifications. Many will need to be re-enabled because they are one-shot,
        // so ensure that we can build that incrementally.
        registrationCount = 0;
        ZeroMemory(registrationBuffer, sizeof(registrationBuffer));

        for (UINT32 i = 0; i < notificationCount; i += 1) {
            if (notifications[i].lpCompletionKey == SERVER_EXIT_KEY) {
                _ASSERT(serverThreadContext->shouldExit);

                // On exit, this thread will post the next exit message.
                errorCode = ERROR_SUCCESS;
                goto Exit;
            }

            socketContext = (SOCKET_CONTEXT*)notifications[i].lpCompletionKey;
            events = SocketNotificationRetrieveEvents(&notifications[i]);

            // Process the socket notification, taking socket-specific actions.
            switch (socketContext->socketType) {
            case SOCKET_TYPE_LISTENER:

                // Accepting connections in response to notifications implicitly throttles
                // the rate at which incoming connections are accepted, and limits scale-out for
                // new connection acceptance. Consider using AcceptEx if greater scaling of
                //connection acceptance is desired.

                // Perform an accept regardless of the notification. The only possible notifications
                // are for available connections or error conditions. Any possible error conditions
                // will be processed as part of the accept.
                errorCode = AcceptConnection(socketContext->socket, &acceptedContext);
                if (errorCode == ERROR_SUCCESS) {
                    // Register the accepted connection.
                    registration = &registrationBuffer[registrationCount];
                    registration->socket = acceptedContext->socket;
                    registration->completionKey = acceptedContext;
                    registration->eventFilter = SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_HANGUP;
                    registration->operation =
                        SOCK_NOTIFY_OP_ENABLE;
                    registration->triggerFlags = SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                    registrationCount += 1;
                }

                // Re-arm the existing listening socket registration.
                registration = &registrationBuffer[registrationCount];
                registration->socket = socketContext->socket;
                registration->completionKey = socketContext;
                registration->eventFilter = SOCK_NOTIFY_EVENT_IN;
                registration->operation =
                    SOCK_NOTIFY_OP_ENABLE;
                registration->triggerFlags = SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                registrationCount += 1;
                break;

            case SOCKET_TYPE_ACCEPT:
                // The registration was removed. Clean up the context.
                if (events & SOCK_NOTIFY_EVENT_REMOVE) {
                    AcquireSRWLockExclusive(&serverThreadContext->stateLock);
                    serverThreadContext->deregisterCount += 1;
                    if (serverThreadContext->deregisterCount >= CLIENT_THREAD_COUNT) {
                        serverThreadContext->shouldExit = TRUE;
                    }
                    ReleaseSRWLockExclusive(&serverThreadContext->stateLock);

                    DestroySocketContext(socketContext);
                    continue;
                }

                registration = &registrationBuffer[registrationCount];

                // If a hangup occurred, then remove the registration. 
                if (events & SOCK_NOTIFY_EVENT_HANGUP) {
                    registration->eventFilter = 0;
                    registration->operation = SOCK_NOTIFY_OP_REMOVE;
                }

                // Receive data.
                if (events & (SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_ERR)) {
                    // TODO: Handle errors (for example, due to connection reset). The error from recv can
                    // be used to retrieve the underlying socket for a SOCK_NOTIFY_EVENT_ERR.
                    if (recv(socketContext->socket, dataBuffer, sizeof(dataBuffer), 0) < 0) {
                        registration->operation = SOCK_NOTIFY_OP_REMOVE;
                        registration->eventFilter = 0;
                    }
                    else {
                        registration->operation |=
                            SOCK_NOTIFY_OP_ENABLE;
                        registration->triggerFlags =
                            SOCK_NOTIFY_TRIGGER_ONESHOT | SOCK_NOTIFY_TRIGGER_LEVEL;
                        registration->eventFilter = SOCK_NOTIFY_EVENT_IN | SOCK_NOTIFY_EVENT_HANGUP;
                    }
                }

                registration->socket = socketContext->socket;
                registration->completionKey = socketContext;
                registrationCount += 1;
                break;

                // TODO:
                //
                // Other (potentially non-socket) I/O completion can be processed here. For instance,
                // this could also be processing disk I/O. The contexts will need to have a common
                // header that can be used to differentiate between the different context types,
                // similar to how the listening and accepted sockets are differentiated.
                //
                // case ... :

            default:
                _ASSERT(!"Unexpected socket type!");
                errorCode = ERROR_UNIDENTIFIED_ERROR;
                goto Exit;
            }
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    // If an error occurred, then ensure the other threads know they should exit.
    // TODO: use an error handling strategy that isn't just exiting.
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);
        CancelServerThreadsAsync(serverThreadContext);
    }

    // Wake a remaining server thread.
    IndicateServerThreadExit(ioCompletionPort);

    AcquireSRWLockExclusive(&g_printLock);
    wprintf_s(L"Server thread %d exited\r\n", GetCurrentThreadId());
    ReleaseSRWLockExclusive(&g_printLock);

    return errorCode;
}

VOID MultiThreadedTcpServer() {
    DWORD errorCode;
    WSADATA wsaData;
    SERVER_THREAD_CONTEXT serverContext = { NULL, SRWLOCK_INIT, 0, FALSE };
    SOCKET_CONTEXT listenContext = {};
    SOCK_NOTIFY_REGISTRATION registration = {};
    HANDLE serverThreads[SERVER_THREAD_COUNT] = {};
    UINT32 serverThreadCount = 0;

    if (WSAStartup(WINSOCK_VERSION, &wsaData) != 0) {
        errorCode = GetLastError();
        PrintError(errorCode);
        return;
    }

    listenContext.socket = INVALID_SOCKET;
    listenContext.socketType = SOCKET_TYPE_LISTENER;
    errorCode = CreateServerContext(&serverContext.commonContext);
    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Register the listening socket with the I/O completion port so the server threads are notified
    // of incoming connections.
    listenContext.socket = serverContext.commonContext->listenerSocket;
    registration.completionKey = &listenContext;
    registration.eventFilter = SOCK_NOTIFY_EVENT_IN;
    registration.operation = SOCK_NOTIFY_OP_ENABLE;
    registration.triggerFlags = SOCK_NOTIFY_TRIGGER_LEVEL | SOCK_NOTIFY_TRIGGER_PERSISTENT;
    registration.socket = listenContext.socket;
    errorCode = ProcessSocketNotifications(serverContext.commonContext->ioCompletionPort,
        1,
        &registration,
        0,
        0,
        NULL,
        NULL);

    if (errorCode != ERROR_SUCCESS) {
        goto Exit;
    }

    // Create the server threads. These are likely over-subscribed, but the I/O completion port
    // ensures that they scale appropriately.
    while (serverThreadCount < RTL_NUMBER_OF(serverThreads)) {
        serverThreads[serverThreadCount] =
            CreateThread(NULL, 0, ServerThreadRoutine, &serverContext, 0, NULL);

        if (serverThreads[serverThreadCount] == NULL) {
            errorCode = GetLastError();
            goto Exit;
        }
    }

    // Create the client threads, which are badly over-subscribed.
    for (UINT32 i = 0; i < CLIENT_THREAD_COUNT; i += 1) {
        errorCode = CreateClientThread(CLIENT_LOOP_COUNT);
        if (errorCode != ERROR_SUCCESS) {
            goto Exit;
        }
    }

    errorCode = ERROR_SUCCESS;

Exit:
    if (errorCode != ERROR_SUCCESS) {
        PrintError(errorCode);

        // In case of error, ensure that all server threads know to exit.
        if (serverContext.commonContext != NULL) {
            CancelServerThreadsAsync(&serverContext);
            IndicateServerThreadExit(serverContext.commonContext->ioCompletionPort);
        }
    }

    if (serverThreadCount > 0) {
        wprintf_s(L"Waiting for %d server threads to exit...\r\n", serverThreadCount);
        errorCode = WaitForMultipleObjects(serverThreadCount, serverThreads, TRUE, INFINITE);
        _ASSERT(errorCode == ERROR_SUCCESS);
    }

    // TODO: In case of failure, clean up remaining state. For example, Accepted connections can be kept in
    // a global list, which can be closed from this thread.

    for (UINT32 i = 0; i < serverThreadCount; i += 1) {
        CloseHandle(serverThreads[i]);
    }

    DestroyServerContext(serverContext.commonContext);

    WSACleanup();
}
```

## <a name="see-also"></a><span data-ttu-id="d3d72-170">См. также</span><span class="sxs-lookup"><span data-stu-id="d3d72-170">See also</span></span>

* [<span data-ttu-id="d3d72-171">процесссоккетнотификатионс</span><span class="sxs-lookup"><span data-stu-id="d3d72-171">ProcessSocketNotifications</span></span>](/windows/win32/api/winsock2/nf-winsock2-processsocketnotifications)
* [<span data-ttu-id="d3d72-172">SOCK_NOTIFY_REGISTRATION</span><span class="sxs-lookup"><span data-stu-id="d3d72-172">SOCK_NOTIFY_REGISTRATION</span></span>](/windows/win32/api/winsock2/ns-winsock2-sock_notify_registration)
* [<span data-ttu-id="d3d72-173">соккетнотификатионретриевивентс</span><span class="sxs-lookup"><span data-stu-id="d3d72-173">SocketNotificationRetrieveEvents</span></span>](/windows/win32/api/winsock2/nf-winsock2-socketnotificationretrieveevents)
