---
description: Описывает ошибки поставщика WMI SNMP с 1071 по 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Ошибки с 1071 по 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c92cfd1c79b5bedd070229adcbc4c663d209903428073fc976cd575022e9ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679624"
---
# <a name="errors-1071-through-1080"></a>Ошибки с 1071 по 1080

Описывает ошибки поставщика WMI SNMP с 1071 по 1080.

[Предупреждение 1071](#warning-1071)

[Предупреждение 1072](#warning-1072)

[Неустранимая ошибка 1074](#fatal-error-1074)

[Неустранимая ошибка 1075](#fatal-error-1075)

[Неустранимая ошибка 1077](#fatal-error-1077)

[Неустранимая ошибка 1079](#fatal-error-1079)

[Предупреждение 1080](#warning-1080)

## <a name="warning-1071"></a>Предупреждение 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, предупреждение>: " <fileName><строка \#>: символ <identifier> отсутствует в импортированном модуле <identifier> "**
</dt> <dd>

Семантическое предупреждение модуля о перекрестных ссылках, характерное для неограниченного или SNMPv2C. Символ, импортированный из модуля, не разрешается ни на что в этом модуле. Несмотря на то, что этот модуль указан во входных данных, отображается это предупреждение.

</dd> </dl>

## <a name="warning-1072"></a>Предупреждение 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, предупреждение>: " <fileName> : <строка \#> объект-тип <name> является потомком объекта типа <name> module <name> "**
</dt> <dd>

**Тип объекта —** семантическое предупреждение модуля вызова макроса. Скалярный объект не может иметь дочерние объекты.

Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Неустранимая ошибка 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Неустранимая>: " <fileName> : <строка \#> Sequence (концептуальная строка) тип объекта не <name> имеет последовательности (концептуальной таблицы) типа Object-Type в качестве родительского элемента"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Каждый объект Row должен иметь объект Table в качестве своего родителя.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1075"></a>Неустранимая ошибка 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Неустранимая>: " <fileName> : <line \#>: тип объекта <name> не может быть дочерним по отношению к типу объекта Table, <name> <name> если он не находится в последовательности последних"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Каждый объект последовательности должен иметь точно те же объекты, которые упоминаются в определении типа последовательности в качестве дочерних элементов. Аналогичным образом каждая последовательность объекта должна иметь только один дочерний элемент.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1077"></a>Неустранимая ошибка 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Неустранимая>: " <fileName> : <line \#>: синтаксис табличного типа" объект-тип <name> "не является последовательностью синтаксиса типа" дочерний объект <name> "для модуля <name> "**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Предложение синтаксиса объекта таблицы должно быть "последовательностью" синтаксиса объекта Row.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1079"></a>Неустранимая ошибка 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Неустранимая>: "имя_файла>: <строка \#>: Object-Type <name> является дополнительным дочерним объектом для типа <name> модуля <name> "**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Каждая последовательность объекта должна иметь только один дочерний элемент.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="warning-1080"></a>Предупреждение 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, предупреждение>: " <fileName><line \#>: модуль MIB <moduleName> , из которого <symbolName> импортируется символ, отсутствует во входных данных"**
</dt> <dd>

Семантическое предупреждение модуля о перекрестных ссылках, характерное для неограниченного или SNMPv2C. Если один из модулей в разделе IMPORTs основного модуля или дочернего модуля не существует, но на символы из этого модуля нет ссылок, отображается это предупреждение.

</dd> </dl>

 

 



