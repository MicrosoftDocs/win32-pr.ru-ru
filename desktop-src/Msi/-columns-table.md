---
description: '\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов. В нем перечислены столбцы для всех таблиц. Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.'
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Таблица _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cbb603c077d7873cdfbea88070e555902883ba579b422627b2581aca04745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640479"
---
# <a name="_columns-table"></a>\_Таблица Columns

\_Таблица Columns — это системная таблица только для чтения, содержащая каталог столбцов. В нем перечислены столбцы для всех таблиц. Можно выполнить запрос к этой таблице, чтобы выяснить, существует ли данный столбец.

\_Таблица Columns содержит следующие столбцы.



| Столбец | Type                   | Ключ | Допускает значения NULL |
|--------|------------------------|-----|----------|
| Таблица  | [Text](text.md)       | Д   | Нет        |
| Число | [Integer](integer.md) | Д   | Нет        |
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

## <a name="remarks"></a>Remarks

поскольку \_ таблица columns является системной таблицей, которая не может быть изменена с помощью запросов SQL, вы не можете получить первичные ключи с помощью функции [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) или [**свойства примарикэйс**](database-primarykeys.md).

В таблице Columns хранятся только постоянные столбцы \_ . Чтобы определить, существует ли временный столбец, необходимо создать представление с помощью инструкции SELECT для \* таблицы, а затем перебрать все поля в записи, возвращаемой функцией [**мсивиевжетколумнинфо**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) , с \_ параметром мсиколинфо Names.

 

 



