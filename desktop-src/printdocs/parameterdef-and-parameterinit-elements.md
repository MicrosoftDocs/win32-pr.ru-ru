---
description: Этот раздел не является актуальным. Текущие сведения см. в спецификации печати схемы.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Элементы Параметердеф и Параметеринит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693911"
---
# <a name="parameterdef-and-parameterinit-elements"></a><span data-ttu-id="df094-104">Элементы Параметердеф и Параметеринит</span><span class="sxs-lookup"><span data-stu-id="df094-104">ParameterDef and ParameterInit Elements</span></span>

<span data-ttu-id="df094-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="df094-105">This topic is not current.</span></span> <span data-ttu-id="df094-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="df094-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="df094-107">Элемент Параметердеф отличается от элемента Параметеринит тем, что он описывает значение, которое может содержать элемент Параметеринит, а элемент Параметеринит присваивает параметру значение.</span><span class="sxs-lookup"><span data-stu-id="df094-107">A ParameterDef element differs from a ParameterInit element in that it describes the value that a ParameterInit element can contain, while a ParameterInit element assigns a value to the parameter.</span></span> <span data-ttu-id="df094-108">Элемент Параметердеф состоит из определенного набора элементов свойств, являющихся дочерними элементами элемента Параметердеф, которые указывают тип данных, максимальное, минимальное и значение по умолчанию для данных и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="df094-108">A ParameterDef element consists of a specific set of Property elements, which are children of the ParameterDef element, that specify the type of data, maximum, minimum, and default values for the data, and other information.</span></span> <span data-ttu-id="df094-109">Эти элементы свойств обсуждаются далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="df094-109">These Property elements are discussed later in this topic.</span></span>

<span data-ttu-id="df094-110">Элементы Параметердеф могут использоваться только в разрешенном контексте.</span><span class="sxs-lookup"><span data-stu-id="df094-110">ParameterDef elements can appear only in their allowed context.</span></span> <span data-ttu-id="df094-111">Для начальной версии схемы печати они могут располагаться на корневом уровне документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="df094-111">For the initial version of the Print Schema they may be located at the root level of the PrintCapabilities document.</span></span> <span data-ttu-id="df094-112">Атрибут Name элемента Параметердеф определяет имя параметра.</span><span class="sxs-lookup"><span data-stu-id="df094-112">The name attribute of the ParameterDef element defines the parameter name.</span></span> <span data-ttu-id="df094-113">Каждому элементу Параметердеф в документе PrintCapabilities должен быть назначен уникальный атрибут имени.</span><span class="sxs-lookup"><span data-stu-id="df094-113">Each ParameterDef element in the PrintCapabilities document must be assigned a unique name attribute.</span></span>

> [!Note]
> <span data-ttu-id="df094-114">для печати возможностей поставщиков документов:</span><span class="sxs-lookup"><span data-stu-id="df094-114">to Print Capabilities Document Providers:</span></span>
> 
> <span data-ttu-id="df094-115">Значение имени параметра является универсальным; то есть, если элемент Параметердеф в одном документе PrintCapabilities имеет тот же атрибут Name (строка, сформированная из пространства имен и описательное имя элемента Параметердеф) в качестве элемента Параметердеф в другом PrintCapabilities документе, предполагается, что оба этих элемента представляют одну и ту же концепцию и должны интерпретироваться одинаковым образом.</span><span class="sxs-lookup"><span data-stu-id="df094-115">The meaning of a parameter name is universal; that is, if a ParameterDef element in one PrintCapabilities document has the same name attribute (the string formed from the namespace and the descriptive name of the ParameterDef element) as a ParameterDef element in another PrintCapabilities document, it is assumed that both of these elements represent the same concept and should be interpreted in the same manner.</span></span> <span data-ttu-id="df094-116">Поэтому элемент Параметердеф, определенный в PrintTicket для одного документа PrintCapabilities, можно использовать для инициализации элемента Параметеринит с тем же именем, определенным в другом PrintCapabilities документе.</span><span class="sxs-lookup"><span data-stu-id="df094-116">Thus a ParameterDef element defined in a PrintTicket for one PrintCapabilities document can be used to initialize the ParameterInit element of the same name defined in a different PrintCapabilities document.</span></span>

 

## <a name="relationship-to-xml-attributes"></a><span data-ttu-id="df094-117">Связь с XML-атрибутами</span><span class="sxs-lookup"><span data-stu-id="df094-117">Relationship to XML Attributes</span></span>

