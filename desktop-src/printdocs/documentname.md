---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Имя_документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5f087744f40111f176e6797dab356c5d290d8f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820412"
---
# <a name="documentname"></a><span data-ttu-id="61305-104">Имя_документа</span><span class="sxs-lookup"><span data-stu-id="61305-104">DocumentName</span></span>

<span data-ttu-id="61305-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="61305-105">This topic is not current.</span></span> <span data-ttu-id="61305-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="61305-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="61305-107">Указывает описательное имя документа.</span><span class="sxs-lookup"><span data-stu-id="61305-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="61305-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="61305-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="61305-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="61305-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="61305-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="61305-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="61305-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="61305-111">Element Information</span></span>



| <span data-ttu-id="61305-112">Имя</span><span class="sxs-lookup"><span data-stu-id="61305-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="61305-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="61305-113">Element Type</span></span> <br/>   | <span data-ttu-id="61305-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="61305-114">Property</span></span><br/> |
| <span data-ttu-id="61305-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="61305-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="61305-116">Документ</span><span class="sxs-lookup"><span data-stu-id="61305-116">Document</span></span><br/> |
| <span data-ttu-id="61305-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="61305-117">Notes</span></span> <br/>          | <span data-ttu-id="61305-118">Нет</span><span class="sxs-lookup"><span data-stu-id="61305-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="61305-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="61305-119">Structural Content</span></span>

<span data-ttu-id="61305-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61305-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="61305-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="61305-121">Structure Variables</span></span>

<span data-ttu-id="61305-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="61305-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="61305-123">Имя</span><span class="sxs-lookup"><span data-stu-id="61305-123">Name</span></span>                             | <span data-ttu-id="61305-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="61305-124">Data type</span></span>         | <span data-ttu-id="61305-125">Unit</span><span class="sxs-lookup"><span data-stu-id="61305-125">Unit</span></span> | <span data-ttu-id="61305-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="61305-126">Supported values</span></span> | <span data-ttu-id="61305-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="61305-127">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="61305-128">\_документнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="61305-128">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="61305-129">строка</span><span class="sxs-lookup"><span data-stu-id="61305-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="61305-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="61305-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="61305-131">См. также</span><span class="sxs-lookup"><span data-stu-id="61305-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61305-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="61305-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




