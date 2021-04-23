---
title: Остановка серверного приложения
description: Серверное приложение может прекратить прослушивание клиентов, вызвав Рпкмгмтстопсерверлистенинг и Рпксерверунрегистериф или просто выходя из процесса узла.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Удаленный вызов процедур RPC, задачи, остановка серверного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779217"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="85085-104">Остановка серверного приложения</span><span class="sxs-lookup"><span data-stu-id="85085-104">Stopping the Server Application</span></span>

<span data-ttu-id="85085-105">Серверное приложение может прекратить прослушивание клиентов, вызвав [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) и [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)или просто выходя из процесса узла.</span><span class="sxs-lookup"><span data-stu-id="85085-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="85085-106">Оба метода приемлемы.</span><span class="sxs-lookup"><span data-stu-id="85085-106">Both methods are acceptable.</span></span> <span data-ttu-id="85085-107">Если сервер соответствует первому подходу, он должен реализовать следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="85085-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="85085-108">Функция сервера [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) не возвращает вызывающей программе, пока не произойдет исключение или пока не будет вызван вызов [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) .</span><span class="sxs-lookup"><span data-stu-id="85085-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="85085-109">По умолчанию для остановки сервера RPC с помощью **рпкмгмтстопсерверлистенинг** можно использовать только другой поток сервера.</span><span class="sxs-lookup"><span data-stu-id="85085-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="85085-110">Клиенты, пытающиеся приостановить работу сервера, получат сообщение об ошибке \_ \_ отказа в доступе RPC S \_ .</span><span class="sxs-lookup"><span data-stu-id="85085-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="85085-111">Однако можно настроить RPC, чтобы разрешить некоторым или всем клиентам прекращать работу сервера.</span><span class="sxs-lookup"><span data-stu-id="85085-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="85085-112">Дополнительные сведения см. в разделе **рпкмгмтстопсерверлистенинг** .</span><span class="sxs-lookup"><span data-stu-id="85085-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="85085-113">Кроме того, клиентское приложение может выполнить удаленный вызов процедур в подпрограммы завершения работы на сервере.</span><span class="sxs-lookup"><span data-stu-id="85085-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="85085-114">Подпрограммы завершения работы вызывают [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) и [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span><span class="sxs-lookup"><span data-stu-id="85085-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="85085-115">В этом примере программное приложение использует этот подход, добавляя новую удаленную функцию **Shutdown** в файл хеллоп. c.</span><span class="sxs-lookup"><span data-stu-id="85085-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="85085-116">В функции **Shutdown** один параметр NULL для [**рпкмгмтстопсерверлистенинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) указывает, что локальное приложение должно прекращать прослушивание удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="85085-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="85085-117">Два параметра NULL для [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) — это подстановочные знаки, указывающие, что все интерфейсы должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="85085-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="85085-118">Параметр **false** указывает, что интерфейс должен быть немедленно удален из реестра, а не ожидать завершения отложенных вызовов.</span><span class="sxs-lookup"><span data-stu-id="85085-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




