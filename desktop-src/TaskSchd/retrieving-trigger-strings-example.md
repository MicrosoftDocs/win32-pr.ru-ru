---
title: Пример получения строк триггера
description: Вы можете получить строки триггера известного триггера, используя интерфейс Исчедуледворкитем или Итасктригжер, в зависимости от типа объекта, с которым вы работаете.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Получение строк триггера планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681668"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="f1cc0-104">Пример получения строк триггера</span><span class="sxs-lookup"><span data-stu-id="f1cc0-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="f1cc0-105">Вы можете получить строки триггера известного триггера, используя интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) или [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , в зависимости от типа объекта, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="f1cc0-106">При работе с [*объектом Task*](t.md)используйте методы интерфейса [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) для получения строк триггера рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="f1cc0-107">При работе с [*объектом триггера задачи*](t.md)используйте методы интерфейса [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , чтобы получить строку триггера триггера.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="f1cc0-108">В следующем примере показано, как использовать [**исчедуледворкитем:: жеттригжерстринг**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) для отображения строк всех триггеров, связанных с известной задачей.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="f1cc0-109">В следующей процедуре описывается получение строк триггера задачи.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="f1cc0-110">**Получение строк триггера задачи**</span><span class="sxs-lookup"><span data-stu-id="f1cc0-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="f1cc0-111">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="f1cc0-112">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="f1cc0-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="f1cc0-113">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="f1cc0-114">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="f1cc0-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="f1cc0-115">Вызовите метод **ITask:: жеттригжеркаунт** , чтобы узнать, сколько триггеров связано с задачей.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="f1cc0-116">(Обратите внимание, что [**жеттригжеркаунт**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="f1cc0-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="f1cc0-117">Отобразить строки триггера, вызвав **ITask:: жеттригжерстринг** для каждого триггера, связанного с задачей.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="f1cc0-118">(Обратите внимание, что [**жеттригжерстринг**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="f1cc0-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="f1cc0-119">Освободите все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-119">Release all resources.</span></span> <span data-ttu-id="f1cc0-120">Вызовите [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить строки триггера и **ITask:: Release** , чтобы освободить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="f1cc0-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="f1cc0-121">(Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="f1cc0-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="f1cc0-122">Пример кода</span><span class="sxs-lookup"><span data-stu-id="f1cc0-122">For a code example of</span></span>                                                         | <span data-ttu-id="f1cc0-123">См.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1cc0-124">Получение строки триггера для всех триггеров, связанных с известной задачей</span><span class="sxs-lookup"><span data-stu-id="f1cc0-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="f1cc0-125">Пример кода. Получение строк триггера</span><span class="sxs-lookup"><span data-stu-id="f1cc0-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="f1cc0-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f1cc0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1cc0-127">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="f1cc0-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 