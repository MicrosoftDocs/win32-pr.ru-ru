---
title: Порядок причин асинхронных вызовов
description: В асинхронном приложении RPC клиентский поток может выполнить второй асинхронный вызов в обработчике привязки до завершения предыдущего вызова, сделанного для этого обработчика.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067895"
---
# <a name="causal-ordering-of-asynchronous-calls"></a><span data-ttu-id="06b73-103">Порядок причин асинхронных вызовов</span><span class="sxs-lookup"><span data-stu-id="06b73-103">Causal Ordering of Asynchronous Calls</span></span>

<span data-ttu-id="06b73-104">В асинхронном приложении RPC клиентский поток может выполнить второй асинхронный вызов в обработчике привязки до завершения предыдущего вызова, сделанного для этого обработчика.</span><span class="sxs-lookup"><span data-stu-id="06b73-104">In an asynchronous RPC application, it is possible for a client thread to make a second asynchronous call on a binding handle before an earlier call made on that handle has completed.</span></span> <span data-ttu-id="06b73-105">Библиотека времени выполнения RPC обрабатывает эту ситуацию следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06b73-105">The RPC run-time library handles this situation as follows:</span></span>

-   <span data-ttu-id="06b73-106">Механизм асинхронного вызова процедур RPC гарантирует, что асинхронные вызовы на одном и том же дескрипторе привязки на одном и том же уровне безопасности отправляются в том порядке, в котором они были сделаны.</span><span class="sxs-lookup"><span data-stu-id="06b73-106">The asynchronous RPC mechanism guarantees that asynchronous calls made on the same binding handle, on the same thread, at the same security level, are dispatched in the order they were made.</span></span> <span data-ttu-id="06b73-107">Фактическое выполнение вызовов может происходить неупорядоченно.</span><span class="sxs-lookup"><span data-stu-id="06b73-107">Actual execution of the calls may occur out of order.</span></span>
-   <span data-ttu-id="06b73-108">Как и в случае синхронных вызовов, асинхронные вызовы удаленных процедур из разных клиентских потоков выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="06b73-108">As with synchronous calls, asynchronous remote procedure calls from different client threads execute simultaneously.</span></span>
-   <span data-ttu-id="06b73-109">Если за асинхронный вызов из клиентского приложения последуют один или несколько синхронных вызовов, асинхронный вызов может выполняться во время выполнения синхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="06b73-109">If an asynchronous call from a client application is followed by one or more synchronous calls, the asynchronous call can execute while the synchronous calls are executing.</span></span> <span data-ttu-id="06b73-110">Независимо от состояния асинхронного вызова синхронные вызовы выполняются в том порядке, в котором они получены сервером.</span><span class="sxs-lookup"><span data-stu-id="06b73-110">Regardless of the status of the asynchronous call, the synchronous calls are executed in the order in which they are received by the server.</span></span>
-   <span data-ttu-id="06b73-111">Если клиентское приложение выбирает порядок неважности для определенного маркера привязки, он отключает сериализацию для этого обработчика.</span><span class="sxs-lookup"><span data-stu-id="06b73-111">If a client application selects noncausal ordering for a particular binding handle, it disables serialization for that handle.</span></span> <span data-ttu-id="06b73-112">Приложения позволяют упорядочивать неважности, вызывая [**рпкбиндингсетоптион**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) с параметром *Option* , установленным в RPC \_ с \_ \_ привязкой opt \_ , а параметру *OptionValue* задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="06b73-112">Applications enable noncausal ordering by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) with the *Option* parameter set to RPC\_C\_OPT\_BINDING\_NONCAUSAL and the *OptionValue* parameter set to **TRUE**.</span></span> <span data-ttu-id="06b73-113">Дополнительные сведения см. в разделе [константы параметров привязки](binding-option-constants.md).</span><span class="sxs-lookup"><span data-stu-id="06b73-113">For details, see [Binding Option Constants](binding-option-constants.md).</span></span>

 

 




