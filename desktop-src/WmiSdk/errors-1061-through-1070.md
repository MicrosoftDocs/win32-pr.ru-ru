---
description: Описывает ошибки поставщика WMI SNMP с 1061 по 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Ошибки с 1061 по 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0072f30c8daf584c1aaf2acf783b15d2d9498a3c1479264a1db361c3e3ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924578"
---
# <a name="errors-1061-through-1070"></a>Ошибки с 1061 по 1070

Описывает ошибки поставщика WMI SNMP с 1061 по 1070.

[Неустранимая ошибка 1063](#fatal-error-1063)

[Неустранимая ошибка 1064](#fatal-error-1064)

[Неустранимая ошибка 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Неустранимая ошибка 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Неустранимая>: " <fileName><line \#>: Верхняя граница спецификации размера меньше нижней границы"**
</dt> <dd>

Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C. Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность. Нижняя граница спецификации диапазона или размера не должна превышать верхнюю границу.

</dd> </dl>

## <a name="fatal-error-1064"></a>Неустранимая ошибка 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Неустранимая>: " <fileName> : <line \#>: элемент последовательности <identifier> не разрешается в объектный тип"**
</dt> <dd>

Семантическая ошибка модуля назначения типа, относящаяся к ни к, ни к, ни к SNMPv2C. Все отдельные элементы объявления последовательности должны разрешаться в ОБЪЕКТный тип.

</dd> </dl>

## <a name="fatal-error-1070"></a>Неустранимая ошибка 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Неустранимая>: " <fileName><line \#>: модуль MIB <moduleName> , из которого <symbolName> импортируется символ, отсутствует во входных данных"**
</dt> <dd>

Семантическая ошибка модуля в перекрестных ссылках, характерная для неограниченного или SNMPv2C. Если один из модулей в разделе IMPORTs основного модуля или дочернего модуля не существует и на самом деле имеются ссылки на один или несколько символов из этого модуля, возникает такая Неустранимая ошибка.

</dd> </dl>

 

 



