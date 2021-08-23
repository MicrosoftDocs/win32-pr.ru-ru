---
description: Таблица Одбкаттрибуте содержит сведения об атрибутах драйверов и переводчиков ODBC.
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Таблица Одбкаттрибуте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943182"
---
# <a name="odbcattribute-table"></a>Таблица Одбкаттрибуте

Таблица Одбкаттрибуте содержит сведения об атрибутах драйверов и переводчиков ODBC.

Таблица Одбкаттрибуте содержит следующие столбцы.



| Столбец    | Type                         | Ключ | Допускает значения NULL |
|-----------|------------------------------|-----|----------|
| Драйвер\_  | [Идентификатор](identifier.md) | Д   | Нет        |
| attribute | [Text](text.md)             | Д   | Нет        |
| Значение     | [Формате](formatted.md)   | Нет   | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Аудиодрайвера\_
</dt> <dd>

Имя внутреннего маркера для драйвера. Первичный ключ для таблицы. Внешний ключ в [таблице одбкдривер](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию
</dt> <dd>

Имя атрибута драйвера. Первичный ключ для таблицы.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений
</dt> <dd>

Локализуемое строковое значение для атрибута.

</dd> </dl>

## <a name="remarks"></a>Remarks

Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице. Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



