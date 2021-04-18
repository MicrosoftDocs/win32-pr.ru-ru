---
description: '\_ \_ \_ \_ Ключевые слова try и Except используются для создания обработчика исключений на основе кадров. В следующем примере показана структура обработчика исключений.'
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Синтаксис Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538309"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="eb948-104">Синтаксис Exception-Handler</span><span class="sxs-lookup"><span data-stu-id="eb948-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="eb948-105">Ключевые слова **\_ \_ try** и **\_ \_ except** используются для создания обработчика исключений на основе кадров.</span><span class="sxs-lookup"><span data-stu-id="eb948-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="eb948-106">В следующем примере показана структура обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="eb948-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="eb948-107">Обратите внимание, что блок **\_ \_ try** и блок обработчика исключений должны иметь фигурные скобки ( {} ).</span><span class="sxs-lookup"><span data-stu-id="eb948-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="eb948-108">Использование оператора **goto** для перехода в тело блока **\_ \_ try** или в блок обработчика исключений не допускается.</span><span class="sxs-lookup"><span data-stu-id="eb948-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="eb948-109">Это правило применяется как к обработчикам исключений, так и к обработчикам завершения.</span><span class="sxs-lookup"><span data-stu-id="eb948-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="eb948-110">Блок **\_ \_ try** содержит защищенный текст кода, который защищается обработчиком исключений.</span><span class="sxs-lookup"><span data-stu-id="eb948-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="eb948-111">Функция может иметь любое количество обработчиков исключений, и эти операторы обработки исключений могут быть вложены в одну и ту же функцию или в разные функции.</span><span class="sxs-lookup"><span data-stu-id="eb948-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="eb948-112">Если в блоке **\_ \_ try** возникает исключение, система получает управление и начинает поиск обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="eb948-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="eb948-113">Подробное описание этого поиска см. в разделе [обработка исключений](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="eb948-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="eb948-114">Обработчик исключений получает только исключения, происходящие в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="eb948-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="eb948-115">Это означает, что если блок **\_ \_ try** содержит вызов функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) или [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , то исключения, происходящие в новом процессе или потоке, не отправляются в этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="eb948-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="eb948-116">Система вычисляет критерий фильтра каждого обработчика исключений, который защищает код, в котором произошло исключение, до тех пор, пока не будет обработано исключение или не будет больше обработчиков.</span><span class="sxs-lookup"><span data-stu-id="eb948-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="eb948-117">Выражение фильтра должно оцениваться как одно из трех следующих значений.</span><span class="sxs-lookup"><span data-stu-id="eb948-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="eb948-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eb948-118">Value</span></span>                              | <span data-ttu-id="eb948-119">Значение</span><span class="sxs-lookup"><span data-stu-id="eb948-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb948-120">**\_обработчик выполнения \_ исключения**</span><span class="sxs-lookup"><span data-stu-id="eb948-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="eb948-121">Система передает управление обработчику исключений, и выполнение продолжится в кадре стека, в котором находится обработчик.</span><span class="sxs-lookup"><span data-stu-id="eb948-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="eb948-122">**\_Поиск продолжения \_ исключения**</span><span class="sxs-lookup"><span data-stu-id="eb948-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="eb948-123">Система продолжит поиск обработчика.</span><span class="sxs-lookup"><span data-stu-id="eb948-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="eb948-124">**\_продолжение \_ выполнения исключения**</span><span class="sxs-lookup"><span data-stu-id="eb948-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="eb948-125">Система останавливает поиск обработчика и возвращает управление в точку, в которой произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="eb948-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="eb948-126">Если исключение недоступно, это приводит к исключению исключения, которое не может **быть исключено \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="eb948-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="eb948-127">Критерий фильтра вычисляется в контексте функции, в которой находится обработчик исключений, несмотря на то, что исключение могло произойти в другой функции.</span><span class="sxs-lookup"><span data-stu-id="eb948-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="eb948-128">Это означает, что критерий фильтра может получить доступ к локальным переменным функции.</span><span class="sxs-lookup"><span data-stu-id="eb948-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="eb948-129">Аналогичным образом блок обработчика исключений может обращаться к локальным переменным функции, в которой она находится.</span><span class="sxs-lookup"><span data-stu-id="eb948-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="eb948-130">Дополнительные примеры см. в разделе [использование обработчика исключений](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="eb948-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="eb948-131">Дополнительные сведения о выражениях фильтров и функциях фильтрации см. в разделе [обработка исключений на основе кадров](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="eb948-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
