---
title: Серверное приложение
description: Просмотрите серверное приложение часть примера удаленного вызова процедур (RPC). Этот пример относится к приложению "Hello World" в пакете Platform SDK.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406067"
---
# <a name="the-server-application"></a><span data-ttu-id="26f40-104">Серверное приложение</span><span class="sxs-lookup"><span data-stu-id="26f40-104">The Server Application</span></span>

<span data-ttu-id="26f40-105">Приведенный ниже пример относится к приложению "Hello World" в каталоге RPC \\ Hello пакета средств разработки программного обеспечения платформы (SDK).</span><span class="sxs-lookup"><span data-stu-id="26f40-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="26f40-106">Серверная часть распределенного приложения информирует систему о доступности служб.</span><span class="sxs-lookup"><span data-stu-id="26f40-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="26f40-107">Затем он ожидает клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="26f40-107">It then waits for client requests.</span></span> <span data-ttu-id="26f40-108">Компилятор MIDL должен использоваться с примером ниже.</span><span class="sxs-lookup"><span data-stu-id="26f40-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="26f40-109">В зависимости от размера приложения и настроек кода можно реализовать удаленные процедуры в одном или нескольких отдельных файлах.</span><span class="sxs-lookup"><span data-stu-id="26f40-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="26f40-110">В этой программе учебника исходный файл Hello. c содержит основную подпрограмму сервера.</span><span class="sxs-lookup"><span data-stu-id="26f40-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="26f40-111">Файл Хеллоп. c содержит удаленную процедуру.</span><span class="sxs-lookup"><span data-stu-id="26f40-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="26f40-112">Преимущество организации удаленных процедур в отдельных файлах заключается в том, что процедуры можно связать с автономной программой для отладки кода перед его преобразованием в распределенное приложение.</span><span class="sxs-lookup"><span data-stu-id="26f40-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="26f40-113">После того как процедуры будут работать в автономной программе, можно скомпилировать и связать исходные файлы, содержащие удаленные процедуры, с серверным приложением.</span><span class="sxs-lookup"><span data-stu-id="26f40-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="26f40-114">Как и в случае с исходным файлом клиентского приложения, исходный файл серверного приложения должен включать файл заголовка Hello. h.</span><span class="sxs-lookup"><span data-stu-id="26f40-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="26f40-115">Сервер вызывает функции времени выполнения RPC [**рпксерверусепротсекеп**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) и [**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , чтобы сделать сведения о привязке доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="26f40-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="26f40-116">Этот пример программы передает имя обработчика интерфейса в **рпксерверрегистериф**.</span><span class="sxs-lookup"><span data-stu-id="26f40-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="26f40-117">Другие параметры имеют значение **null**.</span><span class="sxs-lookup"><span data-stu-id="26f40-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="26f40-118">Затем сервер вызывает функцию [**рпксерверлистен**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) , чтобы указать, что она ожидает клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="26f40-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="26f40-119">Серверное приложение также должно включать две функции управления памятью, которые вызываются заглушкой сервера: MIDL, пользовательское [**\_ \_ выделение**](the-midl-user-allocate-function.md) и [**MIDL \_ \_**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="26f40-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="26f40-120">Эти функции выделяют и освобождают память на сервере, когда удаленная процедура передает параметры на сервер.</span><span class="sxs-lookup"><span data-stu-id="26f40-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="26f40-121">В этом примере программы MIDL для пользовательского **\_ \_ выделения** и **MIDL \_ является \_** просто оболочками для функций C-Library [**malloc**](pointers-and-memory-allocation.md) и **Free**.</span><span class="sxs-lookup"><span data-stu-id="26f40-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="26f40-122">(Обратите внимание, что в объявлениях, созданных компилятором MIDL, "MIDL" является прописной буквой.</span><span class="sxs-lookup"><span data-stu-id="26f40-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="26f40-123">В файле заголовка Рпкндр. h определено пользовательское \_ \_ бесплатное значение MIDL, а \_ пользователь MIDL \_ выделит пользователя MIDL \_ \_ свободным и MIDL \_ \_ , соответственно.)</span><span class="sxs-lookup"><span data-stu-id="26f40-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
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



 

 




