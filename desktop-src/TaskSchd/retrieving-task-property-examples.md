---
title: Получение примеров свойств задачи
description: Чтобы получить свойства задачи, вызовите Итасксчедулер Activate, чтобы получить интерфейс объекта Task, а затем вызовите соответствующий метод ITask, чтобы получить интересующее вас свойство задачи.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- получение свойств задачи планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338692"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="b31a4-104">Получение примеров свойств задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="b31a4-105">Чтобы получить свойства задачи, вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс объекта Task, а затем вызовите соответствующий метод [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , чтобы получить интересующее вас свойство задачи.</span><span class="sxs-lookup"><span data-stu-id="b31a4-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="b31a4-106">В примерах кода, приведенных в нижней части страницы, показано, как получить различные свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="b31a4-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="b31a4-107">В примерах кода, приведенных в нижней части страницы, показано, как получить свойства, уникальные для объектов Task.</span><span class="sxs-lookup"><span data-stu-id="b31a4-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="b31a4-108">Сведения о других свойствах [*рабочих элементов*](w.md) , которые также применяются к задачам, см. в разделе [Получение примеров рабочих элементов](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="b31a4-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="b31a4-109">В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="b31a4-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="b31a4-110">Обратите внимание, что при извлечении свойства строки (например, имени приложения, параметров или рабочего каталога) необходимо вызвать [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память, выделенную для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="b31a4-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="b31a4-111">В следующей процедуре описывается получение свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="b31a4-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="b31a4-112">**Получение свойства задачи**</span><span class="sxs-lookup"><span data-stu-id="b31a4-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="b31a4-113">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="b31a4-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="b31a4-114">(В этих примерах предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="b31a4-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="b31a4-115">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="b31a4-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="b31a4-116">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="b31a4-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="b31a4-117">Вызовите соответствующий метод [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , чтобы получить интересующее вас свойство.</span><span class="sxs-lookup"><span data-stu-id="b31a4-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="b31a4-118">При необходимости обработайте свойство.</span><span class="sxs-lookup"><span data-stu-id="b31a4-118">Process the property as needed.</span></span> <span data-ttu-id="b31a4-119">(Эти примеры напечатают свойство на экране.)</span><span class="sxs-lookup"><span data-stu-id="b31a4-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="b31a4-120">Если возвращаемое свойство является строкой, вызовите [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память, выделенную для возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="b31a4-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="b31a4-121">Пример кода</span><span class="sxs-lookup"><span data-stu-id="b31a4-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="b31a4-122">См.</span><span class="sxs-lookup"><span data-stu-id="b31a4-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b31a4-123">Получение имени приложения, связанного с заданной задачей</span><span class="sxs-lookup"><span data-stu-id="b31a4-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="b31a4-124">Пример кода C/C++: получение имени приложения задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="b31a4-125">Получение максимального времени, в течение которого может выполняться задача и отображение этого числа на экране</span><span class="sxs-lookup"><span data-stu-id="b31a4-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="b31a4-126">Пример кода C/C++: получение Максрунтиме задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="b31a4-127">Получение строки параметра, которая выполняется при выполнении задачи и отображение этой строки на экране</span><span class="sxs-lookup"><span data-stu-id="b31a4-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="b31a4-128">Пример кода C/C++. получение параметров задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="b31a4-129">Получение [*уровня приоритета*](p.md) задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="b31a4-130">Пример кода C/C++: получение приоритета задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="b31a4-131">Получение [*рабочего каталога*](w.md) задачи и отображение пути к рабочему каталогу на экране</span><span class="sxs-lookup"><span data-stu-id="b31a4-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="b31a4-132">Пример кода C/C++: получение рабочего каталога задачи</span><span class="sxs-lookup"><span data-stu-id="b31a4-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="b31a4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b31a4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b31a4-134">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="b31a4-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 