<span data-ttu-id="df094-118">Как и в случае со всеми атрибутами имени, имя параметра представлено в формате XML QName.</span><span class="sxs-lookup"><span data-stu-id="df094-118">As is true of all name attributes, the parameter name is in the form of an XML QName.</span></span> <span data-ttu-id="df094-119">Конструкция параметра, определяемая схемой, имеет имя, уточненное общедоступным пространством имен, формирующее атрибут Name, а атрибут Name для закрытой конструкции параметра дополнен закрытым пространством имен, уникальным для создателя.</span><span class="sxs-lookup"><span data-stu-id="df094-119">A Schema-defined parameter construct has a name that is qualified by the public namespace, forming the name attribute, while the name attribute of a privately-defined parameter construct is qualified by a private namespace that is unique to the creator.</span></span>

## <a name="relationship-between-parameterdef-and-property-element-types"></a><span data-ttu-id="df094-120">Отношение между Параметердеф и типами элементов свойств</span><span class="sxs-lookup"><span data-stu-id="df094-120">Relationship between ParameterDef and Property Element Types</span></span>

<span data-ttu-id="df094-121">Элементы Параметердеф, определенные в ключевых словах схемы Print, должны быть полностью определены в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="df094-121">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span> <span data-ttu-id="df094-122">Документ по ключевым словам схемы печати предоставляет номинальные значения для некоторых элементов свойств элемента Параметердеф (например, DefaultValue и др.), но автор документа PrintCapabilities отвечает за определение остальных элементов свойств.</span><span class="sxs-lookup"><span data-stu-id="df094-122">The Print Schema Keywords document provides nominal values for some Property elements of a ParameterDef element (such as DefaultValue and others), but the author of a PrintCapabilities document is responsible for defining the remaining Property elements.</span></span> <span data-ttu-id="df094-123">В любом случае все элементы свойств должны быть явно определены в элементе Параметердеф, включая те, которые определены в ключевых словах схемы Print.</span><span class="sxs-lookup"><span data-stu-id="df094-123">In any case, all Property elements must be explicitly defined in a ParameterDef element, including those that are defined in the Print Schema Keywords.</span></span>

<span data-ttu-id="df094-124">Некоторые элементы свойств каждого элемента Параметердеф, отображаемые в ключевых словах схемы Print, обозначаются как *неизменяемые*.</span><span class="sxs-lookup"><span data-stu-id="df094-124">Certain Property elements of each ParameterDef element appearing in the Print Schema Keywords are designated as *immutable*.</span></span> <span data-ttu-id="df094-125">Это означает, что все определения документов PrintCapabilities, определяемые ключевыми словами схемы печати, должны сохранять эти элементы свойств без изменения.</span><span class="sxs-lookup"><span data-stu-id="df094-125">This means that all PrintCapabilities document definitions of Print Schema Keywords-defined ParameterDef elements must preserve these Property elements without modification.</span></span> <span data-ttu-id="df094-126">Эти неизменяемые элементы свойств позволяют использовать конструкции параметров как переносимые, так и неоднозначные во всех документах PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="df094-126">These immutable Property elements allow the parameter constructs to be portable and unambiguous across all PrintCapabilities documents.</span></span> <span data-ttu-id="df094-127">Простым примером являются единицы, используемые в элементе Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="df094-127">A prime example is the units used in a ParameterDef element.</span></span> <span data-ttu-id="df094-128">Эти единицы должны быть неизменяемыми, чтобы обеспечить согласованное понимание их значения.</span><span class="sxs-lookup"><span data-stu-id="df094-128">These units should be immutable, to promote a consistent understanding of their meaning.</span></span> <span data-ttu-id="df094-129">Элементы свойств Параметердеф, которые обозначены как неизменяемые, могут быть переопределены в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="df094-129">Property elements of a ParameterDef that are designated as not immutable may be redefined within a PrintCapabilities document.</span></span>

