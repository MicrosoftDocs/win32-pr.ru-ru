---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: жобури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb06148438b0fd6715370c56ff9efe54d512219
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693925"
---
# <a name="joburi"></a><span data-ttu-id="173a3-104">жобури</span><span class="sxs-lookup"><span data-stu-id="173a3-104">JobURI</span></span>

<span data-ttu-id="173a3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="173a3-105">This topic is not current.</span></span> <span data-ttu-id="173a3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="173a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="173a3-107">Задает универсальный код ресурса (URI) для документа.</span><span class="sxs-lookup"><span data-stu-id="173a3-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="173a3-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="173a3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="173a3-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="173a3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="173a3-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="173a3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="173a3-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="173a3-111">Element Information</span></span>



| <span data-ttu-id="173a3-112">Имя</span><span class="sxs-lookup"><span data-stu-id="173a3-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="173a3-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="173a3-113">Element Type</span></span> <br/>   | <span data-ttu-id="173a3-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="173a3-114">Property</span></span><br/> |
| <span data-ttu-id="173a3-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="173a3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="173a3-116">Задание</span><span class="sxs-lookup"><span data-stu-id="173a3-116">Job</span></span><br/>      |
| <span data-ttu-id="173a3-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="173a3-117">Notes</span></span> <br/>          | <span data-ttu-id="173a3-118">Нет</span><span class="sxs-lookup"><span data-stu-id="173a3-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="173a3-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="173a3-119">Structural Content</span></span>

<span data-ttu-id="173a3-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="173a3-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="173a3-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="173a3-121">Structure Variables</span></span>

<span data-ttu-id="173a3-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="173a3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="173a3-123">Имя</span><span class="sxs-lookup"><span data-stu-id="173a3-123">Name</span></span>                       | <span data-ttu-id="173a3-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="173a3-124">Data type</span></span>         | <span data-ttu-id="173a3-125">Unit</span><span class="sxs-lookup"><span data-stu-id="173a3-125">Unit</span></span> | <span data-ttu-id="173a3-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="173a3-126">Supported values</span></span> | <span data-ttu-id="173a3-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="173a3-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="173a3-128">\_жобуривалуе\_</span><span class="sxs-lookup"><span data-stu-id="173a3-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="173a3-129">строка</span><span class="sxs-lookup"><span data-stu-id="173a3-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="173a3-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="173a3-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="173a3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="173a3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173a3-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="173a3-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




