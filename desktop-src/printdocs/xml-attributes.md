---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML-атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105684826"
---
# <a name="xml-attributes"></a><span data-ttu-id="108ba-104">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="108ba-104">XML Attributes</span></span>

<span data-ttu-id="108ba-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="108ba-105">This topic is not current.</span></span> <span data-ttu-id="108ba-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="108ba-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="108ba-107">Существует ряд XML-атрибутов, которые отображаются в нескольких типах элементов, определенных в платформе схемы печати.</span><span class="sxs-lookup"><span data-stu-id="108ba-107">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="108ba-108">Атрибуты XML с одинаковыми именами обычно имеют одинаковое значение и подчиняются тем же правилам независимо от типа элемента, в котором они находятся.</span><span class="sxs-lookup"><span data-stu-id="108ba-108">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="108ba-109">Таким образом, XML-атрибуты перечисляются по имени, а не по типу элемента узла.</span><span class="sxs-lookup"><span data-stu-id="108ba-109">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="108ba-110">Закрытые атрибуты XML не допускаются.</span><span class="sxs-lookup"><span data-stu-id="108ba-110">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="108ba-111">Только определенные здесь XML-атрибуты могут использоваться в документе PrintCapabilities или PrintTicket, а затем только в определенном контексте.</span><span class="sxs-lookup"><span data-stu-id="108ba-111">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="108ba-112">Хотя частные лица не могут добавлять новые определения в пространство имен другого лица, им разрешено использовать существующие имена из другого закрытого пространства имен, если его использование согласуется с использованием, установленным другой стороной.</span><span class="sxs-lookup"><span data-stu-id="108ba-112">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="108ba-113">Таким же вариантом может быть элемент Скоредпроперти, определенный несколькими сторонами, каждый из которых размещается в разных пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="108ba-113">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="108ba-114">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="108ba-114">Attribute Name</span></span></th>
<th><span data-ttu-id="108ba-115">Типы и значения данных</span><span class="sxs-lookup"><span data-stu-id="108ba-115">Data Types and Values</span></span></th>
<th><span data-ttu-id="108ba-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="108ba-116">Purpose</span></span></th>
<th><span data-ttu-id="108ba-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="108ba-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="108ba-118">name</span><span class="sxs-lookup"><span data-stu-id="108ba-118">name</span></span> <br/></td>
<td><span data-ttu-id="108ba-119">XML QName</span><span class="sxs-lookup"><span data-stu-id="108ba-119">XML QName</span></span><br/></td>
<td><span data-ttu-id="108ba-120">Этот XML-атрибут определяет экземпляр элемента.</span><span class="sxs-lookup"><span data-stu-id="108ba-120">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="108ba-121">Он отличает один элемент от другого в том же типе элемента.</span><span class="sxs-lookup"><span data-stu-id="108ba-121">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="108ba-122">Этот атрибут XML широко используется, так как он называется атрибутом Name.</span><span class="sxs-lookup"><span data-stu-id="108ba-122">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="108ba-123">К атрибуту name относятся следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="108ba-123">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="108ba-124">Атрибут name должен иметь форму допустимого типа QName, определенного в XML.</span><span class="sxs-lookup"><span data-stu-id="108ba-124">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="108ba-125">То есть он должен уточняться допустимым пространством имен XML.</span><span class="sxs-lookup"><span data-stu-id="108ba-125">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="108ba-126">Имена QName, отображаемые в виде значений атрибутов имени, должны быть явно квалифицированы, даже если определено пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="108ba-126">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="108ba-127">Символьное содержимое должно иметь допустимый XML-определенный QName.</span><span class="sxs-lookup"><span data-stu-id="108ba-127">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="108ba-128">Закрыто определенные имена должны быть дополнены пространством имен, которое однозначно связано с стороной, в которой появился атрибут Name.</span><span class="sxs-lookup"><span data-stu-id="108ba-128">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="108ba-129">Требование уникальности одноуровневого элемента: ни один из двух родственных элементов, принадлежащих одному и тому же типу, не может иметь одинаковый атрибут Name.</span><span class="sxs-lookup"><span data-stu-id="108ba-129">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="108ba-130">Единственным исключением являются элементы параметров, где атрибут Name может использоваться для определения параметра.</span><span class="sxs-lookup"><span data-stu-id="108ba-130">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="108ba-131">Поэтому одноуровневые элементы параметров могут иметь одинаковый атрибут Name.</span><span class="sxs-lookup"><span data-stu-id="108ba-131">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="108ba-132">Следующие типы элементов могут содержать атрибуты Name: Property, Скоредпроперти, Параметердеф, Option и Feature.</span><span class="sxs-lookup"><span data-stu-id="108ba-132">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="108ba-133">атрибуты имени должны присутствовать в каждом из типов элементов, содержащих их, за исключением некоторых ранее определенных элементов параметров общей схемы печати, таких как Документнуп.</span><span class="sxs-lookup"><span data-stu-id="108ba-133">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="108ba-134">В следующем примере показано, как задать экземпляр параметра с помощью атрибута "Name".</span><span class="sxs-lookup"><span data-stu-id="108ba-134">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="108ba-135">Это правильный способ определения элементов параметров.</span><span class="sxs-lookup"><span data-stu-id="108ba-135">This is the correct way to define Option elements.</span></span> <span data-ttu-id="108ba-136">Поставщик не должен иметь безымянных параметров, если они не определены в схеме печати, например Документнуп.</span><span class="sxs-lookup"><span data-stu-id="108ba-136">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="108ba-137">распространения</span><span class="sxs-lookup"><span data-stu-id="108ba-137">propagate</span></span> <br/></td>
<td><span data-ttu-id="108ba-138">Перечисление</span><span class="sxs-lookup"><span data-stu-id="108ba-138">Enumeration</span></span><br/> <span data-ttu-id="108ba-139">В настоящее время значения не определены.</span><span class="sxs-lookup"><span data-stu-id="108ba-139">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="108ba-140">Атрибут Propagate не используется в начальной версии платформы схемы печати.</span><span class="sxs-lookup"><span data-stu-id="108ba-140">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="108ba-141">Он описан здесь, чтобы код проверки PrintCapabilities или PrintTicket, реализованный для начальной версии платформы схемы печати, мог обрабатывать любые последующие версии схемы без ошибок.</span><span class="sxs-lookup"><span data-stu-id="108ba-141">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="108ba-142">ограниченного</span><span class="sxs-lookup"><span data-stu-id="108ba-142">constrained</span></span> <br/></td>
<td><span data-ttu-id="108ba-143">Перечисление</span><span class="sxs-lookup"><span data-stu-id="108ba-143">Enumeration</span></span><br/> <span data-ttu-id="108ba-144">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="108ba-144">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="108ba-145">Нет</span><span class="sxs-lookup"><span data-stu-id="108ba-145">None</span></span> <br/></li>
<li><span data-ttu-id="108ba-146">принттиккетсеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-146">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="108ba-147">админсеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-147">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="108ba-148">девицесеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-148">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="108ba-149">Указывает, доступен ли параметр для выбора или для использования.</span><span class="sxs-lookup"><span data-stu-id="108ba-149">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="108ba-150">Разрешенные значения атрибута CONSTRAINED имеют следующие значения.</span><span class="sxs-lookup"><span data-stu-id="108ba-150">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="108ba-151">Обратите внимание, что эти значения перечислены по порядку, от минимально ограниченного (None) до наиболее ограниченного (Девицесеттингс).</span><span class="sxs-lookup"><span data-stu-id="108ba-151">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="108ba-152">Нет</span><span class="sxs-lookup"><span data-stu-id="108ba-152">None</span></span> <br/>
<ul>
<li><span data-ttu-id="108ba-153">Параметр не ограничен.</span><span class="sxs-lookup"><span data-stu-id="108ba-153">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="108ba-154">принттиккетсеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-154">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="108ba-155">Параметр ограничен параметрами PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="108ba-155">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="108ba-156">Это означает, что изменение конфигурации может удалить ограничение.</span><span class="sxs-lookup"><span data-stu-id="108ba-156">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="108ba-157">админсеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-157">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="108ba-158">Параметр ограничен параметрами администратора; Параметр не может быть включен пользователем.</span><span class="sxs-lookup"><span data-stu-id="108ba-158">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="108ba-159">девицесеттингс</span><span class="sxs-lookup"><span data-stu-id="108ba-159">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="108ba-160">Параметр ограничен параметрами устройства или физически установленным устройством. Этот параметр нельзя включить ни пользователем, ни администратором.</span><span class="sxs-lookup"><span data-stu-id="108ba-160">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="108ba-161">Когда поставщик PrintCapabilities сообщает значения атрибута CONSTRAINED, необходимо сообщить о самом ограниченном ограничении.</span><span class="sxs-lookup"><span data-stu-id="108ba-161">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="108ba-162">Например, если параметр ограничен как параметром администратора, так и параметром устройства, поставщик PrintCapabilities должен сообщить о Девицесеттингс.</span><span class="sxs-lookup"><span data-stu-id="108ba-162">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="108ba-163">xmlns</span><span class="sxs-lookup"><span data-stu-id="108ba-163">xmlns</span></span> <br/></td>
<td><span data-ttu-id="108ba-164">URI</span><span class="sxs-lookup"><span data-stu-id="108ba-164">URI</span></span><br/></td>
<td><span data-ttu-id="108ba-165">Этот XML-атрибут устанавливает связь между универсальным идентификатором ресурса (URI) пространства имен и префиксом пространства имен, который отображается в XML QName.</span><span class="sxs-lookup"><span data-stu-id="108ba-165">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="108ba-166">Необходимо установить такую ссылку на URI пространства имен, определенный для платформы печати схемы, прежде чем можно будет использовать какие-либо теги элементов, атрибуты, атрибуты имени и т. д.</span><span class="sxs-lookup"><span data-stu-id="108ba-166">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="108ba-167">Можно объявить это пространство имен по умолчанию, чтобы избежать фактического уточнения тегов элементов префиксом пространства имен, хотя все остальные QName должны быть определены явно.</span><span class="sxs-lookup"><span data-stu-id="108ba-167">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="108ba-168">Стандартное пространство имен должно быть определено в соответствующем корневом элементе.</span><span class="sxs-lookup"><span data-stu-id="108ba-168">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="108ba-169">Обратите внимание на все правила и соглашения XML, касающиеся использования атрибута xmlns.</span><span class="sxs-lookup"><span data-stu-id="108ba-169">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="108ba-170">Универсальный код ресурса (URI) для платформы схемы печати — http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="108ba-170">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="108ba-171">URI для ключевых слов схемы Print имеет значение https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="108ba-171">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="108ba-172">См. также</span><span class="sxs-lookup"><span data-stu-id="108ba-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="108ba-173">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="108ba-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




