---
title: Использование дескрипторов привязки и выполнение вызовов RPC
description: Распространенной ошибкой между программистами RPC является обработка всех исключений.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792787"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="8cd69-103">Использование дескрипторов привязки и выполнение вызовов RPC</span><span class="sxs-lookup"><span data-stu-id="8cd69-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="8cd69-104">Распространенной ошибкой между программистами RPC является обработка всех исключений.</span><span class="sxs-lookup"><span data-stu-id="8cd69-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="8cd69-105">Многие программисты структурируют свои обработчики исключений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8cd69-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="8cd69-106">Проблема с этим обработчиком заключается в том, что он перехватывает все ошибки, включая ошибки в клиентской программе.</span><span class="sxs-lookup"><span data-stu-id="8cd69-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="8cd69-107">Перехват ошибок в клиентской программе делает отладку более сложной.</span><span class="sxs-lookup"><span data-stu-id="8cd69-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="8cd69-108">Ниже приведен правильный способ структурирования обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="8cd69-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="8cd69-109">Этот обработчик исключений имеет преимущество разрешив определенный диапазон ошибок с помощью.</span><span class="sxs-lookup"><span data-stu-id="8cd69-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="8cd69-110">Эти ошибки никогда не будут возвращаться сервером, так как они указывают на проблему на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="8cd69-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="8cd69-111">Кроме того, рекомендуется использовать **\[** [строгое \_ использование \_ маркера контекста](/windows/desktop/Midl/strict-context-handle) **\]** и **\[** атрибутов [ \_ строгого \_ контекста \_](/windows/desktop/Midl/type-strict-context-handle), **\]** чтобы гарантировать, что во время выполнения RPC создается описатель контекста на одном интерфейсе, который может быть передан в качестве аргумента только методам этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8cd69-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="8cd69-112">Это предотвратит сбои сервера, происходящие при открытии и передаче дескрипторов контекста между различными интерфейсами, которые существуют в рамках одного процесса.</span><span class="sxs-lookup"><span data-stu-id="8cd69-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cd69-113">См. также</span><span class="sxs-lookup"><span data-stu-id="8cd69-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd69-114">Нечеткий \_ Контекстный \_ маркер</span><span class="sxs-lookup"><span data-stu-id="8cd69-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="8cd69-115">Тип \_ строгого \_ \_ маркера контекста</span><span class="sxs-lookup"><span data-stu-id="8cd69-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 