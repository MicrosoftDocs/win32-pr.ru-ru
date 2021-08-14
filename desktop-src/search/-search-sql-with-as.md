---
description: Псевдонимы групп столбцов предоставляют способ использования более коротких имен вместо имени столбца или группы столбцов. Необязательный предикат псевдонима группы является частью предложения WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: С параметром--AS предикат псевдонима группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226737"
---
# <a name="with----as-group-alias-predicate"></a>С параметром--AS предикат псевдонима группы

Псевдонимы групп столбцов предоставляют способ использования более коротких имен вместо имени столбца или группы столбцов. Необязательный предикат псевдонима группы является частью предложения WHERE. Его синтаксис выглядит следующим образом:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Можно указать более одного псевдонима группы, разделяя на... Предикаты AS запятыми.

При ссылке на псевдоним группы в предикате предложения WHERE условие применяется к каждому столбцу в группе. Логические значения, полученные в результате сопоставления каждого столбца, объединяются с помощью логического оператора **или** .

Псевдоним должен быть определен до того, как его можно будет использовать, и его можно использовать только в предложении WHERE. Имя псевдонима должно быть обычным идентификатором, которому предшествует обязательный знак решетки ( \# ).

Описатель столбца может содержать один или несколько описателей столбцов, разделенных запятыми. Список столбцов должен быть заключен в круглые скобки, и для каждого из них можно назначить весовые значения. Каждый столбец имеет следующий синтаксис:


```
<column_identifier> [<weight_assignment>]
```



Сведения об указании веса столбцов см. в разделе [предикат FREETEXT](-search-sql-freetext.md) и [предикат CONTAINS](-search-sql-contains.md).

Идентификатор столбца может быть обычным или разделителем.

## <a name="examples"></a>Примеры

В следующих примерах предложения WHERE демонстрируется, когда и как можно использовать предикат псевдонима группы. В первом примере показано более повторяющееся предложение WHERE, которое не использует Псевдонимы групп.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



Предыдущий пример можно упростить с помощью псевдонима группы, как показано в следующем примере.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Ниже приведен пример положительного веса, в котором свойству **Title** присваивается больший вес при определении относительного ранга.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Ниже приведен пример отрицательного веса, при котором свойство **Title** с весом 0 не учитывается.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[Предикат FREETEXT](-search-sql-freetext.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Полнотекстовые предикаты](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Неполнотекстовые предикаты](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



