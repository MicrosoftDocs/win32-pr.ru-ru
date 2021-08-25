---
description: Предложение ORDER IN GROUP используется в сочетании с инструкцией GROUP ON, которая возвращает результирующие наборы в группах.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER в предложении GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944654"
---
# <a name="order-in-group-clause"></a>ORDER в предложении GROUP

Предложение ORDER IN GROUP используется в сочетании с инструкцией [Group on](-search-sql-group-on-over.md) , которая возвращает результирующие наборы в группах. Предложение ORDER IN GROUP позволяет сортировать каждую возвращаемую группу по-другому. Например, если вы выполняете группировку по System. Kind, можно сортировать все документы по System.Docумент. Ластаусор, все музыкальные файлы по System. Music. Албумартист и все сообщения электронной почты с помощью System. Message. Фромнаме.

## <a name="syntax"></a>Синтаксис

Ниже приведен синтаксис предложения ORDER IN GROUP:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



Описатель имени группы — это диапазон или известное значение из столбца Group, как указано в инструкции GROUP ON. Например, известные значения для System. photo. Исоспид будут содержать "ISO-100", "ISO-200" и т. д. Диапазон для System. photo. Датетакен будет включать "2006-1-1" и "2007-1-1" для инструкции, такой как GROUP ON System. Итемдате \[ ' 2006-1-1 ', ' 2007-1-1 ' \] .

Спецификатор столбца должен быть допустимым столбцом, указанным в инструкции GROUP ON или SELECT. Можно включить несколько столбцов, разделенных запятыми. Например, если вы выполняете группировку по System. photo. Исоспид, вы можете сортировать все фотографии ISO-100 сначала по System. photo. Шуттерспид, а затем по System. photo. апертуры.

Необязательный спецификатор направления может быть либо ASC для возрастания (от низкого до высокого), либо DESC для нисходящей (от высокого до низкого). Если не указать описатель направления, используется значение по умолчанию (по возрастанию). Если указать более одного столбца, но не указывать все направления, то направление, заданное последним, применяется к каждому последовательному столбцу до тех пор, пока не будет явно изменено направление.

Диапазоны или значения, которые явно не указаны в предложении GROUP ORDER, сортируются в возрастающем порядке по значениям в столбце GROUP ON.

## <a name="examples"></a>Примеры

В следующем примере результаты группируются по свойству System. Kind. Запрос упорядочивает группу "Program" по имени приложения и группе "Музыка" по названию альбома и номеру отслеживания. Группа **со значением NULL** будет упорядочена по имени элемента. Все остальные группы будут упорядочены по дате элемента.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



Следующий пример группирует результаты по свойству System. Итемдате, а затем сортирует каждую группу по URL-адресу элемента, виду или имени.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Результаты предыдущего запроса будут возвращены в пяти группах и отсортированы, как описано в следующей таблице.



| Группа    | Описание                                               | Отсортировано по                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MINVALUE | Элементы с датами до 2006-1-1                          | Сортировка по URL-адресу элемента в порядке возрастания |
| 2006-1-1 | Элементы с датами от 2006-1-1 до 2007-1-1 | Сортировка по дате элемента в возрастающем порядке      |
| 2007-1-1 | Элементы с датами от 2007-1-1 до 2008-1-1 | Сортировка по значению типа в возрастающем порядке     |
| 2008-1-1 | Элементы с датами в или после 2008-1-1                     | Сортировка по дате элемента в возрастающем порядке      |
| **NULL** | Элементы, не имеющие значения в столбце System. Итемдате         | Сортировка по имени элемента в возрастающем порядке      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[ГРУППИРОВАТЬ ПО... Поверх... Баланс](-search-sql-group-on-over.md)
</dt> <dt>

[Предложение ORDER BY](-search-sql-orderby.md)
</dt> </dl>

 

 



