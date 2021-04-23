---
title: Сведения о регистрации задачи
description: Регистрационные данные предоставляют способ определения задачи несколькими различными способами. Например, задача может быть идентифицирована автором, как она была создана (называется источником задачи) и датой регистрации.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- сведения о регистрации планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328307"
---
# <a name="task-registration-information"></a><span data-ttu-id="4dc6e-105">Сведения о регистрации задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-105">Task Registration Information</span></span>

<span data-ttu-id="4dc6e-106">Регистрационные данные предоставляют способ определения задачи несколькими различными способами.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="4dc6e-107">Например, задача может быть идентифицирована автором, как она была создана (называется источником задачи) и датой регистрации.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="4dc6e-108">Использование сведений о регистрации</span><span class="sxs-lookup"><span data-stu-id="4dc6e-108">Using Registration Information</span></span>

<span data-ttu-id="4dc6e-109">Сведения о регистрации обычно указываются при создании задачи, а затем используются следующими способами.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="4dc6e-110">Отображается в планировщик задач пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="4dc6e-111">Возвращает или задает приложения или скрипты C++.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="4dc6e-112">В корпоративной среде используется в качестве критерия поиска при перечислении всех зарегистрированных задач.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="4dc6e-113">Типы сведений о регистрации</span><span class="sxs-lookup"><span data-stu-id="4dc6e-113">Types of Registration Information</span></span>

<span data-ttu-id="4dc6e-114">Сведения о регистрации задач определяются свойствами объекта [**регистратионинфо**](registrationinfo.md) для сценариев приложений, свойствами интерфейса [**Ирегистратионинфо**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) для приложений C++ и дочерними элементами [**элемента регистратионинфо (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) для чтения или записи XML.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="4dc6e-115">Эти свойства предоставляют доступ к следующим типам сведений о регистрации:</span><span class="sxs-lookup"><span data-stu-id="4dc6e-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="4dc6e-116">Автор задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-116">Task Author</span></span>

    <span data-ttu-id="4dc6e-117">Планировщик задач задает автора задачи при ее создании.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="4dc6e-118">Дата регистрации задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-118">Task Registration Date</span></span>

    <span data-ttu-id="4dc6e-119">Планировщик задач задает эту дату при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="4dc6e-120">Описание задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-120">Task Description</span></span>

    <span data-ttu-id="4dc6e-121">Определяемое пользователем описание, которое может включать триггеры, используемые для запуска задачи, или действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="4dc6e-122">Документация по задачам</span><span class="sxs-lookup"><span data-stu-id="4dc6e-122">Task Documentation</span></span>

    <span data-ttu-id="4dc6e-123">Предоставленная пользователем документация, необходимая для задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="4dc6e-124">Дескриптор безопасности задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-124">Task Security Descriptor</span></span>

    <span data-ttu-id="4dc6e-125">Предоставляемый пользователем дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="4dc6e-126">Источник задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-126">Task Source</span></span>

    <span data-ttu-id="4dc6e-127">Предоставляемая пользователем информация, описывающая источник задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="4dc6e-128">Например, задача может исходить из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="4dc6e-129">URI задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-129">Task URI</span></span>

    <span data-ttu-id="4dc6e-130">Универсальный код ресурса (URI) для задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="4dc6e-131">Версия задачи</span><span class="sxs-lookup"><span data-stu-id="4dc6e-131">Task Version</span></span>

    <span data-ttu-id="4dc6e-132">Предоставляемые пользователем сведения, используемые при наличии нескольких версий задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="4dc6e-133">Текст XML</span><span class="sxs-lookup"><span data-stu-id="4dc6e-133">XML Text</span></span>

    <span data-ttu-id="4dc6e-134">Версия сведений о регистрации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="4dc6e-135">Обратите внимание, что вы можете задать или изменить сведения о регистрации напрямую с помощью этого XML, и соответствующие свойства объекта и интерфейса будут обновлены соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="4dc6e-136">Регистрация задач</span><span class="sxs-lookup"><span data-stu-id="4dc6e-136">Registering Tasks</span></span>

<span data-ttu-id="4dc6e-137">Задачу можно зарегистрировать после создания определений задач, а также получить сведения о регистрации и задать значения, предоставленные пользователем.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="4dc6e-138">Задача регистрируется с помощью метода [**таскфолдер. регистертаскдефинитион**](taskfolder-registertaskdefinition.md) для приложений скриптов или метода [**ITaskFolder:: Регистертаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) для приложений C++.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="4dc6e-139">Если вы хотите зарегистрировать задачу с помощью XML для определения задачи, используйте метод [**таскфолдер. регистертаск**](taskfolder-registertask.md) для приложений скриптов и метод [**ITaskFolder:: Регистертаск**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) для приложений C++.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="4dc6e-140">В указанных выше методах можно указать контекст безопасности для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="4dc6e-141">Чтобы запланировать выполнение заданий в контексте, отличном от собственного, необходимо быть администратором системы.</span><span class="sxs-lookup"><span data-stu-id="4dc6e-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="4dc6e-142">Дополнительные сведения о контекстах безопасности для выполнения задач см. в разделе [контексты безопасности для выполняющихся задач](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="4dc6e-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dc6e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="4dc6e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dc6e-144">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="4dc6e-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="4dc6e-145">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4dc6e-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




