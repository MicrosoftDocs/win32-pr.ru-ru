---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720827"
---
# <a name="printcapabilities"></a><span data-ttu-id="74d18-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="74d18-104">PrintCapabilities</span></span>

<span data-ttu-id="74d18-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="74d18-105">This topic is not current.</span></span> <span data-ttu-id="74d18-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74d18-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74d18-107">Элемент PrintCapabilities представляет корень документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="74d18-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="74d18-108">Документ PrintCapabilities содержит все сведения, необходимые для описания поддерживаемых атрибутов устройств с учетом конкретной конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="74d18-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="74d18-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="74d18-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="74d18-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="74d18-110">XML Attributes</span></span>

<span data-ttu-id="74d18-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="74d18-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="74d18-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="74d18-112">XML Attribute</span></span>      | <span data-ttu-id="74d18-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="74d18-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d18-114">version</span><span class="sxs-lookup"><span data-stu-id="74d18-114">version</span></span><br/> | <span data-ttu-id="74d18-115">Указывает версию схемы, определяющую типы элементов и их структуру.</span><span class="sxs-lookup"><span data-stu-id="74d18-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="74d18-116">Атрибут Version имеет тип Integer.</span><span class="sxs-lookup"><span data-stu-id="74d18-116">The version attribute is of type integer.</span></span> <span data-ttu-id="74d18-117">Текущая версия схемы обозначена как "1".</span><span class="sxs-lookup"><span data-stu-id="74d18-117">The current schema version is designated "1".</span></span> <span data-ttu-id="74d18-118">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="74d18-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="74d18-119">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="74d18-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="74d18-120">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="74d18-120">Element Information</span></span>

<span data-ttu-id="74d18-121">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="74d18-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="74d18-122">Категория</span><span class="sxs-lookup"><span data-stu-id="74d18-122">Category</span></span>                   | <span data-ttu-id="74d18-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="74d18-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d18-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="74d18-124">Parent elements</span></span><br/> | <span data-ttu-id="74d18-125">Только корневой документ.</span><span class="sxs-lookup"><span data-stu-id="74d18-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="74d18-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="74d18-126">Child elements</span></span><br/>  | <span data-ttu-id="74d18-127">*Функция* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="74d18-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="74d18-128">*Параметердеф* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="74d18-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="74d18-129">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="74d18-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="74d18-130">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="74d18-130">This element</span></span><br/>    | <span data-ttu-id="74d18-131">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="74d18-131">No character data is permitted.</span></span><br/> <span data-ttu-id="74d18-132">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="74d18-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="74d18-133">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="74d18-133">Configuration Dependencies</span></span>

<span data-ttu-id="74d18-134">Корневой элемент не может иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="74d18-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="74d18-135">Пример</span><span class="sxs-lookup"><span data-stu-id="74d18-135">Example</span></span>

<span data-ttu-id="74d18-136">См. [Пример документа PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="74d18-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="74d18-137">См. также</span><span class="sxs-lookup"><span data-stu-id="74d18-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74d18-138">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="74d18-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




