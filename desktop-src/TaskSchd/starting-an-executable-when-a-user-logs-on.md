---
title: Запуск исполняемого файла при входе пользователя в систему
description: Создание задачи, запускающей исполняемый файл при входе пользователя в систему, путем определения триггера входа и исполняемого действия.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Планировщик задач примеры планировщик задач, триггер входа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410593"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a><span data-ttu-id="828c5-104">Запуск исполняемого файла при входе пользователя в систему</span><span class="sxs-lookup"><span data-stu-id="828c5-104">Starting an Executable When a User Logs On</span></span>

<span data-ttu-id="828c5-105">Создание задачи, запускающей исполняемый файл при входе пользователя в систему, путем определения триггера входа и исполняемого действия.</span><span class="sxs-lookup"><span data-stu-id="828c5-105">Writing a task that starts an executable when a user logs on is done by defining a logon trigger and an executable action.</span></span>

## <a name="logon-trigger"></a><span data-ttu-id="828c5-106">Триггер входа</span><span class="sxs-lookup"><span data-stu-id="828c5-106">Logon Trigger</span></span>

<span data-ttu-id="828c5-107">Триггеры входа активируются их начальной границей, но не запускают исполняемый файл до тех пор, пока указанный пользователь не войдет в систему.</span><span class="sxs-lookup"><span data-stu-id="828c5-107">Logon triggers are activated by their start boundary but they do not start the executable until a specified user logs on.</span></span> <span data-ttu-id="828c5-108">Можно указать триггер входа, который будет запускаться при входе определенного пользователя в систему, указав пользователя в свойстве [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) интерфейса [**илогонтригжер**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**логонтригжер**](logontrigger.md) для сценариев).</span><span class="sxs-lookup"><span data-stu-id="828c5-108">You can specify the logon trigger to start when a certain user logs on by specifying the user in the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property of the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface ([**LogonTrigger**](logontrigger.md) for scripting).</span></span>

## <a name="logontrigger-examples"></a><span data-ttu-id="828c5-109">Примеры Логонтригжер</span><span class="sxs-lookup"><span data-stu-id="828c5-109">LogonTrigger Examples</span></span>

<span data-ttu-id="828c5-110">В следующих примерах запускается блокнот после входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="828c5-110">The following examples start Notepad after a user logs on.</span></span>

-   [<span data-ttu-id="828c5-111">Пример триггера LOGON (скрипт)</span><span class="sxs-lookup"><span data-stu-id="828c5-111">Logon Trigger Example (Scripting)</span></span>](logon-trigger-example--scripting-.md)
-   [<span data-ttu-id="828c5-112">Пример триггера LOGON (C++)</span><span class="sxs-lookup"><span data-stu-id="828c5-112">Logon Trigger Example (C++)</span></span>](logon-trigger-example--c---.md)
-   [<span data-ttu-id="828c5-113">Пример триггера LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="828c5-113">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="828c5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="828c5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="828c5-115">Использование планировщик задач</span><span class="sxs-lookup"><span data-stu-id="828c5-115">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




