---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d05791f4f2214eeac7c2c55b6d13d97c12726
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997881"
---
# <a name="documentid"></a><span data-ttu-id="3480e-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="3480e-104">DocumentID</span></span>

<span data-ttu-id="3480e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="3480e-105">This topic is not current.</span></span> <span data-ttu-id="3480e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3480e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3480e-107">Указывает уникальный идентификатор документа.</span><span class="sxs-lookup"><span data-stu-id="3480e-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="3480e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3480e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3480e-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3480e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3480e-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3480e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3480e-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3480e-111">Element Information</span></span>



| <span data-ttu-id="3480e-112">Имя</span><span class="sxs-lookup"><span data-stu-id="3480e-112">Name</span></span> | <span data-ttu-id="3480e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3480e-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3480e-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="3480e-114">Element Type</span></span> <br/>   | <span data-ttu-id="3480e-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="3480e-115">Property</span></span><br/> |
| <span data-ttu-id="3480e-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="3480e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3480e-117">Документ</span><span class="sxs-lookup"><span data-stu-id="3480e-117">Document</span></span><br/> |
| <span data-ttu-id="3480e-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3480e-118">Notes</span></span> <br/>          | <span data-ttu-id="3480e-119">Нет</span><span class="sxs-lookup"><span data-stu-id="3480e-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3480e-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="3480e-120">Structural Content</span></span>

<span data-ttu-id="3480e-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3480e-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="3480e-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="3480e-122">Structure Variables</span></span>

<span data-ttu-id="3480e-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="3480e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3480e-124">Имя</span><span class="sxs-lookup"><span data-stu-id="3480e-124">Name</span></span>                           | <span data-ttu-id="3480e-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3480e-125">Data type</span></span>         | <span data-ttu-id="3480e-126">Unit</span><span class="sxs-lookup"><span data-stu-id="3480e-126">Unit</span></span> | <span data-ttu-id="3480e-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="3480e-127">Supported values</span></span> | <span data-ttu-id="3480e-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="3480e-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="3480e-129">\_документидвалуе\_</span><span class="sxs-lookup"><span data-stu-id="3480e-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="3480e-130">строка</span><span class="sxs-lookup"><span data-stu-id="3480e-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3480e-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3480e-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="3480e-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3480e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3480e-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="3480e-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




