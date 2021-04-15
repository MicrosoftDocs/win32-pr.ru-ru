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
# <a name="using-an-exception-handler"></a>Использование обработчика исключений

В следующих примерах демонстрируется использование обработчика исключений.

## <a name="example-1"></a>Пример 1

В следующем фрагменте кода используется структурированная обработка исключений для проверки того, что операция деления в 2 32-разрядных целых чисел приведет к появлению ошибки деления на ноль. Если это происходит, функция возвращает **значение false**— в противном случае возвращается **значение true**.


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



## <a name="example-2"></a>Пример 2

Следующий пример функции вызывает функцию [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) и использует структурированную обработку исключений для проверки исключения точки останова. При возникновении такой функции функция возвращает **значение false**— в противном случае возвращается **значение true**.

Выражение фильтра в примере использует функцию [**GetExceptionCode**](getexceptioncode.md) для проверки типа исключения перед выполнением обработчика. Это позволяет системе продолжить поиск соответствующего обработчика, если возникает исключение другого типа.

Кроме того, использование оператора **return** в блоке **\_ \_ try** обработчика исключений отличается от использования **возврата** в блоке **\_ \_ try** обработчика завершения, что приводит к аномальному завершению работы блока **\_ \_ try** . Это допустимое использование оператора return в обработчике исключений.


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



Возвращать \_ обработчик исключений \_ из фильтра исключений следует только в том случае, если ожидается тип исключения и известный адрес сбоя. Необходимо разрешить обработчику исключений по умолчанию обрабатывать непредвиденные типы исключений и ошибочные адреса.

## <a name="example-3"></a>Пример 3

В следующем примере показано взаимодействие вложенных обработчиков. Функция [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) вызывает исключение в защищенном тексте обработчика завершения, который находится внутри защищенного тела обработчика исключений. Это исключение заставляет систему оценить функцию FilterFunction, возвращаемое значение которой в свою очередь приводит к вызову обработчика исключений. Однако перед выполнением блока обработчика исключений выполняется блок **\_ \_ finally** обработчика завершения, поскольку поток управления покинул блок **\_ \_ try** обработчика завершения.


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



 

 
