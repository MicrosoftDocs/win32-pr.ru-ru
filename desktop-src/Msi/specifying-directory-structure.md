---
description: Установщик сохраняет сведения о структуре каталогов установки в таблице Directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Указание структуры каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897677"
---
# <a name="specifying-directory-structure"></a>Указание структуры каталогов

Установщик сохраняет сведения о структуре каталогов установки в [таблице Directory](directory-table.md). См. раздел [группа основных таблиц](core-tables-group.md). В этом разделе вы добавите сведения о структуре каталогов для примера "Блокнот" в пустую базу данных, созданную при [импорте пустой базы данных](importing-a-blank-database.md). Используйте редактор базы данных Orca, поставляемый вместе с пакетом SDK, или другой редактор, чтобы открыть таблицу Directory в MNP2000.msi. Используйте редактор для ввода следующих данных в таблицу пустого каталога.

[Таблица каталога](directory-table.md)



| Каталог                                        | \_Родительский каталог                                | дефаултдир        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| артсдир                                          | нотепаддир                                       | Искусство: события       |
| холдир                                           | мондир                                           | .: Праздники        |
| менудир                                          | нотепаддир                                       | Меню              |
| мондир                                           | нотепаддир                                       | Frame              |
| нотепаддир                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Красный \_ парк: Блокнот |
| спортдир                                         | нотепаддир                                       | Спорт: события     |



 

Ввод этих данных в таблицу Directory задает структуры исходного и целевого каталогов. См. [таблицу Directory](directory-table.md) и разделы [таблицы каталогов](using-the-directory-table.md) . Обратите внимание, что свойство [**targetDir**](targetdir.md) должно быть именем одного корня в таблице Directory каждой установки.

[Продолжить](specifying-components.md)

 

 



