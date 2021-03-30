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
# <a name="starting-an-executable-when-a-user-logs-on"></a>Запуск исполняемого файла при входе пользователя в систему

Создание задачи, запускающей исполняемый файл при входе пользователя в систему, путем определения триггера входа и исполняемого действия.

## <a name="logon-trigger"></a>Триггер входа

Триггеры входа активируются их начальной границей, но не запускают исполняемый файл до тех пор, пока указанный пользователь не войдет в систему. Можно указать триггер входа, который будет запускаться при входе определенного пользователя в систему, указав пользователя в свойстве [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) интерфейса [**илогонтригжер**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) ([**логонтригжер**](logontrigger.md) для сценариев).

## <a name="logontrigger-examples"></a>Примеры Логонтригжер

В следующих примерах запускается блокнот после входа пользователя в систему.

-   [Пример триггера LOGON (скрипт)](logon-trigger-example--scripting-.md)
-   [Пример триггера LOGON (C++)](logon-trigger-example--c---.md)
-   [Пример триггера LOGON (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




