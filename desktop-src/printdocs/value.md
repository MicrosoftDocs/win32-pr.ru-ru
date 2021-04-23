---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Значение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105651242"
---
# <a name="value"></a><span data-ttu-id="5afb9-104">Значение</span><span class="sxs-lookup"><span data-stu-id="5afb9-104">Value</span></span>

<span data-ttu-id="5afb9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5afb9-105">This topic is not current.</span></span> <span data-ttu-id="5afb9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5afb9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5afb9-107">Элемент value связывает литерал с типом.</span><span class="sxs-lookup"><span data-stu-id="5afb9-107">A Value element associates a literal with a type.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5afb9-108">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="5afb9-108">Element Tag</span></span>

<Value>

## <a name="xml-attributes"></a><span data-ttu-id="5afb9-109">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="5afb9-109">XML Attributes</span></span>

<span data-ttu-id="5afb9-110">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="5afb9-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5afb9-111">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="5afb9-111">XML Attribute</span></span>       | <span data-ttu-id="5afb9-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="5afb9-112">Details</span></span>                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5afb9-113">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5afb9-113">xsi:type</span></span><br/> | <span data-ttu-id="5afb9-114">Задает тип данных value, который должен быть одним из следующих типов, определенных XSD: строка, целое число, десятичное, QName.</span><span class="sxs-lookup"><span data-stu-id="5afb9-114">Specifies the data type of Value, which must be one of the following XSD-defined types: string, integer, decimal, QName.</span></span> <span data-ttu-id="5afb9-115">Если он отсутствует, типом данных по умолчанию является String.</span><span class="sxs-lookup"><span data-stu-id="5afb9-115">If missing, the default data type is string.</span></span><br/> |



 

<span data-ttu-id="5afb9-116">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5afb9-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5afb9-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5afb9-117">Element Information</span></span>

<span data-ttu-id="5afb9-118">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="5afb9-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5afb9-119">Категория</span><span class="sxs-lookup"><span data-stu-id="5afb9-119">Category</span></span>                   | <span data-ttu-id="5afb9-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="5afb9-120">Details</span></span>                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5afb9-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5afb9-121">Parent elements</span></span><br/> | <span data-ttu-id="5afb9-122">параметеринит</span><span class="sxs-lookup"><span data-stu-id="5afb9-122">ParameterInit</span></span> <br/> <span data-ttu-id="5afb9-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="5afb9-123">Property</span></span><br/> <span data-ttu-id="5afb9-124">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="5afb9-124">ScoredProperty</span></span><br/>                                                                                   |
| <span data-ttu-id="5afb9-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5afb9-125">Child elements</span></span><br/>  | <span data-ttu-id="5afb9-126">Допускается только символьное или целочисленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="5afb9-126">Only character or integer content is permitted.</span></span><br/>                                                                                                |
| <span data-ttu-id="5afb9-127">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="5afb9-127">This element</span></span><br/>    | <span data-ttu-id="5afb9-128">Разрешено содержимое null.</span><span class="sxs-lookup"><span data-stu-id="5afb9-128">Null content is allowed.</span></span> <span data-ttu-id="5afb9-129">Символьное содержимое должно соответствовать синтаксису, определяемому типом данных.</span><span class="sxs-lookup"><span data-stu-id="5afb9-129">Character content must conform to syntax defined by data type.</span></span><br/> <span data-ttu-id="5afb9-130">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="5afb9-130">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5afb9-131">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="5afb9-131">Configuration Dependencies</span></span>

<span data-ttu-id="5afb9-132">Элементы значения, отображаемые в элементе Скоредпроперти, могут не иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5afb9-132">Value elements that appear within ScoredProperty element may not have any configuration dependencies.</span></span> <span data-ttu-id="5afb9-133">Элементы значений, которые отображаются в элементах свойств, могут иметь произвольную зависимость от конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5afb9-133">Value elements that appear within Property elements may have arbitrary dependencies on the configuration.</span></span>

