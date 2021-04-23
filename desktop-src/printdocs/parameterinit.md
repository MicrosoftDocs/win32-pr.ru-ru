---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: параметеринит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273325"
---
# <a name="parameterinit"></a><span data-ttu-id="6dfd9-104">параметеринит</span><span class="sxs-lookup"><span data-stu-id="6dfd9-104">ParameterInit</span></span>

<span data-ttu-id="6dfd9-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-105">This topic is not current.</span></span> <span data-ttu-id="6dfd9-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6dfd9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6dfd9-107">Определяет значение для экземпляра элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="6dfd9-108">Элемент Параметеринит является целевым объектом ссылки, созданной элементом ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="6dfd9-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="6dfd9-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="6dfd9-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="6dfd9-110">XML Attributes</span></span>

<span data-ttu-id="6dfd9-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="6dfd9-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="6dfd9-112">XML Attribute</span></span>   | <span data-ttu-id="6dfd9-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="6dfd9-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfd9-114">name</span><span class="sxs-lookup"><span data-stu-id="6dfd9-114">name</span></span><br/> | <span data-ttu-id="6dfd9-115">Содержит атрибут Name элемента Параметердеф, который должен быть инициализирован в контексте текущего документа.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="6dfd9-116">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="6dfd9-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="6dfd9-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6dfd9-117">Element Information</span></span>

<span data-ttu-id="6dfd9-118">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="6dfd9-119">Категория</span><span class="sxs-lookup"><span data-stu-id="6dfd9-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfd9-120">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6dfd9-120">Parent elements</span></span><br/> | <span data-ttu-id="6dfd9-121">PrintTicket (корневой элемент PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="6dfd9-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="6dfd9-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6dfd9-122">Child elements</span></span><br/>  | <span data-ttu-id="6dfd9-123">Значение (одно)</span><span class="sxs-lookup"><span data-stu-id="6dfd9-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="6dfd9-124">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="6dfd9-124">This element</span></span><br/>    | <span data-ttu-id="6dfd9-125">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-125">No character data is permitted.</span></span><br/> <span data-ttu-id="6dfd9-126">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="6dfd9-127">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="6dfd9-127">Configuration Dependencies</span></span>

<span data-ttu-id="6dfd9-128">None</span><span class="sxs-lookup"><span data-stu-id="6dfd9-128">None</span></span>

## <a name="example"></a><span data-ttu-id="6dfd9-129">Пример</span><span class="sxs-lookup"><span data-stu-id="6dfd9-129">Example</span></span>

<span data-ttu-id="6dfd9-130">В следующем примере параметр инициализируется как 1.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="6dfd9-131">В примере в [параметердеф](parameterdef.md) показано, как задать все обязательные элементы свойств для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6dfd9-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="6dfd9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6dfd9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dfd9-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6dfd9-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




