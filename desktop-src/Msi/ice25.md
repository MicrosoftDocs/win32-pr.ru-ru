---
description: ICE25 проверяет, удовлетворяет ли MSI-файл всем внутренним зависимостям модуля слияния и исключениям.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910912"
---
# <a name="ice25"></a>ICE25

ICE25 проверяет, удовлетворяет ли MSI-файл всем внутренним зависимостям [модуля слияния](merge-modules.md) и исключениям. ICE проверяет следующее:

-   Все зависимости модуля слияния, указанные в [таблице модуледепенденци](moduledependency-table.md) файла. msi, удовлетворяются по крайней мере в одном модуле слияния, указанном в [таблице ModuleSignature](modulesignature-table.md).
-   Что ни один из исключенных модулей слияния в [таблице модуликсклусион](moduleexclusion-table.md) несовместим с модулями слияния, перечисленными в [таблице ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Результат

ICE25 отправляет сообщение об ошибке, если MSI-файл ранее был объединен с несовместимым модулем слияния или если он не был объединен с необходимым модулем слияния.

## <a name="example"></a>Пример

ICE25 отправляет следующие ошибки для показанного примера.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[Таблица ModuleSignature](modulesignature-table.md)



| ModuleID | Язык | Версия |
|----------|----------|---------|
| Модуль а  | 0        | 1.0     |
| модулеб  | 1033     | 1.0     |



 

[Таблица Модуледепенденци](moduledependency-table.md)



| ModuleID | модулелангуаже | рекуиредид | рекуиредлангуаже | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Модуль а  | 0              | модулекс    | 0                | 2.0             |



 

[Таблица Модуликсклусион](moduleexclusion-table.md)



| ModuleID | модулелангуаже | ексклудедид | ексклудедлангуаже | ексклудедминверсион | ексклудедмаксверсион |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Модуль а  | 0              | модулеб    | 1033             |                    |                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



