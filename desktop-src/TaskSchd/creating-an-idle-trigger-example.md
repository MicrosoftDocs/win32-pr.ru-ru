---
title: Пример создания триггера Idle
description: Чтобы создать триггер простоя, необходимо указать триггер простоя при создании триггера, а также задать время простоя для задачи. Сведения об условиях простоя см. в разделе условия простоя задачи.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338529"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="0699e-104">Пример создания триггера Idle</span><span class="sxs-lookup"><span data-stu-id="0699e-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="0699e-105">Чтобы создать триггер простоя, необходимо указать триггер простоя при создании триггера, а также задать время простоя для задачи.</span><span class="sxs-lookup"><span data-stu-id="0699e-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="0699e-106">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="0699e-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="0699e-107">После создания триггера просто вызовите [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить новый триггер на диск.</span><span class="sxs-lookup"><span data-stu-id="0699e-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="0699e-108">В следующей процедуре описывается создание триггера Idle для известной задачи.</span><span class="sxs-lookup"><span data-stu-id="0699e-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="0699e-109">**Создание триггера Idle для известной задачи**</span><span class="sxs-lookup"><span data-stu-id="0699e-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="0699e-110">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0699e-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0699e-111">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="0699e-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0699e-112">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="0699e-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0699e-113">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="0699e-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="0699e-114">Вызовите [**сетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) , чтобы указать, как долго система должна оставаться в состоянии простоя, прежде чем будет срабатывать триггер.</span><span class="sxs-lookup"><span data-stu-id="0699e-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="0699e-115">(Обратите внимание, что **сетидлеваит** наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="0699e-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="0699e-116">Определите структуру [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) и вызовите [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) , чтобы создать триггер Idle.</span><span class="sxs-lookup"><span data-stu-id="0699e-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="0699e-117">(Обратите внимание, что **CreateTrigger** наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span><span class="sxs-lookup"><span data-stu-id="0699e-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="0699e-118">Сохраните задачу с новым триггером бездействия на диск с помощью [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="0699e-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="0699e-119">(Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="0699e-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="0699e-120">Вызовите метод **ITask:: Release** , чтобы освободить все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0699e-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="0699e-121">(Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="0699e-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="0699e-122">Пример кода</span><span class="sxs-lookup"><span data-stu-id="0699e-122">For a code example of</span></span>                         | <span data-ttu-id="0699e-123">См.</span><span class="sxs-lookup"><span data-stu-id="0699e-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0699e-124">Создание триггера Idle для существующей задачи</span><span class="sxs-lookup"><span data-stu-id="0699e-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="0699e-125">Пример кода C/C++. Создание триггера Idle</span><span class="sxs-lookup"><span data-stu-id="0699e-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0699e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0699e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0699e-127">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="0699e-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 