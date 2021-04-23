---
title: Получение примеров свойств рабочего элемента
description: Чтобы получить свойства рабочего элемента, вызовите Итасксчедулер Activate, чтобы получить интерфейс объекта рабочего элемента, а затем вызовите соответствующий метод, чтобы получить интересующее вас свойство задачи.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- получение свойств рабочего элемента планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413236"
---
# <a name="retrieving-work-item-property-examples"></a><span data-ttu-id="c2334-104">Получение примеров свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="c2334-104">Retrieving Work Item Property Examples</span></span>

<span data-ttu-id="c2334-105">Чтобы получить свойства рабочего элемента, вызовите [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс объекта рабочего элемента, а затем вызовите соответствующий метод, чтобы получить интересующее вас свойство задачи.</span><span class="sxs-lookup"><span data-stu-id="c2334-105">To retrieve the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to retrieve the task property you are interested in.</span></span> <span data-ttu-id="c2334-106">В настоящее время единственными допустимыми рабочими элементами являются задачи.</span><span class="sxs-lookup"><span data-stu-id="c2334-106">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="c2334-107">В примерах кода, приведенных в нижней части этой страницы, показано, как получить свойства, которые применяются ко всем рабочим элементам.</span><span class="sxs-lookup"><span data-stu-id="c2334-107">The code examples listed at the bottom of this page show how to retrieve the properties that apply to all work items.</span></span> <span data-ttu-id="c2334-108">Другие свойства, которые являются уникальными для задач, см. в разделе [Задание примеров свойств задачи](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c2334-108">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="c2334-109">В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="c2334-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="c2334-110">Обратите внимание, что при извлечении свойства строки (например, комментария к рабочему элементу) необходимо вызвать [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память, выделенную для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="c2334-110">Note that if you are retrieving a string property (such as comment for a work item), you must call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="c2334-111">В следующей процедуре описывается получение свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="c2334-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="c2334-112">**Получение свойства задачи**</span><span class="sxs-lookup"><span data-stu-id="c2334-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="c2334-113">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c2334-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="c2334-114">(В этих примерах предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="c2334-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="c2334-115">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="c2334-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="c2334-116">(Обратите внимание, что в настоящее время задачи являются единственным допустимым типом рабочего элемента.)</span><span class="sxs-lookup"><span data-stu-id="c2334-116">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="c2334-117">Вызовите соответствующий метод, чтобы получить интересующее вас свойство.</span><span class="sxs-lookup"><span data-stu-id="c2334-117">Call the appropriate method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="c2334-118">При необходимости обработайте свойство.</span><span class="sxs-lookup"><span data-stu-id="c2334-118">Process the property as needed.</span></span> <span data-ttu-id="c2334-119">(В этих примерах просто распечатывается свойство на экране.)</span><span class="sxs-lookup"><span data-stu-id="c2334-119">(These examples simply print the property to the screen.)</span></span>
5.  <span data-ttu-id="c2334-120">Если возвращаемое свойство является строкой, вызовите [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память, выделенную для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="c2334-120">If the returned property is a string, call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="c2334-121">Пример кода</span><span class="sxs-lookup"><span data-stu-id="c2334-121">For a code example of</span></span>                                                                        | <span data-ttu-id="c2334-122">См.</span><span class="sxs-lookup"><span data-stu-id="c2334-122">See</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2334-123">Получение сведений об учетной записи известной задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-123">Retrieving the account information of a known task</span></span>                                           | [<span data-ttu-id="c2334-124">Пример кода C/C++: получение сведений об учетной записи задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-124">C/C++ Code Example: Retrieving Task Account Information</span></span>](c-c-code-example-retrieving-task-account-information.md)       |
| <span data-ttu-id="c2334-125">Получение строки комментария известной задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-125">Retrieving the comment string of a known task</span></span>                                                | [<span data-ttu-id="c2334-126">Пример кода C/C++: получение комментария к задаче</span><span class="sxs-lookup"><span data-stu-id="c2334-126">C/C++ Code Example: Retrieving a Task Comment</span></span>](c-c-code-example-retrieving-a-task-comment.md)                           |
| <span data-ttu-id="c2334-127">Получение имени создателя задачи и отображение ее на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-127">Retrieving the name of the creator of the task and displaying it on the screen</span></span>               | [<span data-ttu-id="c2334-128">Пример кода C/C++: получение создателя задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-128">C/C++ Code Example: Retrieving the Task Creator</span></span>](c-c-code-example-retrieving-the-task-creator.md)                       |
| <span data-ttu-id="c2334-129">Получение последнего кода выхода, возвращенного известной задачей</span><span class="sxs-lookup"><span data-stu-id="c2334-129">Retrieving the last exit code returned by a known task</span></span>                                       | [<span data-ttu-id="c2334-130">Пример кода C/C++: получение кода завершения задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-130">C/C++ Code Example: Retrieving Task Exit Code</span></span>](c-c-code-example-retrieving-task-exit-code.md)                           |
| <span data-ttu-id="c2334-131">Получение времени ожидания простоя задачи и отображение ее на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-131">Retrieving the idle-wait time of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="c2334-132">Пример кода C/C++: получение времени ожидания задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-132">C/C++ Code Example: Retrieving Task Idle-wait Time</span></span>](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| <span data-ttu-id="c2334-133">Получение времени последнего выполнения задачи и его отображение на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-133">Retrieving the time the task was last run and displaying it on the screen</span></span>                    | [<span data-ttu-id="c2334-134">Пример кода C/C++: получение времени Мострецентрун задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-134">C/C++ Code Example: Retrieving the Task MostRecentRun Time</span></span>](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| <span data-ttu-id="c2334-135">Извлечение при следующем запланированном запуске задачи и отображении этого времени на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-135">Retrieving the next time the task is scheduled to run and displaying that time on the screen</span></span> | [<span data-ttu-id="c2334-136">Пример кода C/C++: получение времени Некструн задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-136">C/C++ Code Example: Retrieving the Task NextRun Time</span></span>](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| <span data-ttu-id="c2334-137">Получение времени выполнения задачи и отображение их на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-137">Retrieving the run times of the task and displaying them on the screen</span></span>                       | [<span data-ttu-id="c2334-138">Пример кода C/C++: получение времени выполнения задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-138">C/C++ Code Example: Retrieving Task Run Times</span></span>](c-c-code-example-retrieving-task-run-times.md)                           |
| <span data-ttu-id="c2334-139">Получение текущего состояния задачи и отображение ее на экране</span><span class="sxs-lookup"><span data-stu-id="c2334-139">Retrieving the current status of the task and displaying it on the screen</span></span>                    | [<span data-ttu-id="c2334-140">Пример кода C/C++: получение состояния задачи</span><span class="sxs-lookup"><span data-stu-id="c2334-140">C/C++ Code Example: Retrieving Task Status</span></span>](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c2334-141">См. также</span><span class="sxs-lookup"><span data-stu-id="c2334-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2334-142">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="c2334-142">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 