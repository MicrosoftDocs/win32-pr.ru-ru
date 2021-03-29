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
# <a name="starting-an-executable-on-system-boot"></a>Запуск исполняемого файла при загрузке системы

Создание задачи, запускающей исполняемый файл при загрузке системы, осуществляется путем определения триггера загрузки и исполняемого действия.

## <a name="boot-trigger"></a>Триггер загрузки

Триггеры загрузки активируются их начальной границей, но не запускают исполняемый файл до загрузки системы. Кроме того, можно указать время задержки в триггере загрузки, определяющее промежуток времени между загрузкой системы и началом задачи. Это определяется свойством [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) в интерфейсе [**Ибуттригжер**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (объект [**буттригжер**](boottrigger.md) для сценариев).

## <a name="boot-trigger-examples"></a>Примеры триггеров загрузки

Следующие примеры запускаются в блокноте после загрузки системы:

-   [Пример триггера загрузки (написание сценариев)](boot-trigger-example--scripting-.md)
-   [Пример триггера Boot (C++)](boot-trigger-example--c---.md)
-   [Пример триггера Boot (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование планировщик задач](using-the-task-scheduler.md)
</dt> </dl>

 

 




