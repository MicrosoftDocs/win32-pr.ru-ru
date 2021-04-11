---
title: планировщик задач для разработчиков
description: Планировщик задач позволяет автоматически выполнять стандартные задачи на выбранном компьютере. Планировщик задач это достигается за счет мониторинга выбранных критериев (называемых триггерами) и выполнения задач при выполнении этих условий.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- планировщик задач для разработчиков
- планировщик задач для разработки
- Разработка с помощью планировщик задач
- Планировщик задач, страница портала
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/19/2019
ms.locfileid: "104133058"
---
# <a name="task-scheduler-for-developers"></a><span data-ttu-id="7d9d8-108">планировщик задач для разработчиков</span><span class="sxs-lookup"><span data-stu-id="7d9d8-108">Task Scheduler for developers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d9d8-109">Этот раздел и другие подразделы этого раздела предназначены для аудитории разработчика.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-109">This topic and the other topics in this section are for a developer audience.</span></span> <span data-ttu-id="7d9d8-110">Если вы хотите использовать компонент планировщик задач в вашей емкости в качестве администратора или специалиста по ИТ, см. [планировщик задач](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span><span class="sxs-lookup"><span data-stu-id="7d9d8-110">If you're wishing to use the the Task Scheduler component in your capacity as an administrator, or an IT Professional, then see [Task Scheduler](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).</span></span>

## <a name="about-the-task-scheduler"></a><span data-ttu-id="7d9d8-111">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7d9d8-111">About the Task Scheduler</span></span>

<span data-ttu-id="7d9d8-112">Планировщик задач позволяет автоматически выполнять стандартные задачи на выбранном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-112">The Task Scheduler enables you to automatically perform routine tasks on a chosen computer.</span></span> <span data-ttu-id="7d9d8-113">Планировщик задач это достигается за счет мониторинга выбранных критериев (называемых триггерами) и выполнения задач при выполнении этих условий.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-113">Task Scheduler does this by monitoring whatever criteria you choose (referred to as triggers) and then executing the tasks when those criteria are met.</span></span>

<span data-ttu-id="7d9d8-114">Планировщик задач можно использовать для выполнения таких задач, как запуск приложения, отправка сообщения электронной почты или отображение окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-114">You can use the Task Scheduler to execute tasks such as starting an application, sending an email message, or showing a message box.</span></span> <span data-ttu-id="7d9d8-115">Задачи могут быть запланированы на выполнение в ответ на эти события или триггеры.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-115">Tasks can be scheduled to execute in response to these events, or triggers.</span></span> 

- <span data-ttu-id="7d9d8-116">При возникновении определенного системного события.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-116">When a specific system event occurs.</span></span>
- <span data-ttu-id="7d9d8-117">В определенное время.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-117">At a specific time.</span></span>
- <span data-ttu-id="7d9d8-118">В определенное время ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-118">At a specific time on a daily schedule.</span></span>
- <span data-ttu-id="7d9d8-119">В определенное время по еженедельному расписанию.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-119">At a specific time on a weekly schedule.</span></span>
- <span data-ttu-id="7d9d8-120">В определенное время по месячному расписанию.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-120">At a specific time on a monthly schedule.</span></span>
- <span data-ttu-id="7d9d8-121">В определенное время для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-121">At a specific time on a monthly day-of-week schedule.</span></span>
- <span data-ttu-id="7d9d8-122">Когда компьютер переходит в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-122">When the computer enters an idle state.</span></span>
- <span data-ttu-id="7d9d8-123">При регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-123">When the task is registered.</span></span>
- <span data-ttu-id="7d9d8-124">При загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-124">When the system is booted.</span></span>
- <span data-ttu-id="7d9d8-125">При входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-125">When a user logs on.</span></span>
- <span data-ttu-id="7d9d8-126">При изменении состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-126">When a Terminal Server session changes state.</span></span>

## <a name="developers"></a><span data-ttu-id="7d9d8-127">Разработчики</span><span class="sxs-lookup"><span data-stu-id="7d9d8-127">Developers</span></span>

<span data-ttu-id="7d9d8-128">Планировщик задач предоставляет интерфейсы API в этих формах.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-128">The Task Scheduler provides APIs in these forms.</span></span>

- <span data-ttu-id="7d9d8-129">Планировщик задач 2,0: интерфейсы и объекты предоставляются для C++ и для разработки сценариев соответственно.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-129">Task Scheduler 2.0: interfaces and objects are provided for C++, and for scripting development, respectively.</span></span>
- <span data-ttu-id="7d9d8-130">Планировщик задач 1,0: интерфейсы предоставляются для разработки на C++.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-130">Task Scheduler 1.0: interfaces are provided for C++ development.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7d9d8-131">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="7d9d8-131">Run-time requirements</span></span>

<span data-ttu-id="7d9d8-132">Для планировщик задач требуются следующие операционные системы.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-132">The Task Scheduler requires the following operating systems.</span></span>

- <span data-ttu-id="7d9d8-133">Планировщик задач 2,0: для клиента требуется Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-133">Task Scheduler 2.0: Client requires Windows Vista, or above.</span></span> <span data-ttu-id="7d9d8-134">Для сервера требуется Windows Server 2008 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-134">Server requires Windows Server 2008, or above.</span></span>
- <span data-ttu-id="7d9d8-135">Планировщик задач 1,0: для клиента требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-135">Task Scheduler 1.0: Client requires Windows Vista, or Windows XP.</span></span> <span data-ttu-id="7d9d8-136">Для сервера требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-136">Server requires Windows Server 2008, or Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d9d8-137">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7d9d8-137">In this section</span></span>

| <span data-ttu-id="7d9d8-138">Раздел</span><span class="sxs-lookup"><span data-stu-id="7d9d8-138">Topic</span></span> | <span data-ttu-id="7d9d8-139">Описание</span><span class="sxs-lookup"><span data-stu-id="7d9d8-139">Description</span></span> |
|-|-|
| [<span data-ttu-id="7d9d8-140">Новые возможности планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7d9d8-140">What's new in Task Scheduler</span></span>](what-s-new-in-task-scheduler.md) | <span data-ttu-id="7d9d8-141">Сводка новых функциональных возможностей, появившихся в планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-141">Summary of new functionality introduced by the Task Scheduler.</span></span> |
| [<span data-ttu-id="7d9d8-142">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7d9d8-142">About the Task Scheduler</span></span>](about-the-task-scheduler.md) | <span data-ttu-id="7d9d8-143">Общие концептуальные сведения о планировщик задач API.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-143">General conceptual information about the Task Scheduler API.</span></span> |
| [<span data-ttu-id="7d9d8-144">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7d9d8-144">Using the Task Scheduler</span></span>](using-the-task-scheduler.md) | <span data-ttu-id="7d9d8-145">Примеры кода, демонстрирующие использование интерфейсов API планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-145">Code examples that show how to use the Task Scheduler APIs.</span></span> |
| [<span data-ttu-id="7d9d8-146">Справочник по планировщик задач</span><span class="sxs-lookup"><span data-stu-id="7d9d8-146">Task Scheduler reference</span></span>](task-scheduler-reference.md) | <span data-ttu-id="7d9d8-147">Подробные справочные сведения о планировщик задач интерфейсах API и схеме планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="7d9d8-147">Detailed reference information for Task Scheduler APIs and the Task Scheduler schema.</span></span> |