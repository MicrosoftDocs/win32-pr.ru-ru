---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713327"
---
# <a name="parameterref"></a><span data-ttu-id="dae79-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="dae79-104">ParameterRef</span></span>

<span data-ttu-id="dae79-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="dae79-105">This topic is not current.</span></span> <span data-ttu-id="dae79-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dae79-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dae79-107">Элемент ParameterRef определяет ссылку на элемент Параметеринит.</span><span class="sxs-lookup"><span data-stu-id="dae79-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="dae79-108">Элемент Скоредпроперти, содержащий элемент ParameterRef, не имеет явно заданного элемента value.</span><span class="sxs-lookup"><span data-stu-id="dae79-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="dae79-109">Вместо этого элемент Скоредпроперти получает свое значение из элемента Параметеринит, на который ссылается элемент ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="dae79-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="dae79-110">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="dae79-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="dae79-111">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="dae79-111">XML Attributes</span></span>

<span data-ttu-id="dae79-112">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="dae79-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="dae79-113">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="dae79-113">XML Attribute</span></span>   | <span data-ttu-id="dae79-114">Сведения</span><span class="sxs-lookup"><span data-stu-id="dae79-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae79-115">name</span><span class="sxs-lookup"><span data-stu-id="dae79-115">name</span></span><br/> | <span data-ttu-id="dae79-116">Содержит атрибут Name элемента Параметердеф, на который имеется ссылка в контексте текущего документа.</span><span class="sxs-lookup"><span data-stu-id="dae79-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="dae79-117">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="dae79-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="dae79-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dae79-118">Element Information</span></span>

<span data-ttu-id="dae79-119">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="dae79-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="dae79-120">Категория</span><span class="sxs-lookup"><span data-stu-id="dae79-120">Category</span></span>                   | <span data-ttu-id="dae79-121">Сведения</span><span class="sxs-lookup"><span data-stu-id="dae79-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae79-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dae79-122">Parent elements</span></span><br/> | <span data-ttu-id="dae79-123">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="dae79-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="dae79-124">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dae79-124">Child elements</span></span><br/>  | <span data-ttu-id="dae79-125">Нет разрешенных.</span><span class="sxs-lookup"><span data-stu-id="dae79-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="dae79-126">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="dae79-126">This element</span></span><br/>    | <span data-ttu-id="dae79-127">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="dae79-127">No character data is permitted.</span></span><br/> <span data-ttu-id="dae79-128">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="dae79-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="dae79-129">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="dae79-129">Configuration Dependencies</span></span>

<span data-ttu-id="dae79-130">Элементы ParameterRef не могут иметь зависимости конфигурации.</span><span class="sxs-lookup"><span data-stu-id="dae79-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="dae79-131">Пример</span><span class="sxs-lookup"><span data-stu-id="dae79-131">Example</span></span>

<span data-ttu-id="dae79-132">В следующем примере показано, как использовать элементы ParameterRef, чтобы пользователи могли вводить пользовательские параметры размера носителя.</span><span class="sxs-lookup"><span data-stu-id="dae79-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="dae79-133">См. также</span><span class="sxs-lookup"><span data-stu-id="dae79-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae79-134">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="dae79-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




