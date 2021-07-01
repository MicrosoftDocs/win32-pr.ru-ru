---
description: Найдите сведения об элементе Скоредпроперти. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: скоредпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb93fbdaeb6101cbd1ff75d6c0b3a829afe0d317
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119119"
---
# <a name="scoredproperty"></a><span data-ttu-id="2eaef-105">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="2eaef-105">ScoredProperty</span></span>

<span data-ttu-id="2eaef-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2eaef-106">This topic is not current.</span></span> <span data-ttu-id="2eaef-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2eaef-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2eaef-108">Элемент Скоредпроперти объявляет свойство, которое является встроенным для определения параметра.</span><span class="sxs-lookup"><span data-stu-id="2eaef-108">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="2eaef-109">Такие свойства следует сравнивать при оценке того, насколько близко запрошенный параметр соответствует параметру, поддерживаемому устройством.</span><span class="sxs-lookup"><span data-stu-id="2eaef-109">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="2eaef-110">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="2eaef-110">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="2eaef-111">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="2eaef-111">XML Attributes</span></span>

<span data-ttu-id="2eaef-112">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="2eaef-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="2eaef-113">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="2eaef-113">XML Attribute</span></span>   | <span data-ttu-id="2eaef-114">Сведения</span><span class="sxs-lookup"><span data-stu-id="2eaef-114">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eaef-115">name</span><span class="sxs-lookup"><span data-stu-id="2eaef-115">name</span></span><br/> | <span data-ttu-id="2eaef-116">Содержит атрибут Name Скоредпроперти, стандартного свойства или закрытого свойства.</span><span class="sxs-lookup"><span data-stu-id="2eaef-116">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="2eaef-117">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="2eaef-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="2eaef-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2eaef-118">Element Information</span></span>

<span data-ttu-id="2eaef-119">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="2eaef-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="2eaef-120">Категория</span><span class="sxs-lookup"><span data-stu-id="2eaef-120">Category</span></span>                   | <span data-ttu-id="2eaef-121">Сведения</span><span class="sxs-lookup"><span data-stu-id="2eaef-121">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eaef-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2eaef-122">Parent elements</span></span><br/> | <span data-ttu-id="2eaef-123">*Параметр*</span><span class="sxs-lookup"><span data-stu-id="2eaef-123">*Option*</span></span><br/> <span data-ttu-id="2eaef-124">*скоредпроперти*</span><span class="sxs-lookup"><span data-stu-id="2eaef-124">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="2eaef-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2eaef-125">Child elements</span></span><br/>  | <span data-ttu-id="2eaef-126">Можно использовать</span><span class="sxs-lookup"><span data-stu-id="2eaef-126">Either</span></span><br/> <span data-ttu-id="2eaef-127">*ParameterRef* (один)</span><span class="sxs-lookup"><span data-stu-id="2eaef-127">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="2eaef-128">или</span><span class="sxs-lookup"><span data-stu-id="2eaef-128">or</span></span><br/> <span data-ttu-id="2eaef-129">*Значение* (одно)</span><span class="sxs-lookup"><span data-stu-id="2eaef-129">*Value* (one)</span></span><br/> <span data-ttu-id="2eaef-130">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="2eaef-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="2eaef-131">*Скоредпроперти* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="2eaef-131">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="2eaef-132">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="2eaef-132">This element</span></span><br/>    | <span data-ttu-id="2eaef-133">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="2eaef-133">No character data is permitted.</span></span><br/> <span data-ttu-id="2eaef-134">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="2eaef-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="2eaef-135">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="2eaef-135">Configuration Dependencies</span></span>

<span data-ttu-id="2eaef-136">Элемент Скоредпроперти не может иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2eaef-136">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="2eaef-137">Пример</span><span class="sxs-lookup"><span data-stu-id="2eaef-137">Example</span></span>

<span data-ttu-id="2eaef-138">Объявите элемент Скоредпроперти с именем Медиасизевидс и значением 11.</span><span class="sxs-lookup"><span data-stu-id="2eaef-138">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="2eaef-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2eaef-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eaef-140">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2eaef-140">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




