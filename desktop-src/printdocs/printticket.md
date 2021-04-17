---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684820"
---
# <a name="printticket"></a><span data-ttu-id="c6395-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="c6395-104">PrintTicket</span></span>

<span data-ttu-id="c6395-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c6395-105">This topic is not current.</span></span> <span data-ttu-id="c6395-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c6395-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c6395-107">Элемент PrintTicket является корневым элементом документа PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="c6395-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="c6395-108">Элемент PrintTicket содержит все сведения о форматировании заданий, необходимые для вывода задания.</span><span class="sxs-lookup"><span data-stu-id="c6395-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="c6395-109">Тег элемента</span><span class="sxs-lookup"><span data-stu-id="c6395-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="c6395-110">XML-атрибуты</span><span class="sxs-lookup"><span data-stu-id="c6395-110">XML Attributes</span></span>

<span data-ttu-id="c6395-111">В следующей таблице перечислены атрибуты XML, которые могут быть связаны с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="c6395-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="c6395-112">Атрибут XML</span><span class="sxs-lookup"><span data-stu-id="c6395-112">XML Attribute</span></span>      | <span data-ttu-id="c6395-113">Сведения</span><span class="sxs-lookup"><span data-stu-id="c6395-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6395-114">version</span><span class="sxs-lookup"><span data-stu-id="c6395-114">version</span></span><br/> | <span data-ttu-id="c6395-115">Указывает версию схемы, определяющую типы элементов и их структуру, литерал типа Integer.</span><span class="sxs-lookup"><span data-stu-id="c6395-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="c6395-116">Текущая версия схемы — "1".</span><span class="sxs-lookup"><span data-stu-id="c6395-116">The current schema version is "1".</span></span> <span data-ttu-id="c6395-117">Атрибут обязателен.</span><span class="sxs-lookup"><span data-stu-id="c6395-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="c6395-118">Дополнительные сведения см. в разделе [XML Attributes](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="c6395-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="c6395-119">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c6395-119">Element Information</span></span>

<span data-ttu-id="c6395-120">В следующей таблице перечислены элементы, которые могут быть родительскими для этого элемента, элементы, которые могут быть дочерними для этого элемента, и любые ограничения на сам элемент.</span><span class="sxs-lookup"><span data-stu-id="c6395-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="c6395-121">Категория</span><span class="sxs-lookup"><span data-stu-id="c6395-121">Category</span></span>                   | <span data-ttu-id="c6395-122">Сведения</span><span class="sxs-lookup"><span data-stu-id="c6395-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6395-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c6395-123">Parent elements</span></span><br/> | <span data-ttu-id="c6395-124">Только корневой документ.</span><span class="sxs-lookup"><span data-stu-id="c6395-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="c6395-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c6395-125">Child elements</span></span><br/>  | <span data-ttu-id="c6395-126">*Функция* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="c6395-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="c6395-127">*Параметеринит* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="c6395-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="c6395-128">*Свойство* (ноль или более)</span><span class="sxs-lookup"><span data-stu-id="c6395-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="c6395-129">Этот элемент</span><span class="sxs-lookup"><span data-stu-id="c6395-129">This element</span></span><br/>    | <span data-ttu-id="c6395-130">Символьные данные не допускаются.</span><span class="sxs-lookup"><span data-stu-id="c6395-130">No character data is permitted.</span></span><br/> <span data-ttu-id="c6395-131">Дублирование дочерних одноуровневых элементов не разрешено.</span><span class="sxs-lookup"><span data-stu-id="c6395-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="c6395-132">Зависимости конфигурации</span><span class="sxs-lookup"><span data-stu-id="c6395-132">Configuration Dependencies</span></span>

<span data-ttu-id="c6395-133">Зависимости конфигурации применимы только к элементам в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c6395-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="c6395-134">Пример</span><span class="sxs-lookup"><span data-stu-id="c6395-134">Example</span></span>

<span data-ttu-id="c6395-135">См. [Пример PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="c6395-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6395-136">См. также</span><span class="sxs-lookup"><span data-stu-id="c6395-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6395-137">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c6395-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




