---
description: База данных установщика позволяет разработчику пакета установки управлять переносом приложения из источника в целевой образ.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Использование базы данных установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec91d8982a8ddac47c96303f03a33e4c85cafa70c3ef480c660df42e72f8a84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996064"
---
# <a name="using-the-installer-database"></a>Использование базы данных установщика

[База данных установщика](installer-database.md) позволяет разработчику пакета установки управлять переносом приложения из источника в целевой образ. Макет исходного и целевого образов приложения указывается в таблице [Directory](directory-table.md) , а действия, которые устанавливают приложение, указываются в шести таблицах последовательностей:

-   Таблица [инсталлуисекуенце](installuisequence-table.md)
-   Таблица [инсталлексекутесекуенце](installexecutesequence-table.md)
-   Таблица [админуисекуенце](adminuisequence-table.md)
-   Таблица [админексекутесекуенце](adminexecutesequence-table.md)
-   Таблица [адвтуисекуенце](advtuisequence-table.md)
-   Таблица [адвтексекутесекуенце](advtexecutesequence-table.md)

В следующих разделах описывается использование [базы данных установщика](installer-database.md).

-   [Использование таблицы Directory](using-the-directory-table.md)
-   [Использование таблицы последовательностей](using-a-sequence-table.md)
-   [Получение маркера базы данных](obtaining-a-database-handle.md)
-   [Фиксация баз данных](committing-databases.md)
-   [Импортирование и экспортирование](importing-and-exporting.md)
-   [Слияние баз данных](merging-databases.md)
-   [Именование настраиваемых таблиц, свойств и действий](naming-custom-tables-properties-and-actions.md)
-   [ограничения OLE на Потоки](ole-limitations-on-streams.md)
-   [Работа с запросами](working-with-queries.md)
-   [Добавление двоичных данных в таблицу с помощью SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Работа с записями](working-with-records.md)
-   [Работа с расположениями папок](working-with-folder-locations.md)
-   [Указание порядка самостоятельной регистрации](specifying-the-order-of-self-registration.md)
-   [Действия по обработке условий, выполняемые во время удаления](conditioning-actions-to-run-during-removal.md)
-   [Вызов функций базы данных из программ](calling-database-functions-from-programs.md)
-   [Синтаксис условных операторов](conditional-statement-syntax.md)
-   [Формат определения столбца](column-definition-format.md)
-   [Определение того, является ли столбец первичным или внешним ключом](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



