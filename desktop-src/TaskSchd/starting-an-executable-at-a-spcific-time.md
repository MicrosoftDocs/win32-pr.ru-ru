---
title: Запуск исполняемого файла в определенное время
description: Создание задачи, запускающей исполняемый файл в определенное время, выполняется путем определения триггера времени и исполняемого действия.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Планировщик задач примеры планировщик задач, триггер времени
- Планировщик задач примеры планировщик задач, запуск исполняемого файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888736"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="ff5c2-105">Запуск исполняемого файла в определенное время</span><span class="sxs-lookup"><span data-stu-id="ff5c2-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="ff5c2-106">Создание задачи, запускающей исполняемый файл в определенное время, выполняется путем определения триггера времени и исполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="ff5c2-107">Начальная граница</span><span class="sxs-lookup"><span data-stu-id="ff5c2-107">Start Boundary</span></span>

<span data-ttu-id="ff5c2-108">Важно отметить, что триггер времени отличается от других триггеров на основе времени в том, что он срабатывает, когда триггер активируется его начальной границей.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="ff5c2-109">Другие триггеры, основанные на времени, активируются их начальной границей, но они не начинают выполнять свои действия (в данном случае запуска исполняемого файла) до тех пор, пока не будет достигнута запланированная дата.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="ff5c2-110">Примеры триггеров времени</span><span class="sxs-lookup"><span data-stu-id="ff5c2-110">Time Trigger Examples</span></span>

<span data-ttu-id="ff5c2-111">В следующих примерах запускается блокнот через 30 секунд после активации задачи:</span><span class="sxs-lookup"><span data-stu-id="ff5c2-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="ff5c2-112">Пример триггера времени (C++)</span><span class="sxs-lookup"><span data-stu-id="ff5c2-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="ff5c2-113">Пример триггера времени (сценарии)</span><span class="sxs-lookup"><span data-stu-id="ff5c2-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="ff5c2-114">Пример триггера времени (XML)</span><span class="sxs-lookup"><span data-stu-id="ff5c2-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="ff5c2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ff5c2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff5c2-116">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="ff5c2-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




