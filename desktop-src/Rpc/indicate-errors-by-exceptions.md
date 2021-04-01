---
title: Указание ошибок в исключениях
description: Для традиционных программистов C ошибки обычно возвращаются через возвращаемые значения или специальным параметром \ out \, который возвращает код ошибки.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890884"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="51ac9-103">Указание ошибок в исключениях</span><span class="sxs-lookup"><span data-stu-id="51ac9-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="51ac9-104">Для традиционных программистов C ошибки обычно возвращаются с помощью возвращаемых значений или специального \[ параметра out \] , который возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="51ac9-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="51ac9-105">Это приводит к интерфейсам, реализованным следующим образом:</span><span class="sxs-lookup"><span data-stu-id="51ac9-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="51ac9-106">Проблема с этим подходом заключается в том, что возвращаемые значения RPC являются просто целыми числами.</span><span class="sxs-lookup"><span data-stu-id="51ac9-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="51ac9-107">Они не имеют специального смысла как ошибки (Обратите внимание, что [**\_ состояние ошибки \_ t**](/windows/desktop/Midl/error-status-t) не имеет специальной семантики на стороне сервера), что несет важные последствия.</span><span class="sxs-lookup"><span data-stu-id="51ac9-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="51ac9-108">Во-первых, RPC не предупреждает о сбое операции; Он пытается распаковать все \[ входные \] и выходные \[ \] аргументы.</span><span class="sxs-lookup"><span data-stu-id="51ac9-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="51ac9-109">Семантика сбоев дескрипторов контекста также отличается.</span><span class="sxs-lookup"><span data-stu-id="51ac9-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="51ac9-110">Пакет, возвращаемый клиенту, фактически является пакетом успешного выполнения с кодом ошибки, который скрыт глубоко в пакете.</span><span class="sxs-lookup"><span data-stu-id="51ac9-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="51ac9-111">Это также означает, что RPC не использует расширенные сведения об ошибке, поэтому клиентское программное обеспечение часто не может распоразличить место вызова.</span><span class="sxs-lookup"><span data-stu-id="51ac9-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="51ac9-112">Указание ошибок в подпрограммах сервера RPC путем вызова исключений структурированной обработки исключений (SEH) (не C++) является гораздо лучшим подходом.</span><span class="sxs-lookup"><span data-stu-id="51ac9-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="51ac9-113">При возникновении исключения SEH управление переходит непосредственно к времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="51ac9-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="51ac9-114">Ошибка иногда возникает в подпрограмме, которая не может быть правильно очищена, и должна указывать на ошибку вызывающей стороне.</span><span class="sxs-lookup"><span data-stu-id="51ac9-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="51ac9-115">Подпрограмма должна возвращать ошибку вызывающему объекту, которая, в свою очередь, может возвращать ошибку вызывающему объекту и т. д.</span><span class="sxs-lookup"><span data-stu-id="51ac9-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="51ac9-116">Однако последняя Серверная подпрограммы в стеке должна вызвать исключение перед возвратом в RPC, чтобы указать RPC на то, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="51ac9-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51ac9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="51ac9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51ac9-118">Обработка исключений</span><span class="sxs-lookup"><span data-stu-id="51ac9-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 