---
description: Таблица Одбксаурцеаттрибуте содержит сведения об атрибутах источников данных.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Таблица Одбксаурцеаттрибуте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082714"
---
# <a name="odbcsourceattribute-table"></a>Таблица Одбксаурцеаттрибуте

Таблица Одбксаурцеаттрибуте содержит сведения об атрибутах источников данных.

Таблица Одбксаурцеаттрибуте содержит следующие столбцы.



| Столбец       | Type                         | Ключ | Допускает значения NULL |
|--------------|------------------------------|-----|----------|
| DataSource\_ | [Идентификатор](identifier.md) | Д   | Нет        |
| attribute    | [Text](text.md)             | Д   | Нет        |
| Значение        | [Формате](formatted.md)   | Нет   | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_
</dt> <dd>

Имя внутреннего маркера для источника данных. Первичный ключ для таблицы.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Версию
</dt> <dd>

Имя атрибута источника данных. Первичный ключ для таблицы.

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

 

 



