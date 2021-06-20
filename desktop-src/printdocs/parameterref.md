---
description: Сведения об элементе ParameterRef, который определяет ссылку на элемент Параметеринит и о том, как он работает с Скоредпроперти.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407187"
---
# <a name="parameterref"></a><span data-ttu-id="bbaef-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="bbaef-103">ParameterRef</span></span>

<span data-ttu-id="bbaef-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="bbaef-104">This topic is not current.</span></span> <span data-ttu-id="bbaef-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bbaef-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bbaef-106">Элемент ParameterRef определяет ссылку на элемент Параметеринит.</span><span class="sxs-lookup"><span data-stu-id="bbaef-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="bbaef-107">Элемент Скоредпроперти, содержащий элемент ParameterRef, не имеет явно заданного элемента value.</span><span class="sxs-lookup"><span data-stu-id="bbaef-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="bbaef-108">Вместо этого элемент Скоредпроперти получает свое значение из элемента Параметеринит, на который ссылается элемент ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="bbaef-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="bbaef-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="bbaef-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="bbaef-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="bbaef-110">XML Attributes</span></span>

<span data-ttu-id="bbaef-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="bbaef-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="bbaef-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="bbaef-112">XML Attribute</span></span>   | <span data-ttu-id="bbaef-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="bbaef-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaef-114">name</span><span class="sxs-lookup"><span data-stu-id="bbaef-114">name</span></span><br/> | <span data-ttu-id="bbaef-115">Содержит атрибут Name элемента Параметердеф, на который имеется ссылка в контексте текущего документа.</span><span class="sxs-lookup"><span data-stu-id="bbaef-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="bbaef-116">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaef-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="bbaef-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bbaef-117">Element Information</span></span>

<span data-ttu-id="bbaef-118">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="bbaef-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="bbaef-119">Категория</span><span class="sxs-lookup"><span data-stu-id="bbaef-119">Category</span></span>                   | <span data-ttu-id="bbaef-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="bbaef-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaef-121">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bbaef-121">Parent elements</span></span><br/> | <span data-ttu-id="bbaef-122">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="bbaef-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="bbaef-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bbaef-123">Child elements</span></span><br/>  | <span data-ttu-id="bbaef-124">Нет разрешенных.</span><span class="sxs-lookup"><span data-stu-id="bbaef-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="bbaef-125">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="bbaef-125">This element</span></span><br/>    | <span data-ttu-id="bbaef-126">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="bbaef-126">No character data is permitted.</span></span><br/> <span data-ttu-id="bbaef-127">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="bbaef-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="bbaef-128">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="bbaef-128">Configuration Dependencies</span></span>

<span data-ttu-id="bbaef-129">Элементы ParameterRef не могут иметь зависимости конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bbaef-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="bbaef-130">Пример</span><span class="sxs-lookup"><span data-stu-id="bbaef-130">Example</span></span>

<span data-ttu-id="bbaef-131">В следующем примере показано, как использовать элементы ParameterRef, чтобы пользователи могли вводить пользовательские параметры размера носителя.</span><span class="sxs-lookup"><span data-stu-id="bbaef-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bbaef-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bbaef-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbaef-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="bbaef-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




