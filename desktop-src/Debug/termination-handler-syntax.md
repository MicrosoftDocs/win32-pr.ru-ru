---
description: '\_ \_ \_ \_ Ключевые слова try и finally используются для создания обработчика завершения. В следующем примере показана структура обработчика завершения.'
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Синтаксис Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655869"
---
# <a name="termination-handler-syntax"></a><span data-ttu-id="f8c8e-104">Синтаксис Termination-Handler</span><span class="sxs-lookup"><span data-stu-id="f8c8e-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="f8c8e-105">Ключевые слова **\_ \_ try** и **\_ \_ finally** используются для создания обработчика завершения.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="f8c8e-106">В следующем примере показана структура обработчика завершения.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-106">The following example shows the structure of a termination handler.</span></span>


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



<span data-ttu-id="f8c8e-107">Примеры см. в разделе [использование обработчика завершения](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="f8c8e-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="f8c8e-108">Как и в случае с обработчиком исключений, блок **\_ \_ try** и блок **\_ \_ finally** должны заключаться в фигурные скобки ( {} ), и использование оператора **goto** для перехода в любой блок не допускается.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="f8c8e-109">Блок **\_ \_ try** содержит защищенный текст кода, защищенного обработчиком завершения.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="f8c8e-110">Функция может иметь любое количество обработчиков завершения, и эти блоки обработки завершения могут быть вложены в одну и ту же функцию или в разные функции.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="f8c8e-111">Блок **\_ \_ finally** выполняется каждый раз, когда поток управления покидает блок **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="f8c8e-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="f8c8e-112">Однако блок **\_ \_ finally** не выполняется при вызове любой из следующих функций в блоке **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)или **Abort**.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="f8c8e-113">Блок **\_ \_ finally** выполняется в контексте функции, в которой находится обработчик завершения.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="f8c8e-114">Это означает, что блок **\_ \_ finally** может обращаться к локальным переменным этой функции.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="f8c8e-115">Выполнение блока **\_ \_ finally** может завершиться любым из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="f8c8e-116">Выполнение последнего оператора в блоке и продолжение до следующей инструкции</span><span class="sxs-lookup"><span data-stu-id="f8c8e-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="f8c8e-117">Использование оператора Control (**return**, **break**, **Continue** или **goto**)</span><span class="sxs-lookup"><span data-stu-id="f8c8e-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="f8c8e-118">Использование **longjmp** или переход к обработчику исключений</span><span class="sxs-lookup"><span data-stu-id="f8c8e-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="f8c8e-119">Если выполнение блока **\_ \_ try** завершается из-за исключения, вызывающего блок обработки исключений обработчика исключений на основе кадров, блок **\_ \_ finally** выполняется перед выполнением блока обработки исключений.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="f8c8e-120">Аналогичным образом, вызов функции библиотеки времени выполнения C **longjmp** из блока **\_ \_ try** приводит к тому, что выполнение блока **\_ \_ finally** до возобновления выполнения на целевом объекте операции **longjmp** .</span><span class="sxs-lookup"><span data-stu-id="f8c8e-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="f8c8e-121">Если выполнение блока **\_ \_ try** завершается из-за оператора управления (**return**, **break**, **Continue** или **goto**), выполняется блок **\_ \_ finally** .</span><span class="sxs-lookup"><span data-stu-id="f8c8e-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="f8c8e-122">Функция [**абнормалтерминатион**](abnormaltermination.md) может использоваться в блоке **\_ \_ finally** для определения того, был ли блок **\_ \_ try** завершен последовательно, то есть вне зависимости от того, достигнут ли он закрывающей фигурной скобкой (}).</span><span class="sxs-lookup"><span data-stu-id="f8c8e-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="f8c8e-123">Выход из блока **\_ \_ try** из-за вызова **longjmp**, перехода к обработчику исключений или оператору **return**, **break**, **Continue** или **goto** считается аномальным завершением.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="f8c8e-124">Обратите внимание, что неуспешное завершение последовательно приводит к тому, что система ищет все кадры стека в порядке, чтобы определить, должны ли быть вызваны какие-либо обработчики завершения.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="f8c8e-125">Это может привести к снижению производительности из-за выполнения сотен инструкций.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="f8c8e-126">Чтобы избежать аварийного завершения обработчика завершения, выполнение продолжается до конца блока.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="f8c8e-127">Можно также выполнить инструкцию **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="f8c8e-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="f8c8e-128">Оператор **\_ \_ Leave** позволяет немедленно завершить блок **\_ \_ try** , не вызывая аварийного завершения и снижения его производительности.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="f8c8e-129">Чтобы определить, поддерживается ли оператор **\_ \_ Leave** , проверьте документацию по компилятору.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="f8c8e-130">Если выполнение блока **\_ \_ finally** завершается из-за инструкции **return** Control, то оно эквивалентно **переходу** на закрывающую фигурную скобку во включающей функции.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="f8c8e-131">Поэтому функция, включающая функцию, будет возвращать значение.</span><span class="sxs-lookup"><span data-stu-id="f8c8e-131">Therefore, the enclosing function will return.</span></span>

 

 
