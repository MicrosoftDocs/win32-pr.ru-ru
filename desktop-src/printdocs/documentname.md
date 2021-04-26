---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: acb25fd6-6706-43ee-9ac0-539f20c13390
title: Имя_документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66809ef18edb7aa313ea5218f9122acf4ddd1ee8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997801"
---
# <a name="documentname"></a><span data-ttu-id="d2b08-104">Имя_документа</span><span class="sxs-lookup"><span data-stu-id="d2b08-104">DocumentName</span></span>

<span data-ttu-id="d2b08-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d2b08-105">This topic is not current.</span></span> <span data-ttu-id="d2b08-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d2b08-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d2b08-107">Указывает описательное имя документа.</span><span class="sxs-lookup"><span data-stu-id="d2b08-107">Specifies a descriptive name for the document.</span></span>

-   [<span data-ttu-id="d2b08-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d2b08-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d2b08-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d2b08-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d2b08-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d2b08-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d2b08-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d2b08-111">Element Information</span></span>



| <span data-ttu-id="d2b08-112">Имя</span><span class="sxs-lookup"><span data-stu-id="d2b08-112">Name</span></span> | <span data-ttu-id="d2b08-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d2b08-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="d2b08-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d2b08-114">Element Type</span></span> <br/>   | <span data-ttu-id="d2b08-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="d2b08-115">Property</span></span><br/> |
| <span data-ttu-id="d2b08-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="d2b08-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d2b08-117">Документ</span><span class="sxs-lookup"><span data-stu-id="d2b08-117">Document</span></span><br/> |
| <span data-ttu-id="d2b08-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2b08-118">Notes</span></span> <br/>          | <span data-ttu-id="d2b08-119">Нет</span><span class="sxs-lookup"><span data-stu-id="d2b08-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="d2b08-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="d2b08-120">Structural Content</span></span>

<span data-ttu-id="d2b08-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2b08-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string">_DocumentNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="d2b08-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="d2b08-122">Structure Variables</span></span>

<span data-ttu-id="d2b08-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="d2b08-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d2b08-124">Имя</span><span class="sxs-lookup"><span data-stu-id="d2b08-124">Name</span></span>                             | <span data-ttu-id="d2b08-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d2b08-125">Data type</span></span>         | <span data-ttu-id="d2b08-126">Unit</span><span class="sxs-lookup"><span data-stu-id="d2b08-126">Unit</span></span> | <span data-ttu-id="d2b08-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="d2b08-127">Supported values</span></span> | <span data-ttu-id="d2b08-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="d2b08-128">Summary</span></span> |
|----------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="d2b08-129">\_документнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="d2b08-129">\_DocumentNameValue\_</span></span><br/> | <span data-ttu-id="d2b08-130">строка</span><span class="sxs-lookup"><span data-stu-id="d2b08-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d2b08-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d2b08-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="d2b08-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d2b08-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2b08-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d2b08-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