## <a name="element-usage"></a><span data-ttu-id="5afb9-134">Использование элементов</span><span class="sxs-lookup"><span data-stu-id="5afb9-134">Element Usage</span></span>

<span data-ttu-id="5afb9-135">Элемент value может присутствовать в свойстве или элементе Скоредпроперти.</span><span class="sxs-lookup"><span data-stu-id="5afb9-135">A Value element may appear within a Property or ScoredProperty element.</span></span> <span data-ttu-id="5afb9-136">Целью элемента value является представление значения как стандартного типа данных XML.</span><span class="sxs-lookup"><span data-stu-id="5afb9-136">The purpose of the Value element is to represent a value as a standard XML data type.</span></span> <span data-ttu-id="5afb9-137">Тип данных указывается как XML-атрибут элемента value, xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="5afb9-137">The data type is specified as an XML attribute of the Value element, xsi:type.</span></span> <span data-ttu-id="5afb9-138">Обратите внимание, что поддерживаются не все определяемые XSD или XML-типы.</span><span class="sxs-lookup"><span data-stu-id="5afb9-138">Note that not all XSD-defined or XML-defined types are supported.</span></span> <span data-ttu-id="5afb9-139">Список поддерживаемых типов см. в разделе [Сводка по типам элементов](summary-of-element-types.md).</span><span class="sxs-lookup"><span data-stu-id="5afb9-139">For a list of supported types, see [Summary of Element Types](summary-of-element-types.md).</span></span> <span data-ttu-id="5afb9-140">Элемент value может содержать только символьное содержимое.</span><span class="sxs-lookup"><span data-stu-id="5afb9-140">A Value element can contain only character content.</span></span> <span data-ttu-id="5afb9-141">Другие элементы не могут отображаться как содержимое в элементе value.</span><span class="sxs-lookup"><span data-stu-id="5afb9-141">Nothing else may appear as content in a Value element.</span></span>

> [!Note]  
> <span data-ttu-id="5afb9-142">Некоторые свойства и элементы Скоредпроперти, определяемые схемой печати, не содержат элемент value, поскольку их назначение просто является родителями вложенных свойств.</span><span class="sxs-lookup"><span data-stu-id="5afb9-142">Some Print Schema-defined Property and ScoredProperty elements do not contain a Value element, because their purpose is simply to be parents of subproperties.</span></span> <span data-ttu-id="5afb9-143">Не следует добавлять элемент value в такие свойства, как свойства, которые не содержат элемент value.</span><span class="sxs-lookup"><span data-stu-id="5afb9-143">You should not add a Value element to such properties as these, properties that do not contain a Value element.</span></span>

 

<span data-ttu-id="5afb9-144">Чтобы обеспечить соответствие платформе схемы печати, которая требует, чтобы элемент value или вложенные элементы присутствовали в элементах, поддерживающих значения, отсутствующее или неопределенное значение должно быть представлено представлением элемента value как пустого элемента. то есть, как</span><span class="sxs-lookup"><span data-stu-id="5afb9-144">To conform to the Print Schema Framework, which requires either a Value element or subelements be present in the elements that support values, an absent or undefined value should be represented by presenting the Value element as an empty element; that is, as</span></span> <Value></Value><span data-ttu-id="5afb9-145">.</span><span class="sxs-lookup"><span data-stu-id="5afb9-145">.</span></span>

## <a name="example"></a><span data-ttu-id="5afb9-146">Пример</span><span class="sxs-lookup"><span data-stu-id="5afb9-146">Example</span></span>

<span data-ttu-id="5afb9-147">Определите значение типа Decimal и инициализируйте его значением "128,5".</span><span class="sxs-lookup"><span data-stu-id="5afb9-147">Define a Value of type decimal and initialize it to "128.5".</span></span>

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a><span data-ttu-id="5afb9-148">См. также</span><span class="sxs-lookup"><span data-stu-id="5afb9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5afb9-149">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5afb9-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




