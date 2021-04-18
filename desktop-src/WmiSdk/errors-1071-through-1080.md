---
description: Описывает ошибки поставщика WMI SNMP с 1071 по 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Ошибки с 1071 по 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703313"
---
# <a name="errors-1071-through-1080"></a><span data-ttu-id="0d1e6-103">Ошибки с 1071 по 1080</span><span class="sxs-lookup"><span data-stu-id="0d1e6-103">Errors 1071 through 1080</span></span>

<span data-ttu-id="0d1e6-104">Описывает ошибки поставщика WMI SNMP с 1071 по 1080.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-104">Describes WMI SNMP provider errors 1071 through 1080.</span></span>

[<span data-ttu-id="0d1e6-105">Предупреждение 1071</span><span class="sxs-lookup"><span data-stu-id="0d1e6-105">Warning 1071</span></span>](#warning-1071)

[<span data-ttu-id="0d1e6-106">Предупреждение 1072</span><span class="sxs-lookup"><span data-stu-id="0d1e6-106">Warning 1072</span></span>](#warning-1072)

[<span data-ttu-id="0d1e6-107">Неустранимая ошибка 1074</span><span class="sxs-lookup"><span data-stu-id="0d1e6-107">Fatal Error 1074</span></span>](#fatal-error-1074)

[<span data-ttu-id="0d1e6-108">Неустранимая ошибка 1075</span><span class="sxs-lookup"><span data-stu-id="0d1e6-108">Fatal Error 1075</span></span>](#fatal-error-1075)

[<span data-ttu-id="0d1e6-109">Неустранимая ошибка 1077</span><span class="sxs-lookup"><span data-stu-id="0d1e6-109">Fatal Error 1077</span></span>](#fatal-error-1077)

[<span data-ttu-id="0d1e6-110">Неустранимая ошибка 1079</span><span class="sxs-lookup"><span data-stu-id="0d1e6-110">Fatal Error 1079</span></span>](#fatal-error-1079)

[<span data-ttu-id="0d1e6-111">Предупреждение 1080</span><span class="sxs-lookup"><span data-stu-id="0d1e6-111">Warning 1080</span></span>](#warning-1080)

## <a name="warning-1071"></a><span data-ttu-id="0d1e6-112">Предупреждение 1071</span><span class="sxs-lookup"><span data-stu-id="0d1e6-112">Warning 1071</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, предупреждение>: " <fileName><строка \#>: символ <identifier> отсутствует в импортированном модуле <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-113"><span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, Warning>: "<fileName><line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-114">Семантическое предупреждение модуля о перекрестных ссылках, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-114">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0d1e6-115">Символ, импортированный из модуля, не разрешается ни на что в этом модуле.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-115">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="0d1e6-116">Несмотря на то, что этот модуль указан во входных данных, отображается это предупреждение.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-116">Even though that module is specified in the input, this warning appears.</span></span>

</dd> </dl>

## <a name="warning-1072"></a><span data-ttu-id="0d1e6-117">Предупреждение 1072</span><span class="sxs-lookup"><span data-stu-id="0d1e6-117">Warning 1072</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, предупреждение>: " <fileName> : <строка \#> объект-тип <name> является потомком объекта типа <name> module <name> "**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-118"><span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Warning>: "<fileName>:<line\#> OBJECT-TYPE <name> is a descendant of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-119">**Тип объекта —** семантическое предупреждение модуля вызова макроса.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-119">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="0d1e6-120">Скалярный объект не может иметь дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-120">A scalar object cannot have any descendant objects.</span></span>

<span data-ttu-id="0d1e6-121">Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-121">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1074"></a><span data-ttu-id="0d1e6-122">Неустранимая ошибка 1074</span><span class="sxs-lookup"><span data-stu-id="0d1e6-122">Fatal Error 1074</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Неустранимая>: " <fileName> : <строка \#> Sequence (концептуальная строка) тип объекта не <name> имеет последовательности (концептуальной таблицы) типа Object-Type в качестве родительского элемента"**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-123"><span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074, Fatal>: "<fileName>:<line\#> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-124">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="0d1e6-124">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="0d1e6-125">Каждый объект Row должен иметь объект Table в качестве своего родителя.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-125">Every row object must have a table object as its parent.</span></span>

<span data-ttu-id="0d1e6-126">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-126">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1075"></a><span data-ttu-id="0d1e6-127">Неустранимая ошибка 1075</span><span class="sxs-lookup"><span data-stu-id="0d1e6-127">Fatal Error 1075</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Неустранимая>: " <fileName> : <line \#>: тип объекта <name> не может быть дочерним по отношению к типу объекта Table, <name> <name> если он не находится в последовательности последних"**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-128"><span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE <name> cannot be a child of table OBJECT-TYPE <name> of module <name> unless it is in the SEQUENCE of the latter"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-129">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="0d1e6-129">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="0d1e6-130">Каждый объект последовательности должен иметь точно те же объекты, которые упоминаются в определении типа последовательности в качестве дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-130">Every SEQUENCE object must have exactly the same objects that are mentioned in the SEQUENCE type definition as its children.</span></span> <span data-ttu-id="0d1e6-131">Аналогичным образом каждая последовательность объекта должна иметь только один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-131">Similarly, every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="0d1e6-132">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-132">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1077"></a><span data-ttu-id="0d1e6-133">Неустранимая ошибка 1077</span><span class="sxs-lookup"><span data-stu-id="0d1e6-133">Fatal Error 1077</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Неустранимая>: " <fileName> : <line \#>: синтаксис табличного типа" объект-тип <name> "не является последовательностью синтаксиса типа" дочерний объект <name> "для модуля <name> "**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-134"><span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, Fatal>: "<fileName>:<line\#>: The syntax of table OBJECT-TYPE <name> is not the SEQUENCE OF the syntax of the child OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-135">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="0d1e6-135">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="0d1e6-136">Предложение синтаксиса объекта таблицы должно быть "последовательностью" синтаксиса объекта Row.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-136">The syntax clause of a table object must be the "SEQUENCE OF" of the syntax of the row object.</span></span>

<span data-ttu-id="0d1e6-137">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-137">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1079"></a><span data-ttu-id="0d1e6-138">Неустранимая ошибка 1079</span><span class="sxs-lookup"><span data-stu-id="0d1e6-138">Fatal Error 1079</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Неустранимая>: "имя_файла>: <строка \#>: Object-Type <name> является дополнительным дочерним объектом для типа <name> модуля <name> "**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-139"><span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, Fatal>:"fileName>:<line\#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE <name> of module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-140">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="0d1e6-140">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="0d1e6-141">Каждая последовательность объекта должна иметь только один дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-141">Every SEQUENCE OF object must have exactly one child.</span></span>

<span data-ttu-id="0d1e6-142">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-142">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1080"></a><span data-ttu-id="0d1e6-143">Предупреждение 1080</span><span class="sxs-lookup"><span data-stu-id="0d1e6-143">Warning 1080</span></span>

<dl> <dt>

<span data-ttu-id="0d1e6-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, предупреждение>: " <fileName><line \#>: модуль MIB <moduleName> , из которого <symbolName> импортируется символ, отсутствует во входных данных"**</span><span class="sxs-lookup"><span data-stu-id="0d1e6-144"><span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, Warning>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="0d1e6-145">Семантическое предупреждение модуля о перекрестных ссылках, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-145">Module semantic warning about cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0d1e6-146">Если один из модулей в разделе IMPORTs основного модуля или дочернего модуля не существует, но на символы из этого модуля нет ссылок, отображается это предупреждение.</span><span class="sxs-lookup"><span data-stu-id="0d1e6-146">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist, but symbols from this module are not referenced, this warning appears.</span></span>

</dd> </dl>

 

 



