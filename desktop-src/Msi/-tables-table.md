---
description: Таблица Tables \_ является системной таблицей только для чтения, в которой перечислены все таблицы в базе данных. Запросите эту таблицу, чтобы узнать, существует ли таблица.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Таблица _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909163"
---
# <a name="_tables-table"></a>\_Таблица таблиц

Таблица Tables \_ является системной таблицей только для чтения, в которой перечислены все таблицы в базе данных. Запросите эту таблицу, чтобы узнать, существует ли таблица.

Таблица Tables \_ содержит следующий столбец.



| Столбец | Type             | Ключ | Допускает значения NULL |
|--------|------------------|-----|----------|
| Имя   | [Text](text.md) | Да   | Нет        |



 

## <a name="column"></a>Столбец

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян
</dt> <dd>

Имя одной из таблиц.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Поскольку \_ Таблица таблиц является системной таблицей, которая не может быть изменена с помощью SQL-запросов, вы не можете получить первичные ключи с помощью функции [**мсидатабасежетпримарикэйс**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) или [**Свойства примарикэйс**](database-primarykeys.md).

 

 



