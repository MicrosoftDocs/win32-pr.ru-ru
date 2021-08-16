---
description: Переменные условия — это примитивы синхронизации, которые позволяют потокам ожидать выполнения определенного условия. Переменные условия — это объекты пользовательского режима, которые нельзя совместно использовать в процессах.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Переменные условия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d7ee98b4f5c5a65e633f7d1647b6c624840f9740efb639959c1500bec591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886364"
---
# <a name="condition-variables"></a>Переменные условия

Переменные условия — это примитивы синхронизации, которые позволяют потокам ожидать выполнения определенного условия. Переменные условия — это объекты пользовательского режима, которые нельзя совместно использовать в процессах.

Переменные условия позволяют потокам атомарно освобождать блокировку и переходить в спящий режим. Их можно использовать с критическими секциями или с упрощенными блокировками потоков чтения/записи (SRW). Переменные условия поддерживают операции, которые переводят ожидающие потоки в спящий режим или пробуждать все. После того как поток пробуждении, он повторно получает блокировку, освобожденную, когда поток перешел в спящий режим.

Обратите внимание, что вызывающий объект должен выделить структуру **\_ переменной условия** и инициализировать ее, вызвав [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (для динамической инициализации структуры) или присвоить переменной Structure значение **\_ \_ init переменной Condition** (для статической инициализации структуры).

**Windows Server 2003 и Windows XP:** Переменные условия не поддерживаются.

Ниже приведены функции переменных условия.



| Переменная Condition, функция                                        | Описание                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Инициализирует переменную условия.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Закрывает указанную переменную условия и освобождает указанную критическую секцию как атомарную операцию. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Закрывает указанную переменную условия и освобождает указанную блокировку SRW как атомарную операцию.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Пробуждает все потоки, ожидающие заданную переменную условия.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Пробуждает один поток, ожидающий заданную переменную условия.                                             |



 

В следующем псевдокоде показан типичный шаблон использования переменных условия.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Например, в реализации блокировки потоков чтения/записи `TestPredicate` функция проверяет, совместим ли текущий запрос на блокировку с существующими владельцами. Если это так, получите блокировку; в противном случае — спящий режим. Более подробный пример см. в разделе [Использование переменных условия](using-condition-variables.md).

Переменные условия подчиняются ложным пробуждениям (не связанным с явной функцией пробуждения) и украденным пробуждениям (другой поток управляет выполнением до потока пробуждении). Поэтому следует проверить предикат (обычно в цикле **while** ) после возврата в спящий режим.

Можно пробудить другие потоки с помощью [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) или [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) внутри или вне блокировки, связанной с переменной Condition. Обычно лучше снять блокировку перед пробуждением других потоков, чтобы уменьшить число переключений контекста.

Часто удобно использовать более одной переменной условия с одной блокировкой. Например, реализация блокировки потоков чтения/записи может использовать одну критическую секцию, но отдельные переменные условия для читателей и модулей записи.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование переменных условия](using-condition-variables.md)
</dt> </dl>

 

 
