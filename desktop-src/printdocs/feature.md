---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Функция
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703518"
---
# <a name="feature"></a><span data-ttu-id="439ed-104">Функция</span><span class="sxs-lookup"><span data-stu-id="439ed-104">Feature</span></span>

<span data-ttu-id="439ed-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="439ed-105">This topic is not current.</span></span> <span data-ttu-id="439ed-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="439ed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="439ed-107">Элемент Feature содержит полный список элементов параметров и свойств, которые полностью описывают атрибут устройства, параметр форматирования задания или другие соответствующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="439ed-107">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="439ed-108">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="439ed-108">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="439ed-109">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="439ed-109">XML Attributes</span></span>

<span data-ttu-id="439ed-110">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="439ed-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="439ed-111">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="439ed-111">XML Attribute</span></span>   | <span data-ttu-id="439ed-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="439ed-112">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="439ed-113">name</span><span class="sxs-lookup"><span data-stu-id="439ed-113">name</span></span><br/> | <span data-ttu-id="439ed-114">Содержит имя функции, стандартной или закрытой функции.</span><span class="sxs-lookup"><span data-stu-id="439ed-114">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="439ed-115">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="439ed-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="439ed-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="439ed-116">Element Information</span></span>

<span data-ttu-id="439ed-117">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="439ed-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="439ed-118">Категория</span><span class="sxs-lookup"><span data-stu-id="439ed-118">Category</span></span></th>
<th><span data-ttu-id="439ed-119">Сведения</span><span class="sxs-lookup"><span data-stu-id="439ed-119">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="439ed-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="439ed-120">Parent elements</span></span><br/></td>
<td><span data-ttu-id="439ed-121">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="439ed-121">PrintCapabilities</span></span> <br/> <span data-ttu-id="439ed-122">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="439ed-122">PrintTicket</span></span> <br/> <span data-ttu-id="439ed-123">Функция</span><span class="sxs-lookup"><span data-stu-id="439ed-123">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="439ed-124">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="439ed-124">Child elements</span></span><br/></td>
<td><span data-ttu-id="439ed-125">Одна из следующих групп:</span><span class="sxs-lookup"><span data-stu-id="439ed-125">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="439ed-126"><em>Функция</em> (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="439ed-126"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="439ed-127"><em>Параметр</em> (один или более)</span><span class="sxs-lookup"><span data-stu-id="439ed-127"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="439ed-128"><em>Свойство</em> (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="439ed-128"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="439ed-129">или</span><span class="sxs-lookup"><span data-stu-id="439ed-129">or</span></span> <br/>
<ul>
<li><span data-ttu-id="439ed-130"><em>Функция</em> (одна или несколько)</span><span class="sxs-lookup"><span data-stu-id="439ed-130"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="439ed-131"><em>Параметр</em> (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="439ed-131"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="439ed-132"><em>Свойство</em> (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="439ed-132"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="439ed-133">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="439ed-133">This element</span></span><br/></td>
<td><span data-ttu-id="439ed-134">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="439ed-134">No character data is permitted.</span></span><br/> <span data-ttu-id="439ed-135">Допускаются дублирующиеся дочерние элементы Option, являющиеся одноуровневыми элементами.</span><span class="sxs-lookup"><span data-stu-id="439ed-135">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="439ed-136">Разрешены ярлыки атрибутов повторяющихся имен.</span><span class="sxs-lookup"><span data-stu-id="439ed-136">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="439ed-137">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="439ed-137">Configuration Dependencies</span></span>

<span data-ttu-id="439ed-138">Элементы компонента могут не иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="439ed-138">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="439ed-139">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="439ed-139">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="439ed-140">Связь с XML-атрибутами</span><span class="sxs-lookup"><span data-stu-id="439ed-140">Relationship to XML Attributes</span></span>

<span data-ttu-id="439ed-141">В представлении "функция-параметр" атрибут устройства представлен элементом Feature.</span><span class="sxs-lookup"><span data-stu-id="439ed-141">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="439ed-142">Атрибут Device однозначно идентифицируется атрибутом Name в элементе Feature атрибута устройства, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="439ed-142">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="439ed-143">В этом примере атрибут устройства имеет разрешение.</span><span class="sxs-lookup"><span data-stu-id="439ed-143">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="439ed-144">Схема печати определяет набор атрибутов имени для определенных экземпляров компонента.</span><span class="sxs-lookup"><span data-stu-id="439ed-144">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="439ed-145">Эти атрибуты имени служат для того, чтобы определить набор предварительно определенных экземпляров компонента, связанных с определенными настраиваемыми атрибутами устройства.</span><span class="sxs-lookup"><span data-stu-id="439ed-145">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="439ed-146">Эти имена экземпляров компонентов следует использовать всякий раз, когда они применимы, так как они увеличивают переносимость документа PrintCapabilities и PrintTicket, полученные от них.</span><span class="sxs-lookup"><span data-stu-id="439ed-146">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="439ed-147">Закрыто определенные экземпляры компонентов могут быть введены, если определенные атрибуты устройства не соответствуют ни одному из экземпляров компонента, определяемых схемой.</span><span class="sxs-lookup"><span data-stu-id="439ed-147">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="439ed-148">Сведения о синтаксисе атрибутов имени и соглашениях, которые применяются к определяемым схемой и частным именам, см. в разделе [атрибуты XML](xml-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="439ed-148">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="439ed-149">Связь с элементом параметра</span><span class="sxs-lookup"><span data-stu-id="439ed-149">Relationship to Option Element</span></span>

<span data-ttu-id="439ed-150">Каждое из возможных состояний представлено элементом Option.</span><span class="sxs-lookup"><span data-stu-id="439ed-150">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="439ed-151">Каждое определение параметра содержит один или несколько элементов Скоредпроперти, которые вместе однозначно описывают или характеризуют представленное состояние.</span><span class="sxs-lookup"><span data-stu-id="439ed-151">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="439ed-152">Методика, используемая для создания определений параметров, описана в разделе [определения параметров](option-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="439ed-152">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="439ed-153">Все элементы Option, связанные с определенным элементом компонента, находятся в качестве дочерних элементов элемента Feature.</span><span class="sxs-lookup"><span data-stu-id="439ed-153">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="439ed-154">Его части</span><span class="sxs-lookup"><span data-stu-id="439ed-154">Subfeatures</span></span>

<span data-ttu-id="439ed-155">Платформа схемы печати также позволяет объединять элементы компонентов в иерархическую структуру.</span><span class="sxs-lookup"><span data-stu-id="439ed-155">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="439ed-156">То есть элемент Feature может сам содержать один или несколько дочерних элементов компонента (подкомпонентов).</span><span class="sxs-lookup"><span data-stu-id="439ed-156">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="439ed-157">Это может быть полезно для организации связанных элементов компонента или для элементов компонента, управляющих аспектами функции устройства.</span><span class="sxs-lookup"><span data-stu-id="439ed-157">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="439ed-158">Одним из примеров является устройство, которое поддерживает сшивание.</span><span class="sxs-lookup"><span data-stu-id="439ed-158">One example is a device that supports stapling.</span></span> <span data-ttu-id="439ed-159">Такое устройство может предложить пользователю выбрать место для размещения сшивания, например, в левом верхнем углу или в правом верхнем углу или на левом краю или вдоль левого края.</span><span class="sxs-lookup"><span data-stu-id="439ed-159">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="439ed-160">Пользовательский интерфейс для этого устройства должен иметь возможность предоставлять пользователю наиболее высокий уровень выбора, в этом случае следует использовать сшивание.</span><span class="sxs-lookup"><span data-stu-id="439ed-160">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="439ed-161">Только после того, как пользователь решил использовать сшивание, он должен быть представлен вторым вариантом выбора, скрепкой.</span><span class="sxs-lookup"><span data-stu-id="439ed-161">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="439ed-162">Иерархия функций добавляет дополнительную структуру, которая делает возможным такой пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="439ed-162">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="439ed-163">Платформа схемы печати позволяет подкомпонентам иметь собственные дочерние функции, тем самым разрешая Неограниченный уровень вложенности.</span><span class="sxs-lookup"><span data-stu-id="439ed-163">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="439ed-164">Платформа схемы печати также позволяет элементам параметров отображаться на том же уровне, что и подкомпоненты. то есть в качестве одноуровневых элементов в пределах одного родительского элемента Feature.</span><span class="sxs-lookup"><span data-stu-id="439ed-164">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="439ed-165">Это позволяет пользователю принять решение высокого уровня (использовать сшивание) перед выбором подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="439ed-165">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="439ed-166">В этом примере корневой элемент Feature, "степлер", может содержать два элемента параметров: "on" и "OFF", а также подфункции с именем "Стаплелокатион".</span><span class="sxs-lookup"><span data-stu-id="439ed-166">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="439ed-167">Пример</span><span class="sxs-lookup"><span data-stu-id="439ed-167">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="439ed-168">См. также</span><span class="sxs-lookup"><span data-stu-id="439ed-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439ed-169">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="439ed-169">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




