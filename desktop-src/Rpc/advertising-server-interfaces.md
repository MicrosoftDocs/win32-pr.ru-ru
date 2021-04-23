---
title: Реклама в интерфейсах сервера
description: Серверная часть приложения, использующего автоматические дескрипторы, должна вызывать функцию Рпкнсбиндинжекспорт, чтобы сделать сведения о привязке сервера доступными для клиентов.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068021"
---
# <a name="advertising-server-interfaces"></a><span data-ttu-id="1b09c-103">Реклама в интерфейсах сервера</span><span class="sxs-lookup"><span data-stu-id="1b09c-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="1b09c-104">Серверная часть приложения, использующего автоматические дескрипторы, должна вызывать функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) , чтобы сделать сведения о привязке сервера доступными для клиентов.</span><span class="sxs-lookup"><span data-stu-id="1b09c-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="1b09c-105">Для автоматической обработки дескрипторов привязки на сервере, доступном для клиента, должна выполняться служба имен.</span><span class="sxs-lookup"><span data-stu-id="1b09c-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="1b09c-106">Реализация службы имен (Майкрософт), локатор Майкрософт, управление автоматическими дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="1b09c-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="1b09c-107">Серверные приложения, использующие неявные и явные дескрипторы привязки, также могут объявлять свое присутствие в базе данных службы имен.</span><span class="sxs-lookup"><span data-stu-id="1b09c-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="1b09c-108">Как правило, сервер вызывает следующие функции времени выполнения:</span><span class="sxs-lookup"><span data-stu-id="1b09c-108">Typically, the server calls the following run-time functions:</span></span>

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

<span data-ttu-id="1b09c-109">Вызовы первых двух функций в этом фрагменте кода похожи на [пример Hello, World](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="1b09c-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="1b09c-110">Эти функции позволяют клиенту получить сведения о привязке.</span><span class="sxs-lookup"><span data-stu-id="1b09c-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="1b09c-111">Вызовы [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) и [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) помещают сведения в базу данных службы имен.</span><span class="sxs-lookup"><span data-stu-id="1b09c-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="1b09c-112">Вызов [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) заполняет вектор привязки допустимыми дескрипторами привязки перед экспортом дескрипторов в службу имен.</span><span class="sxs-lookup"><span data-stu-id="1b09c-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="1b09c-113">После того как программа сервера экспортирует дескрипторы в базу данных, клиент (или клиентские заглушки) может вызвать [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) и [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="1b09c-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="1b09c-114">Дополнительные сведения см. в разделе [Поиск хостовых систем сервера](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="1b09c-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="1b09c-115">Вызовы [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) и [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) и связанных с ними структур данных выглядят следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b09c-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

<span data-ttu-id="1b09c-116">Обратите внимание, что параметр [**Рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *пбиндингвектор* является указателем на указатель [**на \_ \_ вектор привязки RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span><span class="sxs-lookup"><span data-stu-id="1b09c-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="1b09c-117">Также помните, что после каждого вызова [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) должен следовать вызов [**рпкбиндингвекторфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span><span class="sxs-lookup"><span data-stu-id="1b09c-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="1b09c-118">Чтобы удалить экспортированный интерфейс из базы данных службы имен, сервер вызывает [**рпкнсбиндингунекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="1b09c-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="1b09c-119">Функция [**рпкнсбиндингунекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) должна использоваться только при окончательном удалении службы.</span><span class="sxs-lookup"><span data-stu-id="1b09c-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="1b09c-120">Его не следует использовать при временном отключении службы, например при выключении сервера для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1b09c-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="1b09c-121">Серверная программа может зарегистрироваться в базе данных службы имен, но она будет недоступна, так как сервер временно отключен от сети.</span><span class="sxs-lookup"><span data-stu-id="1b09c-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="1b09c-122">Клиентское приложение должно содержать код обработки исключений для такого условия.</span><span class="sxs-lookup"><span data-stu-id="1b09c-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="1b09c-123">Дополнительные сведения о содержимом и формате базы данных службы имен см. в разделе [база данных службы имен RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="1b09c-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="1b09c-124">Приложения могут использовать службу Active Directory, если клиентские и серверные программы работают под управлением Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1b09c-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="1b09c-125">Компьютеры, на которых работают клиентские и серверные программы, должны быть членами домена Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1b09c-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="1b09c-126">Чтобы объявить свое присутствие с помощью службы Active Directory, необходимо запустить серверную программу в контексте безопасности администратора домена.</span><span class="sxs-lookup"><span data-stu-id="1b09c-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="1b09c-127">Если он выполняется в контексте пользователей домена, администратор домена должен изменить список управления доступом (ACL) в контейнере служб RPC.</span><span class="sxs-lookup"><span data-stu-id="1b09c-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="1b09c-128">Дополнительные сведения см. в документации по Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b09c-128">For more information, see the Active Directory documentation.</span></span>

 

 




