---
title: Создание задачи с помощью примера Невворкитем
description: При создании задачи вы будете использовать два интерфейса планировщик задач Итасксчедулер и ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- создание рабочих элементов планировщик задач
- планировщик задач рабочих элементов, создание задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338388"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="de375-105">Создание задачи с помощью примера Невворкитем</span><span class="sxs-lookup"><span data-stu-id="de375-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="de375-106">При создании задачи вы будете использовать два интерфейса планировщик задач: [**итасксчедулер**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) и [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="de375-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="de375-107">Необходимо указать уникальное имя для задачи, идентификатор класса для объекта задачи и идентификатор интерфейса **ITask**.</span><span class="sxs-lookup"><span data-stu-id="de375-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="de375-108">Идентификатор класса и идентификатор интерфейса показаны в примере кода, приведенном в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="de375-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="de375-109">Вы также можете создать задачу, вызвав [**итасксчедулер:: аддворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span><span class="sxs-lookup"><span data-stu-id="de375-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="de375-110">При использовании этого маршрута вы обязаны создавать экземпляр объекта **Task** (который поддерживает интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ), а затем добавлять задачу с предоставленным именем.</span><span class="sxs-lookup"><span data-stu-id="de375-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="de375-111">По умолчанию только члены группы «Администраторы», «операторы архива» или «операторы сервера» могут создавать задачи в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="de375-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="de375-112">Член группы "Администраторы" может изменить дескриптор безопасности \\ папки задач Windows, чтобы разрешить другим пользователям создавать задачи.</span><span class="sxs-lookup"><span data-stu-id="de375-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="de375-113">Имя, указываемое для задачи, должно быть уникальным в папке запланированных задач.</span><span class="sxs-lookup"><span data-stu-id="de375-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="de375-114">Если задача с таким именем уже существует, [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ВОЗВРАЩАЕТ \_ файл ошибки \_ .</span><span class="sxs-lookup"><span data-stu-id="de375-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="de375-115">При получении этого возвращаемого значения следует указать другое имя и попытаться создать задачу еще раз.</span><span class="sxs-lookup"><span data-stu-id="de375-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="de375-116">В следующей процедуре описывается создание новой задачи рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="de375-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="de375-117">**Создание новой задачи рабочего элемента**</span><span class="sxs-lookup"><span data-stu-id="de375-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="de375-118">Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="de375-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="de375-119">(В этом примере предполагается, что служба планировщик задач запущена).</span><span class="sxs-lookup"><span data-stu-id="de375-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="de375-120">Вызовите [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) , чтобы создать новую задачу.</span><span class="sxs-lookup"><span data-stu-id="de375-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="de375-121">(Этот метод возвращает указатель на интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)</span><span class="sxs-lookup"><span data-stu-id="de375-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="de375-122">Сохраните новую задачу на диск, вызвав [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="de375-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="de375-123">(Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом **ITask** .)</span><span class="sxs-lookup"><span data-stu-id="de375-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="de375-124">Вызовите метод **ITask:: Release** , чтобы освободить все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="de375-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="de375-125">(Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span><span class="sxs-lookup"><span data-stu-id="de375-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="de375-126">Пример кода</span><span class="sxs-lookup"><span data-stu-id="de375-126">For a code example of</span></span>  | <span data-ttu-id="de375-127">См.</span><span class="sxs-lookup"><span data-stu-id="de375-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de375-128">Создание одной задачи</span><span class="sxs-lookup"><span data-stu-id="de375-128">Creating a single task</span></span> | [<span data-ttu-id="de375-129">Пример кода C/C++. Создание задачи с помощью Невворкитем</span><span class="sxs-lookup"><span data-stu-id="de375-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="de375-130">См. также</span><span class="sxs-lookup"><span data-stu-id="de375-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de375-131">Примеры планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="de375-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 