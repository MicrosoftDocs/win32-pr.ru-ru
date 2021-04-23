---
title: Пакет управления памятью RPCSS
description: Пара распределитель/распределитель по умолчанию, используемая заглушками и временем выполнения при выделении памяти от имени приложения, — это пользовательское \_ \_ выделение или MIDL пользователя MIDL \_ \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488112"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="34bcb-103">Пакет управления памятью RPCSS</span><span class="sxs-lookup"><span data-stu-id="34bcb-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="34bcb-104">Пара распределитель/распределитель по умолчанию, используемая заглушками и временем выполнения при выделении памяти от имени приложения, — это пользовательское **\_ \_ выделение** / **MIDL \_ \_** пользователем.</span><span class="sxs-lookup"><span data-stu-id="34bcb-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="34bcb-105">Однако можно выбрать пакет RPCSS вместо значения по умолчанию с помощью атрибута ACF **\[ Enable \_ \]**.</span><span class="sxs-lookup"><span data-stu-id="34bcb-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="34bcb-106">Пакет RPCSS состоит из функций RPC, начинающихся с префикса **RPCSS** или **рпксм**.</span><span class="sxs-lookup"><span data-stu-id="34bcb-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="34bcb-107">Пакет RPCSS не рекомендуется для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="34bcb-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="34bcb-108">Пакет управления памятью RPCSS устарел.</span><span class="sxs-lookup"><span data-stu-id="34bcb-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="34bcb-109">Мы советуем использовать в своем расположении пользовательские пользовательские [**\_ \_ выделять**](/windows/desktop/Midl/midl-user-allocate-1) и [**\_ \_ MIDL**](/windows/desktop/Midl/midl-user-free-1) .</span><span class="sxs-lookup"><span data-stu-id="34bcb-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="34bcb-110">В режиме **/ОСФ** пакет RPCSS включает автоматически созданные MIDL-заглушки при использовании полных указателей, когда аргументы нуждаются в выделении памяти или в результате использования атрибута **\[ включения \_ выделения \]** .</span><span class="sxs-lookup"><span data-stu-id="34bcb-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="34bcb-111">В режиме по умолчанию (Microsoft Extended) пакет RPCSS включен, только если используется атрибут **\[ включения \_ выделения \]** .</span><span class="sxs-lookup"><span data-stu-id="34bcb-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="34bcb-112">Атрибут **\[ включить \_ выделение \] позволяет использовать** в качестве заглушки среду RPCSS на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="34bcb-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="34bcb-113">На стороне клиента будет отображаться сообщение о возможности включения пакета RPCSS.</span><span class="sxs-lookup"><span data-stu-id="34bcb-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="34bcb-114">В режиме **/ОСФ** на стороне клиента это не влияет.</span><span class="sxs-lookup"><span data-stu-id="34bcb-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="34bcb-115">Если пакет RPCSS включен, выделение памяти на стороне сервера осуществляется с помощью механизма выделения памяти частных вызовов RPC и дераспределителя.</span><span class="sxs-lookup"><span data-stu-id="34bcb-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="34bcb-116">Можно выделить память, используя тот же механизм, вызвав [**рпксмаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (или [**рпкссаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span><span class="sxs-lookup"><span data-stu-id="34bcb-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="34bcb-117">После возврата из заглушки сервера вся память, выделенная пакетом RPCSS, автоматически освобождается.</span><span class="sxs-lookup"><span data-stu-id="34bcb-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="34bcb-118">В следующем примере показано, как включить пакет RPCSS:</span><span class="sxs-lookup"><span data-stu-id="34bcb-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="34bcb-119">Приложение может явно освободить память, вызвав функцию [**рпкссфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) или [**рпксмфри**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) .</span><span class="sxs-lookup"><span data-stu-id="34bcb-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="34bcb-120">Обратите внимание, что эти функции фактически не освобождают память.</span><span class="sxs-lookup"><span data-stu-id="34bcb-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="34bcb-121">Они помечаются для удаления.</span><span class="sxs-lookup"><span data-stu-id="34bcb-121">They mark it for deletion.</span></span> <span data-ttu-id="34bcb-122">Библиотека RPC освобождает память, когда программа вызывает [**рпкссдисаблеаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) или [**рпкссдисаблеаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span><span class="sxs-lookup"><span data-stu-id="34bcb-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="34bcb-123">Можно также включить среду управления памятью для приложения, вызвав подпрограммы [**рпксменаблеаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (и вы можете отключить ее, вызвав подпрограммы [**рпксмдисаблеаллокате**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ).</span><span class="sxs-lookup"><span data-stu-id="34bcb-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="34bcb-124">После включения код приложения может распределять и освобождать память путем вызова функций из пакета RPCSS.</span><span class="sxs-lookup"><span data-stu-id="34bcb-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 