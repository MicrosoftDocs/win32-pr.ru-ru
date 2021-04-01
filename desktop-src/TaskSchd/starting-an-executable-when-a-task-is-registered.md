---
title: Запуск исполняемого файла при регистрации задачи
description: Создание задачи, запускающей исполняемый файл при регистрации задачи, осуществляется путем определения триггера регистрации и исполняемого действия.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Планировщик задач примеры планировщик задач, триггер регистрации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986589"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="549ab-104">Запуск исполняемого файла при регистрации задачи</span><span class="sxs-lookup"><span data-stu-id="549ab-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="549ab-105">Создание задачи, запускающей исполняемый файл при регистрации задачи, осуществляется путем определения триггера регистрации и исполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="549ab-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="549ab-106">Триггер регистрации</span><span class="sxs-lookup"><span data-stu-id="549ab-106">Registration Trigger</span></span>

<span data-ttu-id="549ab-107">Триггеры регистрации запускают задачу сразу после ее регистрации.</span><span class="sxs-lookup"><span data-stu-id="549ab-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="549ab-108">Кроме того, можно указать задержку для триггера регистрации, которая запускает задачу по истечении определенного времени (задержки) после регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="549ab-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="549ab-109">Задержка указывается в свойстве [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) интерфейса [**ирегистратионтригжер**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**регистратионтригжер**](registrationtrigger.md) для сценариев).</span><span class="sxs-lookup"><span data-stu-id="549ab-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="549ab-110">При обновлении задачи с триггером регистрации задача будет выполнена после обновления.</span><span class="sxs-lookup"><span data-stu-id="549ab-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="549ab-111">Примеры триггеров регистрации</span><span class="sxs-lookup"><span data-stu-id="549ab-111">Registration Trigger Examples</span></span>

<span data-ttu-id="549ab-112">При регистрации задачи в следующих примерах запускается блокнот:</span><span class="sxs-lookup"><span data-stu-id="549ab-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="549ab-113">Пример триггера регистрации (сценарии)</span><span class="sxs-lookup"><span data-stu-id="549ab-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="549ab-114">Пример триггера регистрации (C++)</span><span class="sxs-lookup"><span data-stu-id="549ab-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="549ab-115">Пример триггера регистрации (XML)</span><span class="sxs-lookup"><span data-stu-id="549ab-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="549ab-116">См. также</span><span class="sxs-lookup"><span data-stu-id="549ab-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="549ab-117">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="549ab-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




