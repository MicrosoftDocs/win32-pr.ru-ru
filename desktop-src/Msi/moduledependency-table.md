---
description: В таблице Модуледепенденци хранится список других модулей слияния, необходимых для правильной работы этого модуля слияния.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Таблица Модуледепенденци
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d527ba5874c8fffb0234dbf8f041f424b7bf9aecff5e8f29005324f2a17fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628591"
---
# <a name="moduledependency-table"></a>Таблица Модуледепенденци

В таблице Модуледепенденци хранится список других модулей слияния, необходимых для правильной работы этого модуля слияния. Эта таблица включает средство слияния или проверки, чтобы убедиться в том, что необходимые модули слияния включены в базу данных установщика пользователя. Средство проверяет, перекрестно ссылаясь на эту таблицу с помощью таблицы ModuleSignature в базе данных установщика.

Таблица Модуледепенденци содержит следующие столбцы.



| Столбец           | Type                         | Ключ | Допускает значения NULL |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Идентификатор](identifier.md) | Д   | Нет        |
| модулелангуаже   | [Integer](integer.md)       | Д   | Нет        |
| рекуиредид       | [Идентификатор](identifier.md) | Д   | Нет        |
| рекуиредлангуаже | [Integer](integer.md)       | Д   | Нет        |
| RequiredVersion  | [Версия](version.md)       |     | Д        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Идентификатор модуля слияния. Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>модулелангуаже
</dt> <dd>

Десятичный идентификатор языка модуля слияния в ModuleID. Это внешний ключ в [таблице ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>рекуиредид
</dt> <dd>

Идентификатор модуля слияния, который требуется модулю слияния в ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>рекуиредлангуаже
</dt> <dd>

Числовой идентификатор языка модуля слияния в Рекуиредид. В столбце Рекуиредлангуаже можно указать идентификатор языка для одного языка, например 1033 для английского языка (США), или указать идентификатор языка для языковой группы, например 9 для любого английского языка. Если поле содержит идентификатор языка группы, то любой модуль слияния с кодом языка в этой группе удовлетворяет зависимости. Если Рекуиредлангуаже имеет значение 0, любой модуль слияния, заполняющий другие требования, удовлетворяет зависимости.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Версия модуля слияния в Рекуиредид. Если это поле имеет значение null, любая версия заполняет зависимость.

</dd> </dl>

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



