---
title: Обеспечение доступности сервера в сети
description: Прежде чем серверное приложение сможет принимать удаленные вызовы процедур, оно должно быть доступно в сети.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Удаленный вызов процедур RPC, задачи, обеспечение доступности сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068182"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="aaf3c-104">Обеспечение доступности сервера в сети</span><span class="sxs-lookup"><span data-stu-id="aaf3c-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="aaf3c-105">Прежде чем серверное приложение сможет принимать удаленные вызовы процедур, оно должно быть доступно в сети.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="aaf3c-106">Для этого сервер сообщает времени выполнения RPC о том, что он желает принимать вызовы в одной или нескольких последовательностях протоколов.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="aaf3c-107">Выбор последовательностей протоколов, поддерживаемых серверным приложением, является важным решением. различные последовательности протоколов имеют очень разные возможности.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="aaf3c-108">Серверы, которые предполагают получение вызовов локально, должны использовать **нкалрпк**.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="aaf3c-109">Серверы, принимающие удаленные вызовы, должны использовать **нкакн \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="aaf3c-110">Серверы не должны проверять, что последовательность протокола, в которой они получают вызовы, — это последовательность протокола, в которой они хотят получить вызовы.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="aaf3c-111">Дополнительные сведения см. в статье будьте осторожны с другими конечными точками RPC, работающими в том же процессе.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="aaf3c-112">В следующем примере используется **нкакн \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="aaf3c-113">Большинство серверных программ используют все последовательности протоколов, доступные в сети.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="aaf3c-114">Для этого они вызывают функцию [**рпксерверусепротсек**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="aaf3c-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="aaf3c-115">Первым параметром функции [**рпксерверусепротсек**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) является последовательность протокола.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="aaf3c-116">Второй параметр зависит от последовательности протокола.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="aaf3c-117">Как показано в фрагменте кода, большинство серверных программ применяют этот параметр к **RPC \_ C \_ протсек \_ Max \_ запросов секунду \_ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="aaf3c-118">Это значение задает использование значения по умолчанию для библиотеки RPC.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="aaf3c-119">Третий параметр является дескриптором безопасности и не должен использоваться в приложениях.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="aaf3c-120">Дополнительные сведения см. в разделе [**Безопасность**](security.md).</span><span class="sxs-lookup"><span data-stu-id="aaf3c-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="aaf3c-121">Можно также использовать функции [**рпксерверусеаллпротсекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**рпксерверусепротсекекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**рпксерверусепротсекеп**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)или [**рпксерверусепротсекепекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .</span><span class="sxs-lookup"><span data-stu-id="aaf3c-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="aaf3c-122">Когда серверное приложение выбирает по крайней мере одну последовательность протоколов, серверы, использующие динамические конечные точки, должны создавать сведения о привязке для каждой используемой им последовательности протокола.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="aaf3c-123">Сервер хранит сведения о привязке в векторе привязки, который затем можно экспортировать в службу сопоставителя конечных точек.</span><span class="sxs-lookup"><span data-stu-id="aaf3c-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="aaf3c-124">Используйте функцию [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) для получения вектора привязки для серверного приложения, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="aaf3c-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="aaf3c-125">Единственный параметр, передаваемый функции [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) , — это указатель на указатель на структуру [**\_ \_ вектора привязки RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) .</span><span class="sxs-lookup"><span data-stu-id="aaf3c-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="aaf3c-126">Библиотека времени выполнения RPC динамически выделяет массив векторов привязки и сохраняет адрес массива в переменной параметра (в данном случае это **рпкбиндингвектор**).</span><span class="sxs-lookup"><span data-stu-id="aaf3c-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="aaf3c-127">Каждое серверное приложение отвечает за освобождение этого вектора привязки с помощью функции [**рпкбиндингвекторфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) по завершении ее использования (например, после того, как она была передана соответствующим функциям).</span><span class="sxs-lookup"><span data-stu-id="aaf3c-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




