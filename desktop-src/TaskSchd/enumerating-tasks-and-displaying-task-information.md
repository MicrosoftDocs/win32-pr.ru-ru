---
title: Перечисление задач и отображение сведений о задачах
description: Отображение сведений о задаче, таких как имя задачи, состояние или время последнего запуска задачи, осуществляется путем перечисления выполняемых задач или задач в папке задач и отображения нужных сведений.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Перечисление задач планировщик задач
- Планировщик задач примеры планировщик задач, перечисление задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772815"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="09c66-105">Перечисление задач и отображение сведений о задачах</span><span class="sxs-lookup"><span data-stu-id="09c66-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="09c66-106">Отображение сведений о задаче, таких как имя задачи, состояние или время последнего запуска задачи, осуществляется путем перечисления выполняемых задач или задач в папке задач и отображения нужных сведений.</span><span class="sxs-lookup"><span data-stu-id="09c66-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="09c66-107">Доступ к свойствам зарегистрированных задач</span><span class="sxs-lookup"><span data-stu-id="09c66-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="09c66-108">Чтобы отобразить значение свойства зарегистрированной задачи, необходимо подключиться к службе планировщик задач, а затем получить экземпляр папки Task, содержащей задачи, сведения о которых вам нужны.</span><span class="sxs-lookup"><span data-stu-id="09c66-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="09c66-109">Затем вы получите коллекцию всех зарегистрированных задач в папке Task.</span><span class="sxs-lookup"><span data-stu-id="09c66-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="09c66-110">Затем выполняется перечисление всех зарегистрированных задач, а также получение и отображение значения свойства для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="09c66-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="09c66-111">Доступ к свойствам выполняемых задач</span><span class="sxs-lookup"><span data-stu-id="09c66-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="09c66-112">Чтобы отобразить значение свойства выполняющейся задачи, необходимо подключиться к службе планировщик задач, а затем получить коллекцию всех выполняемых задач (включая или исключить скрытые задачи).</span><span class="sxs-lookup"><span data-stu-id="09c66-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="09c66-113">Затем выполняется перечисление всех выполняемых задач и получение и отображение значения свойства для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="09c66-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="09c66-114">Пример</span><span class="sxs-lookup"><span data-stu-id="09c66-114">Example</span></span>

<span data-ttu-id="09c66-115">В следующих примерах перечисляются задачи и отображаются имя и состояние задач.</span><span class="sxs-lookup"><span data-stu-id="09c66-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="09c66-116">Отображение имен и состояний задач (написание сценариев)</span><span class="sxs-lookup"><span data-stu-id="09c66-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="09c66-117">Отображение имен и состояний задач (C++)</span><span class="sxs-lookup"><span data-stu-id="09c66-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="09c66-118">См. также</span><span class="sxs-lookup"><span data-stu-id="09c66-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c66-119">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="09c66-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




