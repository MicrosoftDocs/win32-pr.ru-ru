---
title: Пример завершения задачи
description: Задачу можно завершить во время ее выполнения, вызвав Исчедуледворкитем Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260956"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="265a6-103">Пример завершения задачи</span><span class="sxs-lookup"><span data-stu-id="265a6-103">Terminating a Task Example</span></span>

<span data-ttu-id="265a6-104">Задачу можно завершить во время ее выполнения, вызвав метод [**исчедуледворкитем:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span><span class="sxs-lookup"><span data-stu-id="265a6-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="265a6-105">Следующая процедура описывает, как завершить задачу, если она запущена.</span><span class="sxs-lookup"><span data-stu-id="265a6-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="265a6-106">**Завершение задачи, если она запущена**</span><span class="sxs-lookup"><span data-stu-id="265a6-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="265a6-107">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="265a6-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="265a6-108">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="265a6-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="265a6-109">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="265a6-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="265a6-110">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="265a6-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="265a6-111">Вызовите **ITask::-Status** , чтобы определить, запущена ли задача.</span><span class="sxs-lookup"><span data-stu-id="265a6-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="265a6-112">(Обратите [**внимание, что параметром**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) является метод, наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="265a6-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="265a6-113">Проверьте состояние задачи, а затем вызовите **ITask:: Terminate** , если задача запущена.</span><span class="sxs-lookup"><span data-stu-id="265a6-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="265a6-114">(Обратите внимание, что [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="265a6-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="265a6-115">Пример кода</span><span class="sxs-lookup"><span data-stu-id="265a6-115">For a code example of</span></span>                | <span data-ttu-id="265a6-116">См.</span><span class="sxs-lookup"><span data-stu-id="265a6-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="265a6-117">Проверка состояния известной задачи</span><span class="sxs-lookup"><span data-stu-id="265a6-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="265a6-118">Пример кода C/C++: завершение задачи</span><span class="sxs-lookup"><span data-stu-id="265a6-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="265a6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="265a6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265a6-120">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="265a6-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 