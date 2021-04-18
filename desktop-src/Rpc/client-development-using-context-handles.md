---
title: Разработка клиентов с помощью дескрипторов контекста
description: Только клиентская программа имеет доступ к контекстному обработчику — он передает его на сервер каждый раз, когда клиент выполняет удаленный вызов процедуры.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532366"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="0d4b4-103">Разработка клиентов с помощью дескрипторов контекста</span><span class="sxs-lookup"><span data-stu-id="0d4b4-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="0d4b4-104">Только клиентская программа имеет доступ к контекстному обработчику — он передает его на сервер каждый раз, когда клиент выполняет удаленный вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="0d4b4-105">Клиентскому приложению не требуется доступ к содержимому маркера.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="0d4b4-106">Он не должен пытаться изменить данные обработчика контекста каким бы то ни было образом.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="0d4b4-107">Удаленные процедуры, которые клиент вызывает, выполняют все необходимые операции в контексте сервера.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="0d4b4-108">Перед запросом маркера контекста с сервера клиенты должны установить привязку к серверу.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="0d4b4-109">Клиент может использовать автоматический, неявный или явный маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="0d4b4-110">С помощью допустимого маркера привязки клиент может вызвать удаленную процедуру на сервере, которая либо возвращает открытый (не **равный null**) обработчик контекста, либо передает один через параметр **\[ out \]** в списке параметров удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="0d4b4-111">Клиенты могут использовать открытые дескрипторы контекста любым необходимым образом.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="0d4b4-112">Однако они должны сделать недействительным обработчик, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="0d4b4-113">Это можно сделать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="0d4b4-113">There are two way to do this:</span></span>

-   <span data-ttu-id="0d4b4-114">Для вызова удаленной процедуры, предлагаемой серверной программой, которая освобождает контекст и закрывает контекстный маркер (присваивает ему **значение NULL**).</span><span class="sxs-lookup"><span data-stu-id="0d4b4-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="0d4b4-115">Если сервер недоступен, вызовите функцию [**рпкссдестройклиентконтекст**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="0d4b4-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="0d4b4-116">Второй подход очищает состояние на стороне клиента и не очищает состояние на стороне сервера, поэтому его следует использовать только в том случае, если обнаружена сетевая секция, и клиент и сервер будут выполнять независимую очистку.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="0d4b4-117">Сервер выполняет независимую очистку с помощью подпрограммы запуска, клиент делает это с помощью функции [**рпкссдестройклиентконтекст**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="0d4b4-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="0d4b4-118">В следующем фрагменте кода представлен пример того, как клиент может использовать контекстный маркер.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="0d4b4-119">Сведения об определении интерфейса, используемого в этом примере, см. в разделе [Разработка интерфейса с использованием дескрипторов контекста](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0d4b4-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="0d4b4-120">Сведения о реализации сервера см. в разделе [Разработка серверов с помощью дескрипторов контекста](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0d4b4-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="0d4b4-121">В этом примере клиент вызывает Ремотеопен для получения маркера контекста, содержащего допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="0d4b4-122">Затем клиент может использовать маркер контекста в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="0d4b4-123">Так как больше не требуется маркер привязки, клиент может освободить явный обработчик, который использовался для создания маркера контекста:</span><span class="sxs-lookup"><span data-stu-id="0d4b4-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="0d4b4-124">Клиентское приложение в этом примере использует процедуру с именем Ремотереад для чтения файла данных на сервере до тех пор, пока не встретится конец файла.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="0d4b4-125">Затем он закрывает файл, вызывая Ремотеклосе.</span><span class="sxs-lookup"><span data-stu-id="0d4b4-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="0d4b4-126">Контекстный маркер отображается как параметр в функциях Ремотереад и Ремотеклосе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0d4b4-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




