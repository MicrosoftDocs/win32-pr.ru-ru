---
title: Функция midl_user_allocate
description: '\_ \_ Функция пользовательского выделения MIDL — это процедура, которая должна быть предоставлена разработчиками приложений RPC.'
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134239"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="1fed8-103">\_ \_ Функция пользовательского выделения MIDL</span><span class="sxs-lookup"><span data-stu-id="1fed8-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="1fed8-104">Функция **\_ пользовательского \_ выделения MIDL** — это процедура, которая должна быть предоставлена разработчиками приложений RPC.</span><span class="sxs-lookup"><span data-stu-id="1fed8-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="1fed8-105">Она выделяет память для заглушек RPC и подпрограмм библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1fed8-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="1fed8-106">Функция **\_ \_ выделения пользователем MIDL** должна соответствовать следующему прототипу:</span><span class="sxs-lookup"><span data-stu-id="1fed8-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="1fed8-107">Параметр *кбитес* указывает число байтов для выделения.</span><span class="sxs-lookup"><span data-stu-id="1fed8-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="1fed8-108">Как клиентские приложения, так и серверные приложения должны реализовать функцию **\_ пользовательского \_ выделения MIDL** , если не выполняется компиляция в режиме использование-Compatibility (/ОСФ).</span><span class="sxs-lookup"><span data-stu-id="1fed8-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="1fed8-109">Приложения и созданные заглушки вызывают **пользователь MIDL, который \_ \_ выделяется** напрямую или косвенно для управления выделенными объектами.</span><span class="sxs-lookup"><span data-stu-id="1fed8-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="1fed8-110">Пример:</span><span class="sxs-lookup"><span data-stu-id="1fed8-110">For example:</span></span>

-   <span data-ttu-id="1fed8-111">Клиентские и серверные приложения вызывают вызов **\_ пользователю MIDL \_** для выделения памяти для приложения, например при создании нового узла в дереве или связанном списке.</span><span class="sxs-lookup"><span data-stu-id="1fed8-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="1fed8-112">Заглушка сервера вызывает метод **MIDL, \_ \_ выделяющий пользователя** при демаршалировании данных в адресное пространство сервера.</span><span class="sxs-lookup"><span data-stu-id="1fed8-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="1fed8-113">Клиентская заглушка вызывает метод **MIDL, \_ \_ выделяющий пользователя** при демаршалировании данных с сервера, на который ссылается \[ \] указатель out.</span><span class="sxs-lookup"><span data-stu-id="1fed8-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="1fed8-114">Обратите внимание, что для \[ в \] , \[ \] и \[ уникальных \] указателей клиентская заглушка вызывает метод **MIDL \_ User, \_ выделяющий** , только если \[ значение уникального \] указателя было равно null во входных данных и при вызове изменяется значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="1fed8-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="1fed8-115">Если \[ \] во входных данных для уникального указателя задано значение, отличное от NULL, клиентская заглушка записывает связанные данные в существующую память.</span><span class="sxs-lookup"><span data-stu-id="1fed8-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="1fed8-116">Если **\_ пользователю MIDL \_** не удается выделить память, он должен вернуть пустой указатель.</span><span class="sxs-lookup"><span data-stu-id="1fed8-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="1fed8-117">Функция пользовательского выделения MIDL должна возвращать 8-байтный **\_ \_ выделенный** указатель.</span><span class="sxs-lookup"><span data-stu-id="1fed8-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="1fed8-118">Например, примеры программ, предоставляемые пакетом средств разработки программного обеспечения платформы (SDK), реализуют **\_ Пользовательский интерфейс \_ MIDL** с точки зрения функции C [**malloc**](pointers-and-memory-allocation.md):</span><span class="sxs-lookup"><span data-stu-id="1fed8-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="1fed8-119">Если пакет RPCSS включен (например, в результате использования \[ атрибута [**включить \_ выделение**](/windows/desktop/Midl/enable-allocate) \] ), используйте [**рпксмаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) для выделения памяти на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="1fed8-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="1fed8-120">Дополнительные сведения о \[ **включении \_ выделения** см \] . в [справочнике по MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="1fed8-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 