<span data-ttu-id="df094-130">Элемент Параметердеф состоит из следующих элементов свойств.</span><span class="sxs-lookup"><span data-stu-id="df094-130">A ParameterDef element is composed of the following Property elements.</span></span> <span data-ttu-id="df094-131">Если не указано иное, должны быть указаны все.</span><span class="sxs-lookup"><span data-stu-id="df094-131">All must be present unless otherwise noted.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df094-132">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="df094-132">Property Name</span></span></th>
<th><span data-ttu-id="df094-133">Значения</span><span class="sxs-lookup"><span data-stu-id="df094-133">Values</span></span></th>
<th><span data-ttu-id="df094-134">Описание</span><span class="sxs-lookup"><span data-stu-id="df094-134">Description</span></span></th>
<th><span data-ttu-id="df094-135">Неизменяемый?</span><span class="sxs-lookup"><span data-stu-id="df094-135">Immutable?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df094-136">DataType</span><span class="sxs-lookup"><span data-stu-id="df094-136">DataType</span></span> <br/></td>
<td><span data-ttu-id="df094-137">Целое число</span><span class="sxs-lookup"><span data-stu-id="df094-137">integer</span></span> <br/> <span data-ttu-id="df094-138">Decimal</span><span class="sxs-lookup"><span data-stu-id="df094-138">decimal</span></span><br/> <span data-ttu-id="df094-139">строка</span><span class="sxs-lookup"><span data-stu-id="df094-139">string</span></span><br/> <span data-ttu-id="df094-140">Нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df094-140">No default value.</span></span><br/></td>
<td><span data-ttu-id="df094-141">Указывает, является ли значение параметра целым числом или числом с плавающей запятой или текстовой строкой.</span><span class="sxs-lookup"><span data-stu-id="df094-141">Specifies whether the parameter value is an integer, or floating point number, or a text string.</span></span> <span data-ttu-id="df094-142">Значение параметра выражается в том же формате, что и соответствующий тип данных XSD Basic; то есть целое число, десятичное значение или строка.</span><span class="sxs-lookup"><span data-stu-id="df094-142">The value of a parameter is expressed in the same format as the corresponding XSD basic data type; that is, as an integer, decimal, or string.</span></span> <br/></td>
<td><span data-ttu-id="df094-143">Да</span><span class="sxs-lookup"><span data-stu-id="df094-143">Yes</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df094-144">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="df094-144">DefaultValue</span></span> <br/></td>
<td><span data-ttu-id="df094-145">Тип, заданный свойством DataType.</span><span class="sxs-lookup"><span data-stu-id="df094-145">The type specified by the DataType Property.</span></span><br/> <span data-ttu-id="df094-146">Нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df094-146">No default value.</span></span><br/></td>
<td><span data-ttu-id="df094-147">Задает значение, с помощью которого инициализируется элемент управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="df094-147">Specifies the value with which to initialize a user interface (UI) control.</span></span><br/>
<ul>
<li><span data-ttu-id="df094-148">или</span><span class="sxs-lookup"><span data-stu-id="df094-148">or</span></span> <br/></li>
</ul>
<span data-ttu-id="df094-149">Указывает значение, используемое, если соответствующий элемент Parameter отсутствует в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="df094-149">Specifies the value to use if the relevant parameter element is missing from the PrintTicket.</span></span><br/></td>
<td><span data-ttu-id="df094-150">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-150">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df094-151">Обязательный</span><span class="sxs-lookup"><span data-stu-id="df094-151">Mandatory</span></span> <br/></td>
<td><span data-ttu-id="df094-152">Безусловное: элемент Параметеринит всегда должен быть представлен.</span><span class="sxs-lookup"><span data-stu-id="df094-152">Unconditional: the ParameterInit element must always be supplied.</span></span> <br/> <span data-ttu-id="df094-153">Conditional: элемент Параметеринит является обязательным только в том случае, если на параметр ссылается элемент Option в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="df094-153">Conditional: the ParameterInit element is required only if the parameter is referenced within an Option element in a PrintTicket.</span></span><br/> <span data-ttu-id="df094-154">DefaultValue: Conditional.</span><span class="sxs-lookup"><span data-stu-id="df094-154">DefaultValue: Conditional.</span></span><br/></td>
<td><span data-ttu-id="df094-155">Указывает, что элемент Параметеринит должен явно отображаться.</span><span class="sxs-lookup"><span data-stu-id="df094-155">Indicates when a ParameterInit element must appear explicitly.</span></span> <span data-ttu-id="df094-156">Если условный, Параметеринит должен быть инициализирован, если PrintTicket содержит параметр, который ссылается на этот параметр.</span><span class="sxs-lookup"><span data-stu-id="df094-156">If Conditional, the ParameterInit must be initialized if the PrintTicket contains an Option that references the parameter.</span></span><br/> <span data-ttu-id="df094-157">Используется клиентами пользовательского интерфейса и поставщиками PrintCapabilities или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="df094-157">Used by UI Clients and PrintCapabilities or PrintTicket providers.</span></span> <span data-ttu-id="df094-158">Обратите внимание, что в любом ограничении для обязательного свойства элемента Параметердеф должно быть задано безусловное значение.</span><span class="sxs-lookup"><span data-stu-id="df094-158">Note that in any constraint, the Mandatory Property of the ParameterDef element must be set to Unconditional.</span></span> <span data-ttu-id="df094-159">Параметердеф должен иметь определенное значение, в противном случае не удалось вычислить зависимое значение или ограничение.</span><span class="sxs-lookup"><span data-stu-id="df094-159">The ParameterDef must have a defined Value, otherwise the dependent Value or constraint could not be evaluated.</span></span><br/></td>
<td><span data-ttu-id="df094-160">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-160">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df094-161">MaxLength</span><span class="sxs-lookup"><span data-stu-id="df094-161">MaxLength</span></span> <br/></td>
<td><span data-ttu-id="df094-162">Integer, если свойство DataType указывает строку.</span><span class="sxs-lookup"><span data-stu-id="df094-162">integer if DataType Property specifies string.</span></span><br/> <span data-ttu-id="df094-163">DefaultValue: максимальное значение не применяется.</span><span class="sxs-lookup"><span data-stu-id="df094-163">DefaultValue: No maximum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="df094-164">Для параметров, возвращающих строковое значение, указывает максимально допустимую строку.</span><span class="sxs-lookup"><span data-stu-id="df094-164">For string-valued parameters, specifies the longest allowed string.</span></span> <span data-ttu-id="df094-165">Поставщики UI и PrintCapabilities или PrintTicket используют это свойство для проверки элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="df094-165">UI and PrintCapabilities or PrintTicket providers use this Property to validate the ParameterDef element.</span></span><br/></td>
<td><span data-ttu-id="df094-166">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-166">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df094-167">MaxValue</span><span class="sxs-lookup"><span data-stu-id="df094-167">MaxValue</span></span> <br/></td>
<td><span data-ttu-id="df094-168">Integer, если свойство DataType задает целое число.</span><span class="sxs-lookup"><span data-stu-id="df094-168">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="df094-169">Decimal, если свойство DataType определяет значение Decimal.</span><span class="sxs-lookup"><span data-stu-id="df094-169">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="df094-170">DefaultValue: максимальное значение не применяется.</span><span class="sxs-lookup"><span data-stu-id="df094-170">DefaultValue: No maximum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="df094-171">Для элементов Параметердеф с целочисленным или десятичным значением определяет максимально допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="df094-171">For integer-or decimal-valued ParameterDef elements, defines the largest allowed value.</span></span><br/></td>
<td><span data-ttu-id="df094-172">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-172">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df094-173">MinLength</span><span class="sxs-lookup"><span data-stu-id="df094-173">MinLength</span></span> <br/></td>
<td><span data-ttu-id="df094-174">Integer, если свойство DataType указывает строку.</span><span class="sxs-lookup"><span data-stu-id="df094-174">integer if DataType Property specifies string.</span></span> <br/> <span data-ttu-id="df094-175">DefaultValue: не применяется минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="df094-175">DefaultValue: No minimum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="df094-176">Для строковых значений определяет минимально допустимую строку.</span><span class="sxs-lookup"><span data-stu-id="df094-176">For string values, defines the shortest allowed string.</span></span> <span data-ttu-id="df094-177">Поставщики UI и PrintCapabilities или PrintTicket используют это свойство для проверки элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="df094-177">UI and PrintCapabilities or PrintTicket providers use this Property to validate the ParameterDef element.</span></span><br/></td>
<td><span data-ttu-id="df094-178">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-178">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df094-179">MinValue</span><span class="sxs-lookup"><span data-stu-id="df094-179">MinValue</span></span> <br/></td>
<td><span data-ttu-id="df094-180">Integer, если свойство DataType задает целое число.</span><span class="sxs-lookup"><span data-stu-id="df094-180">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="df094-181">Decimal, если свойство DataType определяет значение Decimal.</span><span class="sxs-lookup"><span data-stu-id="df094-181">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="df094-182">DefaultValue: не применяется минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="df094-182">DefaultValue: No minimum value is enforced.</span></span><br/></td>
<td><span data-ttu-id="df094-183">Для параметров с целочисленным или десятичным значением определяет наименьшее допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="df094-183">For integer- or decimal-valued parameters, defines the smallest allowed value.</span></span> <br/></td>
<td><span data-ttu-id="df094-184">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-184">No</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df094-185">Несколько</span><span class="sxs-lookup"><span data-stu-id="df094-185">Multiple</span></span> <br/></td>
<td><span data-ttu-id="df094-186">Integer, если свойство DataType задает целое число.</span><span class="sxs-lookup"><span data-stu-id="df094-186">integer if DataType Property specifies integer.</span></span><br/> <span data-ttu-id="df094-187">Decimal, если свойство DataType определяет значение Decimal.</span><span class="sxs-lookup"><span data-stu-id="df094-187">decimal if DataType Property specifies decimal.</span></span><br/> <span data-ttu-id="df094-188">DefaultValue: 1</span><span class="sxs-lookup"><span data-stu-id="df094-188">DefaultValue: 1</span></span><br/></td>
<td><span data-ttu-id="df094-189">Для параметров с целочисленным или десятичным значением значение параметра должно быть кратным этому числу.</span><span class="sxs-lookup"><span data-stu-id="df094-189">For integer- or decimal-valued parameters, the value of the parameter should be a multiple of this number.</span></span> <span data-ttu-id="df094-190">Дополнительные сведения см. <a href="#notes-on-multiple">в разделе Примечания по нескольким</a> следующим таблицам.</span><span class="sxs-lookup"><span data-stu-id="df094-190">For more information, see <a href="#notes-on-multiple">Notes on Multiple</a> following this table.</span></span><br/></td>
<td><span data-ttu-id="df094-191">Нет</span><span class="sxs-lookup"><span data-stu-id="df094-191">No</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df094-192">Единицах UnitType</span><span class="sxs-lookup"><span data-stu-id="df094-192">UnitType</span></span> <br/></td>
<td><span data-ttu-id="df094-193">Строковое значение, указывающее единицы, используемые для параметра.</span><span class="sxs-lookup"><span data-stu-id="df094-193">string value indicating the units used for the parameter.</span></span><br/> <span data-ttu-id="df094-194">Нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df094-194">No default value.</span></span><br/></td>
<td><span data-ttu-id="df094-195">Указывает единицы, в которых выражается параметр.</span><span class="sxs-lookup"><span data-stu-id="df094-195">Indicates the units in which the parameter is expressed.</span></span> <span data-ttu-id="df094-196">Например, угол в десятых долях градуса, длина в микронах и т. д.</span><span class="sxs-lookup"><span data-stu-id="df094-196">For example, angles in tenths of degrees, lengths in microns, and so on.</span></span><br/></td>
<td><span data-ttu-id="df094-197">Да</span><span class="sxs-lookup"><span data-stu-id="df094-197">Yes</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a><span data-ttu-id="df094-198">Примечания к нескольким</span><span class="sxs-lookup"><span data-stu-id="df094-198">Notes on Multiple</span></span>

