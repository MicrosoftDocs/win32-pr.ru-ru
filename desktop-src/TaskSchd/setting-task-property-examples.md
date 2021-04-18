---
title: Примеры свойств задач
description: Чтобы задать свойства задачи, вызовите Итасксчедулер Activate, чтобы получить интерфейс объекта Task, а затем вызовите соответствующий метод ITask, чтобы задать интересующее вас свойство задачи.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- Задание свойств задачи планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681670"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="170e2-104">Примеры свойств задач</span><span class="sxs-lookup"><span data-stu-id="170e2-104">Setting Task Property Examples</span></span>

<span data-ttu-id="170e2-105">Чтобы задать свойства задачи, вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс объекта Task, а затем вызовите соответствующий метод [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , чтобы задать интересующее вас свойство задачи.</span><span class="sxs-lookup"><span data-stu-id="170e2-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="170e2-106">В примерах кода, приведенных в нижней части страницы, показано, как задать свойства, уникальные для объектов Task.</span><span class="sxs-lookup"><span data-stu-id="170e2-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="170e2-107">Сведения о других свойствах [*рабочих элементов*](w.md) , которые также применяются к задачам, см. в разделе [Определение свойств рабочего элемента](setting-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="170e2-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="170e2-108">В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="170e2-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="170e2-109">В следующих примерах измененный объект задачи всегда сохраняется на диск с помощью вызова [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="170e2-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="170e2-110">(Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, наследуемым объектом Task.)</span><span class="sxs-lookup"><span data-stu-id="170e2-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="170e2-111">В следующей процедуре описывается задание свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="170e2-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="170e2-112">**Задание свойства задачи**</span><span class="sxs-lookup"><span data-stu-id="170e2-112">**To set a task property**</span></span>

1.  <span data-ttu-id="170e2-113">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="170e2-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="170e2-114">(В этих примерах предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="170e2-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="170e2-115">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="170e2-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="170e2-116">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="170e2-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="170e2-117">Вызовите соответствующий метод [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , чтобы задать интересующее вас свойство.</span><span class="sxs-lookup"><span data-stu-id="170e2-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="170e2-118">Вызовите метод [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить измененный объект задачи на диск.</span><span class="sxs-lookup"><span data-stu-id="170e2-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="170e2-119">Пример кода</span><span class="sxs-lookup"><span data-stu-id="170e2-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="170e2-120">См.</span><span class="sxs-lookup"><span data-stu-id="170e2-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="170e2-121">Задание имени приложения, связанного с известной задачей</span><span class="sxs-lookup"><span data-stu-id="170e2-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="170e2-122">Пример кода C/C++: Задание имени приложения</span><span class="sxs-lookup"><span data-stu-id="170e2-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="170e2-123">Установка максимального времени выполнения известной задачи</span><span class="sxs-lookup"><span data-stu-id="170e2-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="170e2-124">Пример кода C/C++: Настройка Максрунтиме</span><span class="sxs-lookup"><span data-stu-id="170e2-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="170e2-125">Очистка всех параметров командной строки, связанных с известной задачей</span><span class="sxs-lookup"><span data-stu-id="170e2-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="170e2-126">Пример кода C/C++: Задание параметров задачи</span><span class="sxs-lookup"><span data-stu-id="170e2-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="170e2-127">В этом примере задается приоритет задачи теста, а затем задача сохраняется.</span><span class="sxs-lookup"><span data-stu-id="170e2-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="170e2-128">В этом примере предполагается, что тестовая задача уже существует на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="170e2-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="170e2-129">Пример кода C/C++: Настройка приоритета задачи</span><span class="sxs-lookup"><span data-stu-id="170e2-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="170e2-130">Задание [*рабочего каталога*](w.md) для известной задачи</span><span class="sxs-lookup"><span data-stu-id="170e2-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="170e2-131">Пример кода C/C++: Настройка рабочего каталога</span><span class="sxs-lookup"><span data-stu-id="170e2-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="170e2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="170e2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="170e2-133">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="170e2-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 