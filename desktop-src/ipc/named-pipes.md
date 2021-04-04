---
description: Именованный канал — это именованный односторонний или дуплексный канал для обмена данными между сервером канала и одним или несколькими клиентами канала.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Именованные каналы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998648"
---
# <a name="named-pipes"></a><span data-ttu-id="05463-103">Именованные каналы</span><span class="sxs-lookup"><span data-stu-id="05463-103">Named Pipes</span></span>

<span data-ttu-id="05463-104">*Именованный канал* — это именованный односторонний или дуплексный канал для обмена данными между сервером канала и одним или несколькими клиентами канала.</span><span class="sxs-lookup"><span data-stu-id="05463-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="05463-105">Все экземпляры именованного канала имеют одинаковое имя канала, но каждый экземпляр имеет собственные буферы и дескрипторы, а также предоставляет отдельный канал для обмена данными между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="05463-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="05463-106">Использование экземпляров позволяет нескольким клиентам каналов одновременно использовать один и тот же именованный канал.</span><span class="sxs-lookup"><span data-stu-id="05463-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="05463-107">Любой процесс может обращаться к именованным каналам в соответствии с проверкой безопасности, делая именованные каналы простой формой взаимодействия между связанными или несвязанными процессами.</span><span class="sxs-lookup"><span data-stu-id="05463-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="05463-108">Любой процесс может действовать как сервер и клиент, что делает возможным одноранговую связь.</span><span class="sxs-lookup"><span data-stu-id="05463-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="05463-109">Как здесь используется, термин сервер канала означает процесс, создающий именованный канал, а клиентский канал — процесс, который подключается к экземпляру именованного канала.</span><span class="sxs-lookup"><span data-stu-id="05463-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="05463-110">Серверная функция для создания экземпляра именованного канала — [**креатенамедпипе**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span><span class="sxs-lookup"><span data-stu-id="05463-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="05463-111">Серверная функция для приема соединения — [**коннектнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="05463-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="05463-112">Клиентский процесс подключается к именованному каналу с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) или [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="05463-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="05463-113">Именованные каналы можно использовать для обеспечения взаимодействия между процессами на одном компьютере или между процессами на разных компьютерах по сети.</span><span class="sxs-lookup"><span data-stu-id="05463-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="05463-114">Если служба сервера запущена, все именованные каналы доступны удаленно.</span><span class="sxs-lookup"><span data-stu-id="05463-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="05463-115">Если вы планируете использовать именованный канал только локально, запретите доступ к сети NT AUTHORITY \\ или переключитесь на локальный RPC.</span><span class="sxs-lookup"><span data-stu-id="05463-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="05463-116">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="05463-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="05463-117">Имена каналов</span><span class="sxs-lookup"><span data-stu-id="05463-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="05463-118">Режимы открытия именованных каналов</span><span class="sxs-lookup"><span data-stu-id="05463-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="05463-119">Типы именованных каналов, чтение и режимы ожидания</span><span class="sxs-lookup"><span data-stu-id="05463-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="05463-120">Экземпляры именованного канала</span><span class="sxs-lookup"><span data-stu-id="05463-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="05463-121">Операции именованного канала</span><span class="sxs-lookup"><span data-stu-id="05463-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="05463-122">Синхронные и перекрывающиеся входные и выходные данные</span><span class="sxs-lookup"><span data-stu-id="05463-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="05463-123">Безопасность именованного канала и права доступа</span><span class="sxs-lookup"><span data-stu-id="05463-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="05463-124">Олицетворение клиента именованного канала</span><span class="sxs-lookup"><span data-stu-id="05463-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="05463-125">Использование каналов</span><span class="sxs-lookup"><span data-stu-id="05463-125">Using Pipes</span></span>](using-pipes.md)

 

 
