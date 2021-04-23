---
title: Запуск исполняемого файла при загрузке системы
description: Создание задачи, запускающей исполняемый файл при загрузке системы, осуществляется путем определения триггера загрузки и исполняемого действия.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Планировщик задач примеры планировщик задач, триггер загрузки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778113"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="667d3-104">Запуск исполняемого файла при загрузке системы</span><span class="sxs-lookup"><span data-stu-id="667d3-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="667d3-105">Создание задачи, запускающей исполняемый файл при загрузке системы, осуществляется путем определения триггера загрузки и исполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="667d3-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="667d3-106">Триггер загрузки</span><span class="sxs-lookup"><span data-stu-id="667d3-106">Boot Trigger</span></span>

<span data-ttu-id="667d3-107">Триггеры загрузки активируются их начальной границей, но не запускают исполняемый файл до загрузки системы.</span><span class="sxs-lookup"><span data-stu-id="667d3-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="667d3-108">Кроме того, можно указать время задержки в триггере загрузки, определяющее промежуток времени между загрузкой системы и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="667d3-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="667d3-109">Это определяется свойством [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) в интерфейсе [**Ибуттригжер**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (объект [**буттригжер**](boottrigger.md) для сценариев).</span><span class="sxs-lookup"><span data-stu-id="667d3-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="667d3-110">Примеры триггеров загрузки</span><span class="sxs-lookup"><span data-stu-id="667d3-110">Boot Trigger Examples</span></span>

<span data-ttu-id="667d3-111">Следующие примеры запускаются в блокноте после загрузки системы:</span><span class="sxs-lookup"><span data-stu-id="667d3-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="667d3-112">Пример триггера загрузки (написание сценариев)</span><span class="sxs-lookup"><span data-stu-id="667d3-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="667d3-113">Пример триггера Boot (C++)</span><span class="sxs-lookup"><span data-stu-id="667d3-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="667d3-114">Пример триггера Boot (XML)</span><span class="sxs-lookup"><span data-stu-id="667d3-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="667d3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="667d3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="667d3-116">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="667d3-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




