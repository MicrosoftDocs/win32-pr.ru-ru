---
description: Получение сведений о свойстве Документури. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7926ae9b-e195-4391-9006-1eb4cf386f88
title: документури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb4d1572417ac85e14c25c238be1d49611ba858
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548812"
---
# <a name="documenturi"></a><span data-ttu-id="bd2b3-105">документури</span><span class="sxs-lookup"><span data-stu-id="bd2b3-105">DocumentURI</span></span>

<span data-ttu-id="bd2b3-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="bd2b3-106">This topic is not current.</span></span> <span data-ttu-id="bd2b3-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bd2b3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd2b3-108">Задает универсальный код ресурса (URI) для документа.</span><span class="sxs-lookup"><span data-stu-id="bd2b3-108">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="bd2b3-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bd2b3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="bd2b3-110">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="bd2b3-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="bd2b3-111">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="bd2b3-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bd2b3-112">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bd2b3-112">Element Information</span></span>



| <span data-ttu-id="bd2b3-113">Имя</span><span class="sxs-lookup"><span data-stu-id="bd2b3-113">Name</span></span> | <span data-ttu-id="bd2b3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bd2b3-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="bd2b3-115">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="bd2b3-115">Element Type</span></span> <br/>   | <span data-ttu-id="bd2b3-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="bd2b3-116">Property</span></span><br/> |
| <span data-ttu-id="bd2b3-117">Префикс области</span><span class="sxs-lookup"><span data-stu-id="bd2b3-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bd2b3-118">Документ</span><span class="sxs-lookup"><span data-stu-id="bd2b3-118">Document</span></span><br/> |
| <span data-ttu-id="bd2b3-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd2b3-119">Notes</span></span> <br/>          | <span data-ttu-id="bd2b3-120">Нет</span><span class="sxs-lookup"><span data-stu-id="bd2b3-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="bd2b3-121">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="bd2b3-121">Structural Content</span></span>

<span data-ttu-id="bd2b3-122">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd2b3-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string">_DocumentURIValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="bd2b3-123">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="bd2b3-123">Structure Variables</span></span>

<span data-ttu-id="bd2b3-124">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="bd2b3-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bd2b3-125">Имя</span><span class="sxs-lookup"><span data-stu-id="bd2b3-125">Name</span></span>                            | <span data-ttu-id="bd2b3-126">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bd2b3-126">Data type</span></span>         | <span data-ttu-id="bd2b3-127">Unit</span><span class="sxs-lookup"><span data-stu-id="bd2b3-127">Unit</span></span> | <span data-ttu-id="bd2b3-128">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="bd2b3-128">Supported values</span></span> | <span data-ttu-id="bd2b3-129">Итоги</span><span class="sxs-lookup"><span data-stu-id="bd2b3-129">Summary</span></span> |
|---------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="bd2b3-130">\_документуривалуе\_</span><span class="sxs-lookup"><span data-stu-id="bd2b3-130">\_DocumentURIValue\_</span></span><br/> | <span data-ttu-id="bd2b3-131">строка</span><span class="sxs-lookup"><span data-stu-id="bd2b3-131">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bd2b3-132">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="bd2b3-132">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="bd2b3-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bd2b3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd2b3-134">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="bd2b3-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




