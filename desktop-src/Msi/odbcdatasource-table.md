---
description: В таблице Одбкдатасаурце перечислены источники данных, принадлежащие установке.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Таблица Одбкдатасаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673368"
---
# <a name="odbcdatasource-table"></a>Таблица Одбкдатасаурце

В таблице Одбкдатасаурце перечислены источники данных, принадлежащие установке.

Таблица Одбкдатасаурце содержит следующие столбцы.



| Столбец            | Type                         | Ключ | Допускает значения NULL |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Идентификатор](identifier.md) | Да   | Нет        |
| Компонент\_       | [Идентификатор](identifier.md) | Нет   | Нет        |
| Описание       | [Text](text.md)             | Нет   | Нет        |
| дривердескриптион | [Text](text.md)             | Нет   | Нет        |
| Регистрация      | [Integer](integer.md)       | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource
</dt> <dd>

Имя внутреннего маркера для источника данных. Первичный ключ для таблицы.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_
</dt> <dd>

Внешний ключ в [таблице Component](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание
</dt> <dd>

Описание, зарегистрированное для этого источника данных. Это значение не может быть локализовано. Описания источников данных ODBC не могут превышать \_ максимальную \_ длину имени DSN SQL \_ .

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>дривердескриптион
</dt> <dd>

Связанный драйвер, который может быть предварительно создан. Это значение не может быть локализовано.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Зарегистрировать
</dt> <dd>

В этом поле указывается тип регистрации для источника данных.



| Константа                                      | Шестнадцатеричный | Decimal | Описание                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **мсидбодбкдатасаурцерегистратионпермачине** | 0x000       | 0       | Источник данных регистрируется на компьютере. |
| **мсидбодбкдатасаурцерегистратионперусер**    | 0x001       | 1       | Источник данных регистрируется для каждого пользователя.    |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Действия [инсталлодбк](installodbc-action.md) и [ремовеодбк](removeodbc-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывают сведения, приведенные в этой таблице. Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



