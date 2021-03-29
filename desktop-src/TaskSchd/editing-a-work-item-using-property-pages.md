---
title: Изменение рабочего элемента с помощью страниц свойств
description: Свойства рабочего элемента можно изменить с помощью графического пользовательского интерфейса, предоставленного службой планировщик задач.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- изменение рабочих элементов планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792139"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="c6286-104">Изменение рабочего элемента с помощью страниц свойств</span><span class="sxs-lookup"><span data-stu-id="c6286-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="c6286-105">Свойства рабочего элемента можно изменить с помощью графического пользовательского интерфейса, предоставленного службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c6286-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="c6286-106">(В настоящее время единственными допустимыми рабочими элементами являются задачи.)</span><span class="sxs-lookup"><span data-stu-id="c6286-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="c6286-107">В следующей процедуре описывается изменение задачи с помощью страниц ее свойств.</span><span class="sxs-lookup"><span data-stu-id="c6286-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="c6286-108">**Изменение задачи с помощью страниц свойств**</span><span class="sxs-lookup"><span data-stu-id="c6286-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="c6286-109">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="c6286-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="c6286-110">(В этих примерах предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="c6286-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="c6286-111">Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task.</span><span class="sxs-lookup"><span data-stu-id="c6286-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="c6286-112">(Обратите внимание, что в настоящее время задачи являются единственным допустимым типом рабочего элемента.)</span><span class="sxs-lookup"><span data-stu-id="c6286-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="c6286-113">Вызовите метод [**исчедуледворкитем:: едитворкитем**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) , чтобы отобразить страницы свойств для задачи.</span><span class="sxs-lookup"><span data-stu-id="c6286-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="c6286-114">При необходимости измените свойства задачи, а затем нажмите кнопку ОК, чтобы принять новые значения и удалить отображаемые страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="c6286-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="c6286-115">Пример кода</span><span class="sxs-lookup"><span data-stu-id="c6286-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="c6286-116">См.</span><span class="sxs-lookup"><span data-stu-id="c6286-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6286-117">Отображение страниц свойств для известной задачи и предоставление пользователю возможности изменения свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="c6286-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="c6286-118">Пример кода C/C++: изменение рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="c6286-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="c6286-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c6286-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6286-120">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="c6286-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 