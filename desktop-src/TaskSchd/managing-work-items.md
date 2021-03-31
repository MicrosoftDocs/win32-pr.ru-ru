---
title: Работа с рабочими элементами
description: Интерфейс Исчедуледворкитем предоставляет методы для извлечения и установки свойств рабочих элементов. Создание, извлечение и удаление триггеров для рабочих элементов (Настройка триггера должна выполняться с помощью метода Сеттригжер Итасктригжер); и для запуска, завершения и удаления рабочего элемента. Примечание. свойства определенного типа рабочего элемента см. в интерфейсе для этого типа объекта. Например, нельзя задать уровень приоритета рабочего элемента. Однако для получения и задания приоритета задачи можно использовать методы интерфейса ITask.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- рабочие элементы планировщик задач, управление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792559"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="9fd59-105">Работа с рабочими элементами</span><span class="sxs-lookup"><span data-stu-id="9fd59-105">Manipulating Work Items</span></span>

<span data-ttu-id="9fd59-106">Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) предоставляет методы для извлечения и установки свойств рабочих элементов. Создание, извлечение и удаление триггеров для рабочих элементов (Настройка триггера должна выполняться с помощью метода [**итасктригжер:: сеттригжер**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); и для запуска, завершения и удаления рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="9fd59-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="9fd59-107">Сведения о свойствах определенного типа рабочего элемента см. в интерфейсе для этого типа объекта.</span><span class="sxs-lookup"><span data-stu-id="9fd59-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="9fd59-108">Например, нельзя задать уровень приоритета рабочего элемента. Однако для получения и задания приоритета задачи можно использовать методы интерфейса [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="9fd59-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="9fd59-109">При каждом изменении рабочего элемента необходимо вызвать объект [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить измененный рабочий элемент на диск.</span><span class="sxs-lookup"><span data-stu-id="9fd59-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="9fd59-110">Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .</span><span class="sxs-lookup"><span data-stu-id="9fd59-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="9fd59-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="9fd59-111">For examples of</span></span>                                                            | <span data-ttu-id="9fd59-112">См.</span><span class="sxs-lookup"><span data-stu-id="9fd59-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd59-113">Получение свойств, относящихся ко всем типам рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="9fd59-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="9fd59-114">Получение примеров свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="9fd59-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="9fd59-115">Задание свойств, которые применяются ко всем типам рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="9fd59-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="9fd59-116">Примеры настройки свойств рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="9fd59-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="9fd59-117">Выполнение известной задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-117">Running a known task</span></span>                                                       | [<span data-ttu-id="9fd59-118">Пример запуска задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="9fd59-119">Завершение выполняющейся задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="9fd59-120">Пример завершения задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="9fd59-121">Создание нового триггера для известной задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="9fd59-122">Создание нового триггера</span><span class="sxs-lookup"><span data-stu-id="9fd59-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="9fd59-123">Создание триггера бездействия на основе событий для известной задачи</span><span class="sxs-lookup"><span data-stu-id="9fd59-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="9fd59-124">Пример создания триггера Idle</span><span class="sxs-lookup"><span data-stu-id="9fd59-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="9fd59-125">Получение строки триггера всех триггеров, связанных с известной задачей</span><span class="sxs-lookup"><span data-stu-id="9fd59-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="9fd59-126">Пример получения строк триггера</span><span class="sxs-lookup"><span data-stu-id="9fd59-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 