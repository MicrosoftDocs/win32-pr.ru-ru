---
title: Клиентское приложение
description: Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488181"
---
# <a name="the-client-application"></a><span data-ttu-id="3b4f5-103">Клиентское приложение</span><span class="sxs-lookup"><span data-stu-id="3b4f5-103">The Client Application</span></span>

<span data-ttu-id="3b4f5-104">Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK).</span><span class="sxs-lookup"><span data-stu-id="3b4f5-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="3b4f5-105">Исходный файл Хеллок. c содержит директиву, которая включает созданный MIDL-файл заголовка Hello. h.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-105">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="3b4f5-106">В Hello. h — это директивы для включения RPC. h и рпкндр. h, которые содержат определения для подпрограмм среды выполнения RPC, **хеллопрок** и **завершения работы**, а также типы данных, используемые клиентскими и серверными приложениями.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-106">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="3b4f5-107">Компилятор MIDL должен использоваться с примером ниже.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="3b4f5-108">Так как клиент управляет подключением к серверу, клиентское приложение вызывает функции времени выполнения, чтобы установить обработчик для сервера и освободить этот обработчик после завершения удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-108">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="3b4f5-109">Функция [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) объединяет компоненты маркера привязки в строковое представление этого обработчика и выделяет память для привязки строки.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-109">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="3b4f5-110">Функция [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) создает в клиентском приложении маркер привязки сервера, **Hello \_ клиентифхандле**, из этого строкового представления.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-110">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="3b4f5-111">В вызове [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)параметры не указывают UUID, поскольку в этом учебнике предполагается, что имеется только одна реализация интерфейса "Hello".</span><span class="sxs-lookup"><span data-stu-id="3b4f5-111">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="3b4f5-112">Кроме того, при вызове не указывается сетевой адрес, так как приложение будет использовать значение по умолчанию — локальный хост-компьютер.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-112">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="3b4f5-113">Последовательность протокола — это символьная строка, представляющая базовый сетевой транспорт.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-113">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="3b4f5-114">Конечная точка — это имя, которое зависит от последовательности протокола.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-114">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="3b4f5-115">В этом примере для сетевого транспорта используются именованные каналы, поэтому используется последовательность протокола "нкакн \_ NP".</span><span class="sxs-lookup"><span data-stu-id="3b4f5-115">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="3b4f5-116">Имя конечной точки — " \\ pipe \\ Hello".</span><span class="sxs-lookup"><span data-stu-id="3b4f5-116">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="3b4f5-117">Фактические вызовы удаленных процедур, **хеллопрок** и **Shutdown**, выполняются в обработчике исключений RPC — наборе макросов, которые позволяют управлять исключениями, происходящими вне кода приложения.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-117">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="3b4f5-118">Если модуль времени выполнения RPC сообщает об исключении, управление передается блоку [**рпцексцепт**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="3b4f5-118">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="3b4f5-119">Именно здесь можно вставить код, чтобы выполнить необходимую очистку, а затем завершить работу корректно.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-119">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="3b4f5-120">Этот пример программы просто информирует пользователя о том, что произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-120">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="3b4f5-121">Если вы не хотите использовать исключения, можно использовать атрибуты ACF [ \_ состояние](/windows/desktop/Midl/comm-status) связи и [ \_ состояние сбоя](/windows/desktop/Midl/fault-status) для сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-121">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="3b4f5-122">После завершения удаленных вызовов процедур клиент сначала вызывает [**рпкстрингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) , чтобы освободить память, выделенную для привязки строки.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-122">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="3b4f5-123">Обратите внимание, что после создания маркера привязки клиентская программа может освободить строковую привязку в любое время.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-123">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="3b4f5-124">Клиент затем вызывает [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) для освобождения маркера.</span><span class="sxs-lookup"><span data-stu-id="3b4f5-124">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
}

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 