---
description: Макрос OBJECT-TYPE содержит обязательные и необязательные предложения, описывающие основные характеристики объекта MIB. Поставщик SNMP преобразует MIB в соответствующие части макроса типа OBJECT-TYPE.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Макрос типа OBJECT-TYPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143393"
---
# <a name="object-type-macro"></a>Макрос типа OBJECT-TYPE

Макрос OBJECT-TYPE содержит обязательные и необязательные предложения, описывающие основные характеристики объекта MIB. Поставщик SNMP преобразует MIB в соответствующие части макроса типа OBJECT-TYPE.

> [!Note]  
> Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Компоненты

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Объект MIB
</dt> <dd>

Объект, который содержит большую часть рассматриваемых данных.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Дескриптор объекта
</dt> <dd>

Уникальное имя или дескриптор объекта, определяющие каждый объект MIB. Каждый дескриптор объекта MIB полностью сопоставляется с именем свойства CIM. Например, **ifIndex** преобразуется в **ifIndex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Предложение СИНТАКСИСа](syntax-clause.md)
</dt> <dd>

Определяет данные и тип объекта MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Предложение INDEX](index-clause.md)
</dt> <dd>

Определяет ключ для выбора уникальной строки таблицы.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Предложение дополнения
</dt> <dd>

Указывает, что указанная коллекция таблиц может считаться расширением другой коллекции таблиц и может заменить предложение INDEX в SNMPv2. Коллекции, на которые ссылается предложение дополнения, можно сочетать с другой коллекцией таблиц для формирования одной коллекции. Результирующая коллекция использует свойства первичного ключа, заданные в последней коллекции таблиц в цепочке.

В этом случае предыдущие правила сопоставления, заданные для предложения INDEX, применяются к последней коллекции таблиц в цепочке. Затем Коллекция объектов сопоставляется с одним определением класса CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT — предложение IDENTIFIER
</dt> <dd>

Содержит уникальный идентификатор объекта для объекта MIB. Этот идентификатор объекта сопоставляется с **\_ идентификатором объекта** квалификатора свойства CIM.

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Предложения доступа и MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Определите права доступа к объекту MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Предложение DESCRIPTION
</dt> <dd>

Предоставляет текстовое описание объекта, которое сопоставляется с **описанием** квалификатора свойства CIM. Это предложение может быть пустым.

Каждая **Таблица** и объект **записи** в определении таблицы SNMP также содержат предложение Description, которое также может быть пустым. Предложения "Таблица" и "Описание записи" объединяются, а результат сопоставляется с **описанием** квалификатора класса CIM.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Предложение STATUS
</dt> <dd>

Указывает, должен ли быть поддерживаемый объект. Если значение предложения STATUS **устарело**, поставщик отклоняет объект MIB из сопоставления. В противном случае предложение STATUS сопоставляется с **состоянием** квалификатора свойства CIM.

Для версии в версии, предпочтительным **является либо** обязательное, либо **необязательное**, но квалификатор может содержать какое **-либо другое** значение. Для SNMPv2C предпочтительным значением **Status** является **Current** или **устарело**, но квалификатор может содержать какое-либо другое значение.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Предложение ДЕФВАЛ
</dt> <dd>

Присваивает значение по умолчанию переменной в строке логической таблицы и сопоставляется со строкой квалификатора свойства CIM **дефвал**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Предложение REFERENCE
</dt> <dd>

Ссылается на другой документ, содержащий дополнительные сведения об объекте. Это предложение сопоставляется со **ссылкой** на КВАЛИФИКАТОР свойства CIM, которая относится к типу String.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Предложение UNITs
</dt> <dd>

Предоставляет точное определение того, что представляет объект. Это предложение соответствует **единицам** квалификатора свойства CIM, которые имеют тип String.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Макрос OBJECT-TYPE описывает основные характеристики отдельного объекта MIB. Набор макросов типа OBJECT можно рассматривать как группу связанных объектов. В SNMPv2C используйте макрос OBJECT-GROUP, чтобы формально сгруппировать наборы связанных объектов в коллекцию. Однако для создания коллекций в настоящее время не существует формального механизма. В целях поставщика SNMP макрос группы объектов игнорируется, но вы можете создавать связи группирования и создавать коллекции.

 

 



