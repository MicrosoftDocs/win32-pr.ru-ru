---
description: Добавьте запись в таблицу CustomAction для настраиваемого действия запустить.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Добавление запуска в таблицы CustomAction и binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145967"
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

 

 



