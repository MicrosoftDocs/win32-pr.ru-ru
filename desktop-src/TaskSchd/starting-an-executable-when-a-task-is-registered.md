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
# <a name="starting-an-executable-when-a-task-is-registered"></a>Запуск исполняемого файла при регистрации задачи

Создание задачи, запускающей исполняемый файл при регистрации задачи, осуществляется путем определения триггера регистрации и исполняемого действия.

## <a name="registration-trigger"></a>Триггер регистрации

Триггеры регистрации запускают задачу сразу после ее регистрации. Кроме того, можно указать задержку для триггера регистрации, которая запускает задачу по истечении определенного времени (задержки) после регистрации задачи. Задержка указывается в свойстве [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) интерфейса [**ирегистратионтригжер**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**регистратионтригжер**](registrationtrigger.md) для сценариев).

> [!Note]  
> При обновлении задачи с триггером регистрации задача будет выполнена после обновления.

 

## <a name="registration-trigger-examples"></a>Примеры триггеров регистрации

При регистрации задачи в следующих примерах запускается блокнот:

-   [Пример триггера регистрации (сценарии)](registration-trigger-example--scripting-.md)
-   [Пример триггера регистрации (C++)](registration-trigger-example--c---.md)
-   [Пример триггера регистрации (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




