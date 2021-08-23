---
description: Установщик сохраняет сведения о структуре каталогов установки в таблице Directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Указание структуры каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc71e448c03a7fdbdf9de249122246aaf0038769a1dd409551330a503be7e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627894"
---
# <a name="specifying-directory-structure"></a>Указание структуры каталогов

Установщик сохраняет сведения о структуре каталогов установки в [таблице Directory](directory-table.md). См. раздел [группа основных таблиц](core-tables-group.md). в этом разделе вы добавите сведения о структуре каталогов для образца Блокнот в пустую базу данных, созданную при [импорте пустой базы данных](importing-a-blank-database.md). Используйте редактор базы данных Orca, поставляемый вместе с пакетом SDK, или другой редактор, чтобы открыть таблицу Directory в MNP2000.msi. Используйте редактор для ввода следующих данных в таблицу пустого каталога.

[Таблица каталога](directory-table.md)



| Каталог                                        | \_Родительский каталог                                | дефаултдир        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| артсдир                                          | нотепаддир                                       | Искусство: события       |
| холдир                                           | мондир                                           | .: Праздники        |
| менудир                                          | нотепаддир                                       | Меню              |
| мондир                                           | нотепаддир                                       | Ворота              |
| нотепаддир                                       | [**ProgramFilesFolder**](programfilesfolder.md) | красный \_ парк: Блокнот |
| спортдир                                         | нотепаддир                                       | Спорт: события     |



 

Ввод этих данных в таблицу Directory задает структуры исходного и целевого каталогов. См. [таблицу Directory](directory-table.md) и разделы [таблицы каталогов](using-the-directory-table.md) . Обратите внимание, что свойство [**targetDir**](targetdir.md) должно быть именем одного корня в таблице Directory каждой установки.

[Продолжить](specifying-components.md)

 

 



