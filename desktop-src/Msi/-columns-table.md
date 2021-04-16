---
description: '\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов. В нем перечислены столбцы для всех таблиц. Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.'
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Таблица _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662990"
---
# <a name="_columns-table"></a>\_Таблица Columns

\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов. В нем перечислены столбцы для всех таблиц. Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.

\_Таблица Columns содержит следующие столбцы.



| Столбец | Type                   | Ключ | Допускает значения NULL |
|--------|------------------------|-----|----------|
| Таблица  | [Text](text.md)       | Да   | Нет        |
| Число | [Integer](integer.md) | Да   | Нет        |
| Имя   | [Text](text.md)       | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Таблица
</dt> <dd>

Имя таблицы, содержащей столбец.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Нумерация
</dt> <dd>

Порядок столбцов в таблице.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян
</dt> <dd>

Имя столбца.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Поскольку \_ Таблица Columns является системной таблицей, которая не может быть изменена с помощью SQL-запросов, вы не можете получить первичные ключи с помощью функции [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) или [**Свойства примарикэйс**](database-primarykeys.md).

В таблице Columns хранятся только постоянные столбцы \_ . Чтобы определить, существует ли временный столбец, необходимо создать представление с помощью инструкции SELECT для \* таблицы, а затем перебрать все поля в записи, возвращаемой функцией [**мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) , с \_ параметром мсиколинфо Names.

 

 



