---
description: Сведения об элементе Параметеринит, который определяет значение для экземпляра элемента Параметердеф.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: параметеринит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211fcad2c53824c7786850a7fc78c6825c219a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407267"
---
# <a name="parameterinit"></a><span data-ttu-id="148c1-103">параметеринит</span><span class="sxs-lookup"><span data-stu-id="148c1-103">ParameterInit</span></span>

<span data-ttu-id="148c1-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="148c1-104">This topic is not current.</span></span> <span data-ttu-id="148c1-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="148c1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="148c1-106">Определяет значение для экземпляра элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="148c1-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="148c1-107">Элемент Параметеринит является целевым объектом ссылки, созданной элементом ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="148c1-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="148c1-108">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="148c1-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="148c1-109">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="148c1-109">XML Attributes</span></span>

<span data-ttu-id="148c1-110">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="148c1-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="148c1-111">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="148c1-111">XML Attribute</span></span>   | <span data-ttu-id="148c1-112">Сведения</span><span class="sxs-lookup"><span data-stu-id="148c1-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148c1-113">name</span><span class="sxs-lookup"><span data-stu-id="148c1-113">name</span></span><br/> | <span data-ttu-id="148c1-114">Содержит атрибут Name элемента Параметердеф, который должен быть инициализирован в контексте текущего документа.</span><span class="sxs-lookup"><span data-stu-id="148c1-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="148c1-115">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="148c1-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="148c1-116">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="148c1-116">Element Information</span></span>

<span data-ttu-id="148c1-117">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="148c1-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="148c1-118">Категория</span><span class="sxs-lookup"><span data-stu-id="148c1-118">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148c1-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="148c1-119">Parent elements</span></span><br/> | <span data-ttu-id="148c1-120">PrintTicket (корневой элемент PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="148c1-120">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="148c1-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="148c1-121">Child elements</span></span><br/>  | <span data-ttu-id="148c1-122">Значение (одно)</span><span class="sxs-lookup"><span data-stu-id="148c1-122">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="148c1-123">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="148c1-123">This element</span></span><br/>    | <span data-ttu-id="148c1-124">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="148c1-124">No character data is permitted.</span></span><br/> <span data-ttu-id="148c1-125">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="148c1-125">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="148c1-126">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="148c1-126">Configuration Dependencies</span></span>

<span data-ttu-id="148c1-127">None</span><span class="sxs-lookup"><span data-stu-id="148c1-127">None</span></span>

## <a name="example"></a><span data-ttu-id="148c1-128">Пример</span><span class="sxs-lookup"><span data-stu-id="148c1-128">Example</span></span>

<span data-ttu-id="148c1-129">В следующем примере параметр инициализируется как 1.</span><span class="sxs-lookup"><span data-stu-id="148c1-129">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="148c1-130">В примере в [параметердеф](parameterdef.md) показано, как задать все обязательные элементы свойств для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="148c1-130">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="148c1-131">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="148c1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148c1-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="148c1-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




