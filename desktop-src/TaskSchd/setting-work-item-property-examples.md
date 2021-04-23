---
title: Примеры настройки свойств рабочих элементов
description: Чтобы задать свойства рабочего элемента, вызовите Итасксчедулер Activate, чтобы получить интерфейс объекта рабочего элемента, а затем вызовите соответствующий метод, чтобы задать интересующее вас свойство задачи. В настоящее время единственными допустимыми рабочими элементами являются задачи.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- Настройка свойств рабочего элемента планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987725"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="da921-105">Примеры настройки свойств рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="da921-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="da921-106">Чтобы задать свойства рабочего элемента, вызовите [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс объекта рабочего элемента, а затем вызовите соответствующий метод, чтобы задать интересующее вас свойство задачи.</span><span class="sxs-lookup"><span data-stu-id="da921-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="da921-107">В настоящее время единственными допустимыми рабочими элементами являются задачи.</span><span class="sxs-lookup"><span data-stu-id="da921-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="da921-108">В примерах кода, приведенных в нижней части страницы, показано, как задать свойства, которые применяются ко всем рабочим элементам.</span><span class="sxs-lookup"><span data-stu-id="da921-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="da921-109">Другие свойства, которые являются уникальными для задач, см. в разделе [Задание примеров свойств задачи](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="da921-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="da921-110">В следующем примере кода все интерфейсы освобождаются после того, как они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="da921-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="da921-111">В следующих примерах измененный объект всегда сохраняется на диск с помощью вызова [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="da921-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="da921-112">(Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, наследуемым объектом Task.)</span><span class="sxs-lookup"><span data-stu-id="da921-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="da921-113">В следующей процедуре описывается задание свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="da921-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="da921-114">**Задание свойства задачи**</span><span class="sxs-lookup"><span data-stu-id="da921-114">**To set a task property**</span></span>

1.  <span data-ttu-id="da921-115">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="da921-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="da921-116">(В этих примерах предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="da921-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="da921-117">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="da921-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="da921-118">(Обратите внимание, что в настоящее время задачи являются единственным допустимым типом рабочего элемента.)</span><span class="sxs-lookup"><span data-stu-id="da921-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="da921-119">Вызовите соответствующий метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , чтобы задать интересующее вас свойство.</span><span class="sxs-lookup"><span data-stu-id="da921-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="da921-120">Обратите внимание, что методы **исчедуледворкитем** наследуются интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="da921-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="da921-121">Вызовите метод [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить измененный объект задачи на диск.</span><span class="sxs-lookup"><span data-stu-id="da921-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="da921-122">Пример кода</span><span class="sxs-lookup"><span data-stu-id="da921-122">For a code example of</span></span>                            | <span data-ttu-id="da921-123">См.</span><span class="sxs-lookup"><span data-stu-id="da921-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da921-124">Настройка сведений об учетной записи для известной задачи</span><span class="sxs-lookup"><span data-stu-id="da921-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="da921-125">Пример кода C/C++: Задание сведений об учетной записи задачи</span><span class="sxs-lookup"><span data-stu-id="da921-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="da921-126">Задание комментария к известной задаче</span><span class="sxs-lookup"><span data-stu-id="da921-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="da921-127">Пример кода C/C++: Задание комментария к задаче</span><span class="sxs-lookup"><span data-stu-id="da921-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="da921-128">См. также</span><span class="sxs-lookup"><span data-stu-id="da921-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da921-129">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="da921-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 