---
title: Добавление рабочих элементов
description: Существует два способа добавления рабочих элементов в запланированный Тасксфолдер. В папке можно создать новый рабочий элемент или добавить в нее существующий рабочий элемент.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- планировщик задач рабочих элементов, добавление
- задачи планировщик задач, добавление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672107"
---
# <a name="adding-work-items"></a><span data-ttu-id="0fbec-106">Добавление рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="0fbec-106">Adding Work Items</span></span>

<span data-ttu-id="0fbec-107">Существует два способа добавления [*рабочих элементов*](w.md) в [*запланированный тасксфолдер*](s.md).</span><span class="sxs-lookup"><span data-stu-id="0fbec-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="0fbec-108">В папке можно создать новый рабочий элемент или добавить в нее существующий рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="0fbec-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="0fbec-109">Сейчас в папку "назначенные задания" можно добавлять только объекты задач.</span><span class="sxs-lookup"><span data-stu-id="0fbec-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="0fbec-110">При добавлении задачи необходимо иметь представление идентификаторы для класса Task и интерфейса задачи [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="0fbec-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="0fbec-111">Вы создаете новые рабочие элементы, вызывая метод [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) .</span><span class="sxs-lookup"><span data-stu-id="0fbec-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="0fbec-112">Этот метод создает новый объект рабочего элемента, используя предоставленное имя, и добавляет рабочий элемент в папку "назначенные задания".</span><span class="sxs-lookup"><span data-stu-id="0fbec-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="0fbec-113">При создании нового рабочего элемента планировщик задач выделяет память, необходимую для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="0fbec-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="0fbec-114">Чтобы добавить существующие рабочие элементы в папку "запланированные задания", вызовите метод [**итасксчедулер:: аддворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) .</span><span class="sxs-lookup"><span data-stu-id="0fbec-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="0fbec-115">При вызове этого метода необходимо создать объект.</span><span class="sxs-lookup"><span data-stu-id="0fbec-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="0fbec-116">Имена, указываемые для рабочих элементов, должны быть уникальными в папке запланированных задач.</span><span class="sxs-lookup"><span data-stu-id="0fbec-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="0fbec-117">Если рабочий элемент с таким именем уже существует при вызове метода [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) или метода [**Итасксчедулер:: аддворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , метод возвращает ошибку " **\_ файл \_ существует** ошибка".</span><span class="sxs-lookup"><span data-stu-id="0fbec-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="0fbec-118">Дополнительные сведения см. в разделе [Создание задачи с помощью примера невворкитем](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="0fbec-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




