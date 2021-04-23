---
title: Пример запуска задачи
description: Чтобы запустить задачу, вызовите метод Run интерфейса ITask. Запуск — это асинхронный метод, который пытается выполнить задачу и возвращает значение сразу после запуска задачи. Для выполнения этого метода должна быть запущена служба планировщик задач.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681685"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="9db22-105">Пример запуска задачи</span><span class="sxs-lookup"><span data-stu-id="9db22-105">Starting a Task Example</span></span>

<span data-ttu-id="9db22-106">Чтобы запустить задачу, вызовите метод [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) интерфейса [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="9db22-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="9db22-107">**Запуск** — это асинхронный метод, который пытается выполнить задачу и возвращает значение сразу после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="9db22-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="9db22-108">Для выполнения этого метода должна быть запущена служба планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9db22-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="9db22-109">В следующей процедуре описывается, как запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="9db22-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="9db22-110">**Запуск задачи**</span><span class="sxs-lookup"><span data-stu-id="9db22-110">**To start a task**</span></span>

1.  <span data-ttu-id="9db22-111">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9db22-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="9db22-112">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="9db22-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="9db22-113">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="9db22-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="9db22-114">(Обратите внимание, что в этом примере возвращается задача "задача тестирования".)</span><span class="sxs-lookup"><span data-stu-id="9db22-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="9db22-115">[**Выполните**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) вызов, чтобы запустить задачу.</span><span class="sxs-lookup"><span data-stu-id="9db22-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="9db22-116">Обратите внимание, что этот метод наследуется интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="9db22-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="9db22-117">Продолжайте обработку по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9db22-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="9db22-118">Вызовите метод **ITask:: Release** для освобождения ресурсов и [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , чтобы отменить инициализацию COM.</span><span class="sxs-lookup"><span data-stu-id="9db22-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="9db22-119">В этом примере вызывается [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для освобождения указателя на интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="9db22-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="9db22-120">(Обратите внимание, что **выпуск** — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый **ITask**.)</span><span class="sxs-lookup"><span data-stu-id="9db22-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="9db22-121">Пример кода</span><span class="sxs-lookup"><span data-stu-id="9db22-121">For a code example of</span></span>    | <span data-ttu-id="9db22-122">См.</span><span class="sxs-lookup"><span data-stu-id="9db22-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="9db22-123">Выполнение существующей задачи</span><span class="sxs-lookup"><span data-stu-id="9db22-123">Running an existing task</span></span> | [<span data-ttu-id="9db22-124">Пример кода C/C++: запуск задачи</span><span class="sxs-lookup"><span data-stu-id="9db22-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="9db22-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9db22-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db22-126">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="9db22-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 