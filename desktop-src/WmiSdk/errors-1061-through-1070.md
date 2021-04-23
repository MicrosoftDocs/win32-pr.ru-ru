---
description: Описывает ошибки поставщика WMI SNMP с 1061 по 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Ошибки с 1061 по 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692832"
---
# <a name="errors-1061-through-1070"></a><span data-ttu-id="70d0b-103">Ошибки с 1061 по 1070</span><span class="sxs-lookup"><span data-stu-id="70d0b-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="70d0b-104">Описывает ошибки поставщика WMI SNMP с 1061 по 1070.</span><span class="sxs-lookup"><span data-stu-id="70d0b-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="70d0b-105">Неустранимая ошибка 1063</span><span class="sxs-lookup"><span data-stu-id="70d0b-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="70d0b-106">Неустранимая ошибка 1064</span><span class="sxs-lookup"><span data-stu-id="70d0b-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="70d0b-107">Неустранимая ошибка 1070</span><span class="sxs-lookup"><span data-stu-id="70d0b-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="70d0b-108">Неустранимая ошибка 1063</span><span class="sxs-lookup"><span data-stu-id="70d0b-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="70d0b-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Неустранимая>: " <fileName><line \#>: Верхняя граница спецификации размера меньше нижней границы"**</span><span class="sxs-lookup"><span data-stu-id="70d0b-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="70d0b-110">Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="70d0b-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="70d0b-111">Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="70d0b-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="70d0b-112">Нижняя граница спецификации диапазона или размера не должна превышать верхнюю границу.</span><span class="sxs-lookup"><span data-stu-id="70d0b-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="70d0b-113">Неустранимая ошибка 1064</span><span class="sxs-lookup"><span data-stu-id="70d0b-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="70d0b-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Неустранимая>: " <fileName> : <line \#>: элемент последовательности <identifier> не разрешается в объектный тип"**</span><span class="sxs-lookup"><span data-stu-id="70d0b-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="70d0b-115">Семантическая ошибка модуля назначения типа, относящаяся к ни к, ни к, ни к SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="70d0b-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="70d0b-116">Все отдельные элементы объявления последовательности должны разрешаться в ОБЪЕКТный тип.</span><span class="sxs-lookup"><span data-stu-id="70d0b-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="70d0b-117">Неустранимая ошибка 1070</span><span class="sxs-lookup"><span data-stu-id="70d0b-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="70d0b-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Неустранимая>: " <fileName><line \#>: модуль MIB <moduleName> , из которого <symbolName> импортируется символ, отсутствует во входных данных"**</span><span class="sxs-lookup"><span data-stu-id="70d0b-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="70d0b-119">Семантическая ошибка модуля в перекрестных ссылках, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="70d0b-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="70d0b-120">Если один из модулей в разделе IMPORTs основного модуля или дочернего модуля не существует и на самом деле имеются ссылки на один или несколько символов из этого модуля, возникает такая Неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="70d0b-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



