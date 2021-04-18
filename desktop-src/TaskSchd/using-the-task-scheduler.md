---
title: Использование планировщик задач
description: В этом разделе содержатся примеры кода, иллюстрирующие использование планировщик задач API и примеры XML, демонстрирующие определение задач в схеме планировщик задач.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- триггеры планировщик задач, примеры
- Запуск задачи планировщик задач
- Создание задач планировщик задач
- планировщик задач планировщик задач с помощью
- планировщик задач примеры планировщик задач
- Планировщик задач планировщик задач, примеры см. в планировщик задач примерах планировщик задач
- Примеры планировщик задач см. в планировщик задач примерах планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672001"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="d7ab9-110">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="d7ab9-110">Using the Task Scheduler</span></span>

<span data-ttu-id="d7ab9-111">В этом разделе содержатся примеры кода, иллюстрирующие использование планировщик задач API и примеры XML, демонстрирующие определение задач в схеме планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="d7ab9-112">Большинство из этих примеров представляют собой изолированный код, который может быть запущен независимо или вставлен в более крупное приложение и изменен в зависимости от требований приложения.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="d7ab9-113">В следующей таблице приведены примеры планировщик задач 2,0, которые приведены в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="d7ab9-114">Пример</span><span class="sxs-lookup"><span data-stu-id="d7ab9-114">Example</span></span>                                                                                                    | <span data-ttu-id="d7ab9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d7ab9-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7ab9-116">Запуск исполняемого файла в определенное время</span><span class="sxs-lookup"><span data-stu-id="d7ab9-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="d7ab9-117">Определяет задачу, которая запускает Блокнот в указанное время.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="d7ab9-118">Запуск исполняемого файла ежедневно</span><span class="sxs-lookup"><span data-stu-id="d7ab9-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="d7ab9-119">Определяет задачу, которая ежедневно запускает Блокнот.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="d7ab9-120">Запуск исполняемого файла при загрузке системы</span><span class="sxs-lookup"><span data-stu-id="d7ab9-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="d7ab9-121">Определяет задачу, которая запускает программу «Блокнот» при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="d7ab9-122">Запуск исполняемого файла еженедельно</span><span class="sxs-lookup"><span data-stu-id="d7ab9-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="d7ab9-123">Определяет задачу, которая запускается в блокноте еженедельно.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="d7ab9-124">Запуск исполняемого файла при регистрации задачи</span><span class="sxs-lookup"><span data-stu-id="d7ab9-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="d7ab9-125">Определяет задачу, которая запускает программу «Блокнот» при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="d7ab9-126">Запуск исполняемого файла при входе пользователя в систему</span><span class="sxs-lookup"><span data-stu-id="d7ab9-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="d7ab9-127">Определяет задачу, запускающую Блокнот при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="d7ab9-128">Перечисление задач и отображение сведений о задачах</span><span class="sxs-lookup"><span data-stu-id="d7ab9-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="d7ab9-129">Перечисление всех задач на локальном компьютере и отображение состояния каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="d7ab9-130">В следующей таблице приведены примеры планировщик задач 1,0, которые приведены в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="d7ab9-131">Пример</span><span class="sxs-lookup"><span data-stu-id="d7ab9-131">Example</span></span>                                                                                    | <span data-ttu-id="d7ab9-132">Описание</span><span class="sxs-lookup"><span data-stu-id="d7ab9-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7ab9-133">Создание задачи с помощью примера Невворкитем</span><span class="sxs-lookup"><span data-stu-id="d7ab9-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="d7ab9-134">Создает новую задачу.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="d7ab9-135">Пример перечисления задач</span><span class="sxs-lookup"><span data-stu-id="d7ab9-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="d7ab9-136">Перечисляет все задачи на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="d7ab9-137">Пример запуска задачи</span><span class="sxs-lookup"><span data-stu-id="d7ab9-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="d7ab9-138">Запускает известную задачу.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="d7ab9-139">Изменение рабочего элемента с помощью страниц свойств</span><span class="sxs-lookup"><span data-stu-id="d7ab9-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="d7ab9-140">Отображает страницы свойств задачи для редактирования.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="d7ab9-141">Получение примеров свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="d7ab9-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="d7ab9-142">Набор примеров, демонстрирующих получение свойств, которые применяются ко всем типам рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="d7ab9-143">Примеры настройки свойств рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="d7ab9-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="d7ab9-144">Набор примеров, демонстрирующих установку свойств, которые применяются ко всем типам рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="d7ab9-145">Получение примеров свойств задачи</span><span class="sxs-lookup"><span data-stu-id="d7ab9-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="d7ab9-146">Набор примеров, демонстрирующих получение свойств, уникальных для задач.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="d7ab9-147">Примеры свойств задач</span><span class="sxs-lookup"><span data-stu-id="d7ab9-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="d7ab9-148">Набор примеров, демонстрирующих задание свойств, уникальных для задач.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="d7ab9-149">Получение примера страницы задачи</span><span class="sxs-lookup"><span data-stu-id="d7ab9-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="d7ab9-150">Извлекает и отображает страницу «Общие задачи» для известной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="d7ab9-151">Создание нового триггера</span><span class="sxs-lookup"><span data-stu-id="d7ab9-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="d7ab9-152">Создает новый триггер для известной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="d7ab9-153">Пример создания триггера Idle</span><span class="sxs-lookup"><span data-stu-id="d7ab9-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="d7ab9-154">Создает триггер бездействия на основе событий для известной задачи.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="d7ab9-155">Пример завершения задачи</span><span class="sxs-lookup"><span data-stu-id="d7ab9-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="d7ab9-156">Завершает задачу во время ее выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="d7ab9-157">Пример получения строк триггера</span><span class="sxs-lookup"><span data-stu-id="d7ab9-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="d7ab9-158">Извлекает строку триггера всех триггеров, связанных с известной задачей.</span><span class="sxs-lookup"><span data-stu-id="d7ab9-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="d7ab9-159">См. также</span><span class="sxs-lookup"><span data-stu-id="d7ab9-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ab9-160">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d7ab9-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d7ab9-161">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="d7ab9-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




