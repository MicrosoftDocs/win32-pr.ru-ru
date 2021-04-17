---
title: Сведения о планировщик задач
description: Служба планировщик задач позволяет выполнять автоматизированные задачи на выбранном компьютере.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Планировщик задач планировщик задач, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681480"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="a96e9-104">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="a96e9-104">About the Task Scheduler</span></span>

<span data-ttu-id="a96e9-105">Служба планировщик задач позволяет выполнять автоматизированные задачи на выбранном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a96e9-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="a96e9-106">С помощью этой службы можно запланировать выполнение любой программы в удобное время или при возникновении определенного события.</span><span class="sxs-lookup"><span data-stu-id="a96e9-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="a96e9-107">Планировщик задач отслеживает выбранное время или критерии события, а затем выполняет задачу при соблюдении этих условий.</span><span class="sxs-lookup"><span data-stu-id="a96e9-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="a96e9-108">Где установлена планировщик задач</span><span class="sxs-lookup"><span data-stu-id="a96e9-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="a96e9-109">Планировщик задач устанавливается автоматически с несколькими операционными системами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a96e9-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="a96e9-110">Планировщик задач 1,0 устанавливается вместе с операционными системами Windows Server 2003, Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a96e9-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="a96e9-111">Планировщик задач 2,0 устанавливается вместе с Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a96e9-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="a96e9-112">Планировщик задач API 2,0 следует использовать при разработке приложений, использующих службу планировщик задач в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a96e9-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="a96e9-113">Дополнительные сведения см. в разделе [Справочник по планировщик задач](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a96e9-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="a96e9-114">Планировщик задач запускается каждый раз при запуске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a96e9-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="a96e9-115">Его можно запустить либо с помощью графического пользовательского интерфейса планировщик задач, либо с помощью API планировщик задач, описанного в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="a96e9-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="a96e9-116">Сведения о задачах</span><span class="sxs-lookup"><span data-stu-id="a96e9-116">Information about Tasks</span></span>

<span data-ttu-id="a96e9-117">Задачи являются основным компонентом планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="a96e9-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="a96e9-118">Сведения о задачах и их компонентах см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a96e9-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="a96e9-119">Задачи</span><span class="sxs-lookup"><span data-stu-id="a96e9-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="a96e9-120">Действия задач</span><span class="sxs-lookup"><span data-stu-id="a96e9-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="a96e9-121">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="a96e9-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="a96e9-122">Сведения о регистрации задачи</span><span class="sxs-lookup"><span data-stu-id="a96e9-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="a96e9-123">Условия простоя задачи</span><span class="sxs-lookup"><span data-stu-id="a96e9-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="a96e9-124">Контексты безопасности для задач</span><span class="sxs-lookup"><span data-stu-id="a96e9-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="a96e9-125">Повторение задачи</span><span class="sxs-lookup"><span data-stu-id="a96e9-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="a96e9-126">Автоматическое обслуживание</span><span class="sxs-lookup"><span data-stu-id="a96e9-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="a96e9-127">Дополнительные сведения и примеры использования интерфейсов планировщик задач, сценариев и XML см. [в разделе использование Планировщик задач](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="a96e9-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a96e9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a96e9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a96e9-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a96e9-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




