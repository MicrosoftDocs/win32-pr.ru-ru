---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: жобури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c80611a4e7dbd10f4841fae098578f0a8fdc96
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993891"
---
# <a name="joburi"></a><span data-ttu-id="36986-104">жобури</span><span class="sxs-lookup"><span data-stu-id="36986-104">JobURI</span></span>

<span data-ttu-id="36986-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="36986-105">This topic is not current.</span></span> <span data-ttu-id="36986-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="36986-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36986-107">Задает универсальный код ресурса (URI) для документа.</span><span class="sxs-lookup"><span data-stu-id="36986-107">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="36986-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="36986-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="36986-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="36986-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="36986-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="36986-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="36986-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="36986-111">Element Information</span></span>



| <span data-ttu-id="36986-112">Имя</span><span class="sxs-lookup"><span data-stu-id="36986-112">Name</span></span> | <span data-ttu-id="36986-113">Значение</span><span class="sxs-lookup"><span data-stu-id="36986-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="36986-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="36986-114">Element Type</span></span> <br/>   | <span data-ttu-id="36986-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="36986-115">Property</span></span><br/> |
| <span data-ttu-id="36986-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="36986-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="36986-117">Задание</span><span class="sxs-lookup"><span data-stu-id="36986-117">Job</span></span><br/>      |
| <span data-ttu-id="36986-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="36986-118">Notes</span></span> <br/>          | <span data-ttu-id="36986-119">Нет</span><span class="sxs-lookup"><span data-stu-id="36986-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="36986-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="36986-120">Structural Content</span></span>

<span data-ttu-id="36986-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="36986-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="36986-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="36986-122">Structure Variables</span></span>

<span data-ttu-id="36986-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="36986-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="36986-124">Имя</span><span class="sxs-lookup"><span data-stu-id="36986-124">Name</span></span>                       | <span data-ttu-id="36986-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="36986-125">Data type</span></span>         | <span data-ttu-id="36986-126">Unit</span><span class="sxs-lookup"><span data-stu-id="36986-126">Unit</span></span> | <span data-ttu-id="36986-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="36986-127">Supported values</span></span> | <span data-ttu-id="36986-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="36986-128">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="36986-129">\_жобуривалуе\_</span><span class="sxs-lookup"><span data-stu-id="36986-129">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="36986-130">строка</span><span class="sxs-lookup"><span data-stu-id="36986-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="36986-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="36986-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="36986-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="36986-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36986-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="36986-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




