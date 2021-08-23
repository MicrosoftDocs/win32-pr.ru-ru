---
description: Описывает ошибки поставщика WMI SNMP с 1051 по 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Ошибки с 1051 по 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e75d2fda06b7761fd7e14de936ef7b38fbb18df46dd2597509bc7c1e1502023
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464084"
---
# <a name="errors-1051-through-1060"></a>Ошибки с 1051 по 1060

Описывает ошибки поставщика WMI SNMP с 1051 по 1060.

[Неустранимая ошибка 1051](#fatal-error-1051)

[Неустранимая ошибка 1054](#fatal-error-1054)

[Неустранимая ошибка 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Неустранимая ошибка 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Неустранимая>: " <fileName> : <line \#>: неоднозначные ссылки на символ <identifier> "**
</dt> <dd>

Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C. Каждый дескриптор объекта, соответствующий объекту в стандартной базе MIB в Интернете, должен быть уникальным. Так как корпоративные MIB могут иметь общие дескрипторы объектов, такие дескрипторы, импортированные из двух модулей, должны быть однозначно использованы в модуле MIB с помощью нотации "Module. дескриптор".

</dd> </dl>

## <a name="fatal-error-1054"></a>Неустранимая ошибка 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Неустранимая>: " <fileName> : <line \#>: <identifier> в предложении index не разрешается в один из разрешенных типов"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Тип объекта в предложении INDEX или любой тип, указанный в предложении INDEX, должен разрешаться в скалярный тип, то есть не являющийся последовательностью или не последовательностью типа. Любой тип, указанный в предложении INDEX, также должен разрешаться в один из этих типов.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1055"></a>Неустранимая ошибка 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Неустранимая>: " <fileName> : <line \#>: синтаксис объекта index-Type <identifier> не разрешается в один из разрешенных типов"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Тип объекта в предложении INDEX или любой тип, указанный в предложении INDEX, должен разрешаться в скалярный тип, то есть не являющийся последовательностью или не последовательностью типа.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

 

 



