---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: документури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9964df145e75fe2b30d670d5575928485e00c5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104000019"
---
# <a name="documenturi"></a><span data-ttu-id="98be8-104">документури</span><span class="sxs-lookup"><span data-stu-id="98be8-104">DocumentURI</span></span>

<span data-ttu-id="98be8-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="98be8-105">This topic is not current.</span></span> <span data-ttu-id="98be8-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98be8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98be8-107">Задает универсальный код ресурса (URI) для документа.</span><span class="sxs-lookup"><span data-stu-id="98be8-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="98be8-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98be8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98be8-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="98be8-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="98be8-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="98be8-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="98be8-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98be8-111">Element Information</span></span>



| <span data-ttu-id="98be8-112">Имя</span><span class="sxs-lookup"><span data-stu-id="98be8-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="98be8-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="98be8-113">Element Type</span></span> <br/>   | <span data-ttu-id="98be8-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="98be8-114">Property</span></span><br/> |
| <span data-ttu-id="98be8-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="98be8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98be8-116">Документ</span><span class="sxs-lookup"><span data-stu-id="98be8-116">Document</span></span><br/> |
| <span data-ttu-id="98be8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="98be8-117">Notes</span></span> <br/>          | <span data-ttu-id="98be8-118">Нет</span><span class="sxs-lookup"><span data-stu-id="98be8-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="98be8-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="98be8-119">Structural Content</span></span>

<span data-ttu-id="98be8-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="98be8-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="98be8-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="98be8-121">Structure Variables</span></span>

<span data-ttu-id="98be8-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="98be8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98be8-123">Имя</span><span class="sxs-lookup"><span data-stu-id="98be8-123">Name</span></span>                            | <span data-ttu-id="98be8-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="98be8-124">Data type</span></span>         | <span data-ttu-id="98be8-125">Unit</span><span class="sxs-lookup"><span data-stu-id="98be8-125">Unit</span></span> | <span data-ttu-id="98be8-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="98be8-126">Supported values</span></span> | <span data-ttu-id="98be8-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="98be8-127">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="98be8-128">\_документуривалуе\_</span><span class="sxs-lookup"><span data-stu-id="98be8-128">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="98be8-129">строка</span><span class="sxs-lookup"><span data-stu-id="98be8-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="98be8-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="98be8-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="98be8-131">См. также</span><span class="sxs-lookup"><span data-stu-id="98be8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98be8-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="98be8-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




