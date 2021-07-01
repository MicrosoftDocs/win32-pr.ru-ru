---
description: Поиск сведений об элементе PrintTicket. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120079"
---
# <a name="printticket"></a><span data-ttu-id="77dd7-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="77dd7-105">PrintTicket</span></span>

<span data-ttu-id="77dd7-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="77dd7-106">This topic is not current.</span></span> <span data-ttu-id="77dd7-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="77dd7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="77dd7-108">Элемент PrintTicket является корневым элементом документа PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="77dd7-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="77dd7-109">Элемент PrintTicket содержит все сведения о форматировании заданий, необходимые для вывода задания.</span><span class="sxs-lookup"><span data-stu-id="77dd7-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="77dd7-110">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="77dd7-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="77dd7-111">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="77dd7-111">XML Attributes</span></span>

<span data-ttu-id="77dd7-112">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="77dd7-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="77dd7-113">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="77dd7-113">XML Attribute</span></span>      | <span data-ttu-id="77dd7-114">Сведения</span><span class="sxs-lookup"><span data-stu-id="77dd7-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dd7-115">version</span><span class="sxs-lookup"><span data-stu-id="77dd7-115">version</span></span><br/> | <span data-ttu-id="77dd7-116">Указывает версию схемы, определяющую типы элементов и их структуру, литерал типа Integer.</span><span class="sxs-lookup"><span data-stu-id="77dd7-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="77dd7-117">Текущая версия схемы — "1".</span><span class="sxs-lookup"><span data-stu-id="77dd7-117">The current schema version is "1".</span></span> <span data-ttu-id="77dd7-118">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="77dd7-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="77dd7-119">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="77dd7-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="77dd7-120">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="77dd7-120">Element Information</span></span>

<span data-ttu-id="77dd7-121">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="77dd7-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="77dd7-122">Категория</span><span class="sxs-lookup"><span data-stu-id="77dd7-122">Category</span></span>                   | <span data-ttu-id="77dd7-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="77dd7-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77dd7-124">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="77dd7-124">Parent elements</span></span><br/> | <span data-ttu-id="77dd7-125">Только корневой документ.</span><span class="sxs-lookup"><span data-stu-id="77dd7-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="77dd7-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="77dd7-126">Child elements</span></span><br/>  | <span data-ttu-id="77dd7-127">*Функция* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="77dd7-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="77dd7-128">*Параметеринит* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="77dd7-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="77dd7-129">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="77dd7-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="77dd7-130">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="77dd7-130">This element</span></span><br/>    | <span data-ttu-id="77dd7-131">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="77dd7-131">No character data is permitted.</span></span><br/> <span data-ttu-id="77dd7-132">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="77dd7-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="77dd7-133">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="77dd7-133">Configuration Dependencies</span></span>

<span data-ttu-id="77dd7-134">Зависимости конфигурации применимы только к элементам в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="77dd7-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="77dd7-135">Пример</span><span class="sxs-lookup"><span data-stu-id="77dd7-135">Example</span></span>

<span data-ttu-id="77dd7-136">См. [Пример PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="77dd7-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77dd7-137">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="77dd7-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77dd7-138">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="77dd7-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




