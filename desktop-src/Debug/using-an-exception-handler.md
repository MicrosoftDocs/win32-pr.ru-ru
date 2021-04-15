---
description: В следующих примерах демонстрируется использование обработчика исключений.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Использование обработчика исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655866"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="a87d5-103">Использование обработчика исключений</span><span class="sxs-lookup"><span data-stu-id="a87d5-103">Using an Exception Handler</span></span>

<span data-ttu-id="a87d5-104">В следующих примерах демонстрируется использование обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="a87d5-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="a87d5-105">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a87d5-105">Example 1</span></span>

<span data-ttu-id="a87d5-106">В следующем фрагменте кода используется структурированная обработка исключений для проверки того, что операция деления в 2 32-разрядных целых чисел приведет к появлению ошибки деления на ноль.</span><span class="sxs-lookup"><span data-stu-id="a87d5-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="a87d5-107">Если это происходит, функция возвращает **значение false**— в противном случае возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a87d5-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="a87d5-108">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a87d5-108">Example 2</span></span>

<span data-ttu-id="a87d5-109">Следующий пример функции вызывает функцию [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) и использует структурированную обработку исключений для проверки исключения точки останова.</span><span class="sxs-lookup"><span data-stu-id="a87d5-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="a87d5-110">При возникновении такой функции функция возвращает **значение false**— в противном случае возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a87d5-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="a87d5-111">Выражение фильтра в примере использует функцию [**GetExceptionCode**](getexceptioncode.md) для проверки типа исключения перед выполнением обработчика.</span><span class="sxs-lookup"><span data-stu-id="a87d5-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="a87d5-112">Это позволяет системе продолжить поиск соответствующего обработчика, если возникает исключение другого типа.</span><span class="sxs-lookup"><span data-stu-id="a87d5-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="a87d5-113">Кроме того, использование оператора **return** в блоке **\_ \_ try** обработчика исключений отличается от использования **возврата** в блоке **\_ \_ try** обработчика завершения, что приводит к аномальному завершению работы блока **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="a87d5-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="a87d5-114">Это допустимое использование оператора return в обработчике исключений.</span><span class="sxs-lookup"><span data-stu-id="a87d5-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="a87d5-115">Возвращать \_ обработчик исключений \_ из фильтра исключений следует только в том случае, если ожидается тип исключения и известный адрес сбоя.</span><span class="sxs-lookup"><span data-stu-id="a87d5-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="a87d5-116">Необходимо разрешить обработчику исключений по умолчанию обрабатывать непредвиденные типы исключений и ошибочные адреса.</span><span class="sxs-lookup"><span data-stu-id="a87d5-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="a87d5-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a87d5-117">Example 3</span></span>

<span data-ttu-id="a87d5-118">В следующем примере показано взаимодействие вложенных обработчиков.</span><span class="sxs-lookup"><span data-stu-id="a87d5-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="a87d5-119">Функция [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) вызывает исключение в защищенном тексте обработчика завершения, который находится внутри защищенного тела обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="a87d5-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="a87d5-120">Это исключение заставляет систему оценить функцию FilterFunction, возвращаемое значение которой в свою очередь приводит к вызову обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="a87d5-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="a87d5-121">Однако перед выполнением блока обработчика исключений выполняется блок **\_ \_ finally** обработчика завершения, поскольку поток управления покинул блок **\_ \_ try** обработчика завершения.</span><span class="sxs-lookup"><span data-stu-id="a87d5-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
