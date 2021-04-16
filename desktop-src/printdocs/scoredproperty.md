---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 0552d301-5105-490f-962b-135c8c2e936b
title: скоредпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1605d173e0ab311841a6fcc37a46a0ba3b59b005
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720825"
---
# <a name="scoredproperty"></a><span data-ttu-id="9b227-104">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="9b227-104">ScoredProperty</span></span>

<span data-ttu-id="9b227-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="9b227-105">This topic is not current.</span></span> <span data-ttu-id="9b227-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9b227-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9b227-107">Элемент Скоредпроперти объявляет свойство, которое является встроенным для определения параметра.</span><span class="sxs-lookup"><span data-stu-id="9b227-107">A ScoredProperty element declares a property that is intrinsic to an Option definition.</span></span> <span data-ttu-id="9b227-108">Такие свойства следует сравнивать при оценке того, насколько близко запрошенный параметр соответствует параметру, поддерживаемому устройством.</span><span class="sxs-lookup"><span data-stu-id="9b227-108">Such properties should be compared when evaluating how closely a requested Option matches a device-supported Option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="9b227-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="9b227-109">Element Tag</span></span>

<ScoredProperty>

## <a name="xml-attributes"></a><span data-ttu-id="9b227-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="9b227-110">XML Attributes</span></span>

<span data-ttu-id="9b227-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="9b227-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="9b227-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="9b227-112">XML Attribute</span></span>   | <span data-ttu-id="9b227-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="9b227-113">Details</span></span>                                                                                                                 |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b227-114">name</span><span class="sxs-lookup"><span data-stu-id="9b227-114">name</span></span><br/> | <span data-ttu-id="9b227-115">Содержит атрибут Name Скоредпроперти, стандартного свойства или закрытого свойства.</span><span class="sxs-lookup"><span data-stu-id="9b227-115">Holds the name attribute of the ScoredProperty, either a standard property or a privately-defined property.</span></span> <br/> |



 

<span data-ttu-id="9b227-116">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="9b227-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="9b227-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9b227-117">Element Information</span></span>

<span data-ttu-id="9b227-118">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="9b227-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="9b227-119">Категория</span><span class="sxs-lookup"><span data-stu-id="9b227-119">Category</span></span>                   | <span data-ttu-id="9b227-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="9b227-120">Details</span></span>                                                                                                                                                                  |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b227-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9b227-121">Parent elements</span></span><br/> | <span data-ttu-id="9b227-122">*Параметр*</span><span class="sxs-lookup"><span data-stu-id="9b227-122">*Option*</span></span><br/> <span data-ttu-id="9b227-123">*скоредпроперти*</span><span class="sxs-lookup"><span data-stu-id="9b227-123">*ScoredProperty*</span></span><br/>                                                                                                                          |
| <span data-ttu-id="9b227-124">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9b227-124">Child elements</span></span><br/>  | <span data-ttu-id="9b227-125">Можно использовать</span><span class="sxs-lookup"><span data-stu-id="9b227-125">Either</span></span><br/> <span data-ttu-id="9b227-126">*ParameterRef* (один)</span><span class="sxs-lookup"><span data-stu-id="9b227-126">*ParameterRef* (one)</span></span><br/> <span data-ttu-id="9b227-127">или</span><span class="sxs-lookup"><span data-stu-id="9b227-127">or</span></span><br/> <span data-ttu-id="9b227-128">*Значение* (одно)</span><span class="sxs-lookup"><span data-stu-id="9b227-128">*Value* (one)</span></span><br/> <span data-ttu-id="9b227-129">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="9b227-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="9b227-130">*Скоредпроперти* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="9b227-130">*ScoredProperty* (zero or more)</span></span><br/> |
| <span data-ttu-id="9b227-131">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="9b227-131">This element</span></span><br/>    | <span data-ttu-id="9b227-132">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="9b227-132">No character data is permitted.</span></span><br/> <span data-ttu-id="9b227-133">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="9b227-133">Duplicate child siblings are not permitted.</span></span><br/>                                                                        |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="9b227-134">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="9b227-134">Configuration Dependencies</span></span>

<span data-ttu-id="9b227-135">Элемент Скоредпроперти не может иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9b227-135">A ScoredProperty element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="9b227-136">Пример</span><span class="sxs-lookup"><span data-stu-id="9b227-136">Example</span></span>

<span data-ttu-id="9b227-137">Объявите элемент Скоредпроперти с именем Медиасизевидс и значением 11.</span><span class="sxs-lookup"><span data-stu-id="9b227-137">Declare a ScoredProperty element named MediaSizeWidth with a Value of 11.</span></span>

``` syntax
<psf:ScoredProperty name="psk:MediaSizeWidth">
   <psf:Value xsi:type="integer">11</psf:Value>
</psf:ScoredProperty>
```

## <a name="related-topics"></a><span data-ttu-id="9b227-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9b227-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b227-139">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="9b227-139">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