<span data-ttu-id="df094-199">Для элементов Параметеринит с целочисленными или десятичными значениями значение Параметеринит должно быть кратным этому числу.</span><span class="sxs-lookup"><span data-stu-id="df094-199">For ParameterInit elements with integer or decimal values, the value of the ParameterInit should be a multiple of this number.</span></span> <span data-ttu-id="df094-200">Например, элементы Параметеринит с десятичным значением могут быть ограничены десятыми значениями, присвоив этому свойству значение 0,1.</span><span class="sxs-lookup"><span data-stu-id="df094-200">For example, decimal-valued ParameterInit elements can be limited to tenths by setting this property to 0.1.</span></span> <span data-ttu-id="df094-201">Элементы пользовательского интерфейса используют это свойство при создании диалоговых окон и элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="df094-201">UI elements use this Property when they construct dialogs and UI controls.</span></span> <span data-ttu-id="df094-202">Кроме того, код проверки PrintTicket может использовать это свойство для округления значения Параметеринит до ближайшего значения, указанного кратным.</span><span class="sxs-lookup"><span data-stu-id="df094-202">In addition, PrintTicket validation code can use this Property to round the value of a ParameterInit to the nearest value indicated by Multiple.</span></span> <span data-ttu-id="df094-203">Примечание. драйверы устройств и поставщики PrintCapabilities не должны считать, что значения Параметеринит являются кратными значениям этого свойства.</span><span class="sxs-lookup"><span data-stu-id="df094-203">Note: Device drivers and PrintCapabilities providers should not assume that ParameterInit values are multiples of this Property value.</span></span> <span data-ttu-id="df094-204">Каждый поставщик должен иметь возможность округлять произвольные значения до ближайшего доступного значения из-за того, что разные поставщики могут задавать разные и конфликтующие значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="df094-204">Each provider must be able to round arbitrary values to the nearest useable value due to the possibility that different providers might specify different and conflicting values for this property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df094-205">См. также</span><span class="sxs-lookup"><span data-stu-id="df094-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df094-206">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="df094-206">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




