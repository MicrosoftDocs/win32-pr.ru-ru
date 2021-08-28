---
Description: Ниже приведено краткое сравнение различных методов выделения памяти.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Сравнение методов выделения памяти
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 418ebbf96b1d6f714e1ae7f23f1c15e918ea0c6fa7eabdf7bb9157bb14808bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067904"
---
# <a name="comparing-memory-allocation-methods"></a>Сравнение методов выделения памяти

Ниже приведено краткое сравнение различных методов выделения памяти.

-   [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   **malloc**
-   **new**
-   [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

Хотя функции [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc)и [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) в конечном итоге выделяют память из той же кучи, каждая из них предоставляет слегка отличающийся набор функциональных возможностей. Например, **хеапаллок** может дать указание создавать исключение, если память не может быть выделена, возможность недоступна для **локалаллок**. **Локалаллок** поддерживает выделение дескрипторов, позволяющих перемещать базовую память при перераспределении без изменения значения дескриптора, возможность недоступна для **хеапаллок**.

начиная с 32-разрядных Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) и [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc) реализуются как функции-оболочки, которые вызывают [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) с помощью обработчика для кучи процесса по умолчанию. Таким образом, **GlobalAlloc** и **локалаллок** имеют большие издержки, чем **хеапаллок**.

Так как различные распределительы кучи обеспечивают различенную функциональность с помощью различных механизмов, необходимо освободить память с правильной функцией. Например, память, выделенная с помощью [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) , должна быть освобождена с помощью [**хеапфри**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) , а не [**функции LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) или [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree). Память, выделенная с помощью [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) или [**локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc) , должна быть запрошена, проверена и освобождена с помощью соответствующей глобальной или локальной функции.

Функция [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) позволяет указать дополнительные параметры для выделения памяти. Однако при выделении ресурсов используется гранулярность страницы, поэтому использование **VirtualAlloc** может привести к увеличению использования памяти.

Функция **malloc** имеет недостатки, зависящие от времени выполнения. У оператора **New** есть недостатки, зависящие от компилятора и зависящие от языка.

Функция [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) имеет преимущество при работе с C, C++ или Visual Basic. Это также единственный способ совместного использования памяти в приложении на основе COM, поскольку MIDL использует **CoTaskMemAlloc** и [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) для маршалирования памяти.


## <a name="examples"></a>Примеры

* [Резервирование и фиксация памяти](./reserving-and-committing-memory.md)

* [Пример расширений AWE](./awe-example.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Глобальные и локальные функции](global-and-local-functions.md)
</dt> <dt>

[Функции кучи](heap-functions.md)
</dt> <dt>

[Функции виртуальной памяти](virtual-memory-functions.md)
</dt> </dl>

 

 