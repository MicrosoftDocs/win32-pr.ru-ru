---
description: Описывает ошибки поставщика WMI SNMP с 1051 по 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Ошибки с 1051 по 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693378"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="fa42a-103">Ошибки с 1051 по 1060</span><span class="sxs-lookup"><span data-stu-id="fa42a-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="fa42a-104">Описывает ошибки поставщика WMI SNMP с 1051 по 1060.</span><span class="sxs-lookup"><span data-stu-id="fa42a-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="fa42a-105">Неустранимая ошибка 1051</span><span class="sxs-lookup"><span data-stu-id="fa42a-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="fa42a-106">Неустранимая ошибка 1054</span><span class="sxs-lookup"><span data-stu-id="fa42a-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="fa42a-107">Неустранимая ошибка 1055</span><span class="sxs-lookup"><span data-stu-id="fa42a-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="fa42a-108">Неустранимая ошибка 1051</span><span class="sxs-lookup"><span data-stu-id="fa42a-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="fa42a-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Неустранимая>: " <fileName> : <line \#>: неоднозначные ссылки на символ <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="fa42a-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="fa42a-110">Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fa42a-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fa42a-111">Каждый дескриптор объекта, соответствующий объекту в стандартной базе MIB в Интернете, должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="fa42a-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="fa42a-112">Так как корпоративные MIB могут иметь общие дескрипторы объектов, такие дескрипторы, импортированные из двух модулей, должны быть однозначно использованы в модуле MIB с помощью нотации "Module. дескриптор".</span><span class="sxs-lookup"><span data-stu-id="fa42a-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="fa42a-113">Неустранимая ошибка 1054</span><span class="sxs-lookup"><span data-stu-id="fa42a-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="fa42a-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Неустранимая>: " <fileName> : <line \#>: <identifier> в предложении index не разрешается в один из разрешенных типов"**</span><span class="sxs-lookup"><span data-stu-id="fa42a-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="fa42a-115">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="fa42a-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="fa42a-116">Тип объекта в предложении INDEX или любой тип, указанный в предложении INDEX, должен разрешаться в скалярный тип, то есть не являющийся последовательностью или не последовательностью типа.</span><span class="sxs-lookup"><span data-stu-id="fa42a-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="fa42a-117">Любой тип, указанный в предложении INDEX, также должен разрешаться в один из этих типов.</span><span class="sxs-lookup"><span data-stu-id="fa42a-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="fa42a-118">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="fa42a-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="fa42a-119">Неустранимая ошибка 1055</span><span class="sxs-lookup"><span data-stu-id="fa42a-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="fa42a-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Неустранимая>: " <fileName> : <line \#>: синтаксис объекта index-Type <identifier> не разрешается в один из разрешенных типов"**</span><span class="sxs-lookup"><span data-stu-id="fa42a-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="fa42a-121">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="fa42a-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="fa42a-122">Тип объекта в предложении INDEX или любой тип, указанный в предложении INDEX, должен разрешаться в скалярный тип, то есть не являющийся последовательностью или не последовательностью типа.</span><span class="sxs-lookup"><span data-stu-id="fa42a-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="fa42a-123">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="fa42a-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



