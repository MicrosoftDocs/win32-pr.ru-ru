---
description: ICE25 проверяет, соответствует ли файл .msi всем внутренним зависимостям модуля слияния и исключениям.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2715ce629ad22b872b8d38d0c6848236b9f1af9378a0a652b702e7b72cbd7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528954"
---
# <a name="ice25"></a>ICE25

ICE25 проверяет, соответствует ли файл .msi всем внутренним зависимостям [модуля слияния](merge-modules.md) и исключениям. ICE проверяет следующее:

-   Все зависимости модуля слияния, указанные в [таблице модуледепенденци](moduledependency-table.md) файла .msi, удовлетворяются по крайней мере одним модулем слияния, указанным в [таблице ModuleSignature](modulesignature-table.md).
-   Что ни один из исключенных модулей слияния в [таблице модуликсклусион](moduleexclusion-table.md) несовместим с модулями слияния, перечисленными в [таблице ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Результат

ICE25 отправляет сообщение об ошибке, если .msi файл ранее был объединен с несовместимым модулем слияния или если он не был объединен с необходимым модулем слияния.

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



