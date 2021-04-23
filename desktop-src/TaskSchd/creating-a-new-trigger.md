---
title: Создание нового триггера
description: Для создания триггера необходимо использовать три интерфейса.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413324"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="cdb53-103">Создание нового триггера</span><span class="sxs-lookup"><span data-stu-id="cdb53-103">Creating a New Trigger</span></span>

<span data-ttu-id="cdb53-104">Для создания триггера необходимо использовать три интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cdb53-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="cdb53-105">[**Исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) предоставляет метод [**Исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) для создания объекта Trigger, [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) предоставляет метод [**итасктригжер:: сеттригжер**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) для установки критериев триггера, а COM-интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) предоставляет метод **Save** для сохранения нового триггера на диск.</span><span class="sxs-lookup"><span data-stu-id="cdb53-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="cdb53-106">В следующей процедуре описывается создание нового триггера.</span><span class="sxs-lookup"><span data-stu-id="cdb53-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="cdb53-107">**Создание нового триггера**</span><span class="sxs-lookup"><span data-stu-id="cdb53-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="cdb53-108">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="cdb53-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="cdb53-109">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="cdb53-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="cdb53-110">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="cdb53-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="cdb53-111">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="cdb53-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="cdb53-112">Вызовите [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) , чтобы создать объект триггера.</span><span class="sxs-lookup"><span data-stu-id="cdb53-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="cdb53-113">(Обратите внимание, что [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="cdb53-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="cdb53-114">Определите структуру [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="cdb53-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="cdb53-115">Обратите внимание, что для членов **\_ триггера задачи** вбегиндай, вбегинмонс и вбегинеар должен быть задан допустимый день, месяц и год соответственно.</span><span class="sxs-lookup"><span data-stu-id="cdb53-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="cdb53-116">Вызовите [**итасктригжер:: сеттригжер**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) , чтобы задать критерии триггера.</span><span class="sxs-lookup"><span data-stu-id="cdb53-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="cdb53-117">Сохраните задачу с новым триггером на диск с помощью [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="cdb53-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="cdb53-118">(Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="cdb53-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="cdb53-119">Вызовите [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cdb53-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="cdb53-120">(Обратите внимание, что **выпуск** — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="cdb53-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="cdb53-121">Пример кода</span><span class="sxs-lookup"><span data-stu-id="cdb53-121">For a code example of</span></span>                       | <span data-ttu-id="cdb53-122">См.</span><span class="sxs-lookup"><span data-stu-id="cdb53-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb53-123">Создание нового триггера для существующей задачи</span><span class="sxs-lookup"><span data-stu-id="cdb53-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="cdb53-124">Пример кода C/C++: Создание триггера задачи</span><span class="sxs-lookup"><span data-stu-id="cdb53-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="cdb53-125">См. также</span><span class="sxs-lookup"><span data-stu-id="cdb53-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb53-126">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="cdb53-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 