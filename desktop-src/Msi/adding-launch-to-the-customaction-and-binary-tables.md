---
description: Добавьте запись в таблицу CustomAction для настраиваемого действия запустить.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Добавление запуска в таблицы CustomAction и binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156351"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Добавление запуска в таблицы CustomAction и binary

Добавьте запись в [таблицу CustomAction](customaction-table.md) для настраиваемого действия запустить. Введите имя настраиваемого действия в столбце Действие таблицы CustomAction. Введите общий числовой тип для Launch, 65, в столбец Type пользовательской таблицы действий. Исходный столбец таблицы CustomAction задает ключ в записи [двоичной таблицы](binary-table.md) , содержащей двоичные данные для библиотеки DLL. Введите Tutorial.dll в столбец Source таблицы CustomAction. Точка входа, указанная в целевом поле таблицы CustomAction, должна совпадать со значением, экспортированным из библиотеки DLL. Введите Лаунчтуториал в столбец Target таблицы CustomAction.

[Таблица CustomAction](customaction-table.md)



| Действие | Тип | Источник       | Назначение         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | лаунчтуториал |



 

Добавьте Tutorial.dll, созданные из файла Tutorial. cpp, в двоичный поток в двоичную таблицу.

[Двоичная таблица](binary-table.md)



| Имя         | Данные                          |
|--------------|-------------------------------|
| Tutorial.dll | {*двоичные данные добавлены для библиотеки DLL*} |



 

Продолжайте [добавлять события элемента управления в конце установки для запуска запуска](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



