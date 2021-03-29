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
# <a name="using-binding-handles-and-making-rpc-calls"></a>Использование дескрипторов привязки и выполнение вызовов RPC

Распространенной ошибкой между программистами RPC является обработка всех исключений. Многие программисты структурируют свои обработчики исключений следующим образом:

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

Проблема с этим обработчиком заключается в том, что он перехватывает все ошибки, включая ошибки в клиентской программе. Перехват ошибок в клиентской программе делает отладку более сложной. Ниже приведен правильный способ структурирования обработчика исключений.

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

Этот обработчик исключений имеет преимущество разрешив определенный диапазон ошибок с помощью. Эти ошибки никогда не будут возвращаться сервером, так как они указывают на проблему на стороне клиента.

Кроме того, рекомендуется использовать **\[** [строгое \_ использование \_ маркера контекста](/windows/desktop/Midl/strict-context-handle) **\]** и **\[** атрибутов [ \_ строгого \_ контекста \_](/windows/desktop/Midl/type-strict-context-handle), **\]** чтобы гарантировать, что во время выполнения RPC создается описатель контекста на одном интерфейсе, который может быть передан в качестве аргумента только методам этого интерфейса. Это предотвратит сбои сервера, происходящие при открытии и передаче дескрипторов контекста между различными интерфейсами, которые существуют в рамках одного процесса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Нечеткий \_ Контекстный \_ маркер](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[Тип \_ строгого \_ \_ маркера контекста](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 